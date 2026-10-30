# Google Sheets Integration Plan

## Goal
Let users optionally keep a copy of their finance records in a spreadsheet they own, without operating an app backend.

## Recommended user experience
1. App explains why Sheets access is requested and exactly what data is transferred.
2. User taps Connect Google Sheets.
3. Native OAuth authorization is requested only at this point.
4. User creates a new spreadsheet or selects a specific existing spreadsheet using a supported Google file-picker flow.
5. App previews worksheet names and columns.
6. User selects one-time export or ongoing sync.
7. User confirms first transfer.
8. App writes to the selected spreadsheet and displays last sync/pending changes.

## Authorization design
- Use OAuth 2.0 for the installed mobile app; do not use a service account because the sheet belongs to the user.
- Prefer the narrow Google Drive scope drive.file, which limits access to files created/opened with the app. Confirm that the chosen picker and target-sheet workflow supports this scope.
- Avoid broad spreadsheets or Drive scopes unless a concrete product requirement proves they are necessary.
- Do not request Google access during first-launch onboarding.
- Use incremental authorization when adding a capability that needs a new scope.
- Handle partial/denied permissions gracefully.
- Tokens must be held in platform secure storage and excluded from logs, backups, analytics, and SQLite.
- Do not implement server-side offline access/refresh-token handling because this product has no backend. Use supported native authorization flows and reacquire short-lived access when required.

## API and configuration
Enable Google Sheets API in a Google Cloud project. Configure OAuth consent screen, app branding, audience, platform-specific OAuth clients, and requested scopes. Public apps requesting sensitive scopes may require Google verification. Confirm current Google policy and verification requirements before release.

## Spreadsheet structure
Use one app-owned workbook with separate tabs:
- Transactions
- Accounts
- Categories
- Budgets
- Transfers
- RecurringRules (optional)
- AppMetadata

Include schema_version, export timestamp, stable local IDs, currency code, minor-unit amount, created_at, updated_at, and deleted_at/tombstone where relevant. Keep user-visible header labels localizable only if app parses stable machine column IDs separately.

## Sync model
SQLite remains the source of truth. Each local change creates an outbox entry. Sync sends idempotent upserts keyed by stable UUID. Maintain a local mapping to spreadsheet and worksheet IDs. Avoid duplicate append-only rows.

## Conflict handling
Store local revision and last-known remote revision. If both sides changed since last sync, mark conflict and show record details. Default to no silent overwrite. Offer keep local, use sheet version, or review field differences. Save conflict snapshot before applying.

## Deletion
Use tombstones rather than immediate remote row deletion. Explain remote deletion behavior. A user may choose whether deleting locally should delete the matching spreadsheet row.

## Reliability
- Sync only when connected, authorized, and online.
- Retry transient errors with exponential backoff.
- Respect API quotas and batch reads/writes.
- Validate spreadsheet headers and schema before writing.
- If user edits columns manually, warn and avoid destructive schema rewrites.
- Retain pending local changes after auth/network failure.
- Provide manual sync and pause controls.

## Disconnect
Stop future sync, clear local auth tokens and connection metadata securely, retain SQLite data, and leave the user's spreadsheet untouched. Explain that the user can separately delete the spreadsheet from Google Drive.

## Limitations to disclose
No app server means no guaranteed unattended sync while the app is closed and no server-held long-lived token. Background sync depends on mobile OS scheduling and native authorization/token lifecycle. Treat sync as best-effort; provide manual sync and export.
