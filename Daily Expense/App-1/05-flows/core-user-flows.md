# Core User Flows

## First launch
Splash → initialize SQLite/migrations → language selection → currency/locale preferences → optional account/category setup → Home. No sign-in required.

## Add an expense
Home/Transactions → Add Expense → enter amount → choose category/account/date → optional note → Save → local SQLite commit → dashboard/list updates immediately.

## Add income
Home → Add Income → amount/source category/account/date → Save locally. Income is distinct from transfers.

## Create a budget
Budgets → choose period and currency → choose total or category budget → set limit → save → progress is calculated from eligible expense transactions.

## Review spending
Reports → select period/account/currency → view category breakdown and trends → tap category to open filtered transactions. Never combine unlike currencies.

## Transfer between accounts
Accounts → Transfer → choose source/destination → amount/date → confirm. A transfer is not income or expense; update both account balances atomically.

## Recurring item
More → Recurring → create rule → frequency and next date → optional local reminder → user reviews/creates each occurrence or enables clearly disclosed automatic local generation.

## Connect Google Sheets
More → Data & Backup → Google Sheets → explain data and scope → user chooses Connect → Google authorization → choose/create spreadsheet → preview worksheet schema → choose export or sync mode → confirm first transfer → sync status visible.

## Offline sync
User edits while offline → local write and outbox event → pending sync indicator → network returns → authorized sync runs → validate response → mark synced. Local data remains primary.

## Conflict resolution
If same record changed in both places, compare timestamps/revisions and show field-level choice. Never silently overwrite a newer local edit with sheet data. Preserve a recoverable copy before applying a conflict choice.

## Disconnect Google
Settings → Google Sheets → Disconnect → stop future sync and remove locally stored tokens/metadata as appropriate. Explain that disconnecting does not delete the user's Google spreadsheet or local SQLite records.

## Backup/restore
Export local database/CSV → user selects destination. Restore validates schema and previews counts before merge/replace. Keep a backup before replace.

## Failure states
Consent denied: app works normally. Token expired/revoked: reconnect required, queued changes retained. Spreadsheet deleted/unshared: pause sync and offer another sheet. Quota/network error: backoff and visible retry. Invalid external row: quarantine/report row; do not corrupt local database.
