# Privacy and Security Requirements

## Data classification
Financial transactions, balances, notes, merchant names, account labels, budgets, and goals are sensitive personal data.

## Local storage
- Store records in SQLite in app-private storage.
- Do not include database contents in crash logs or analytics.
- Consider platform backup behavior; explain whether local OS backups include the database and offer a local export.
- Secure sensitive connection tokens using Keychain/Android Keystore-backed secure storage.
- Never store OAuth tokens in SQLite, plain preferences, source code, or logs.

## Google Sheets
- Explicit opt-in, clear scope explanation, selected spreadsheet, and first-sync confirmation.
- No transfer to developer-owned infrastructure.
- Use least-privilege OAuth scopes.
- Provide disconnect and permission-revocation guidance.
- Google Sheet content is visible to whoever the user shares that spreadsheet with; explain this before enabling sync.

## App access
Optional app lock/biometric lock may protect local display, but must not be described as encryption of the SQLite database unless actual database encryption is implemented and keys are safely managed.

## Data deletion
Provide delete-all-local-data flow with confirmation and optional export reminder. Disconnecting Sheets must not delete local data or remote spreadsheet. Remote cleanup is a separate explicit action.

## Threat considerations
Lost device, rooted/jailbroken device, malicious exported file, spreadsheet shared too broadly, revoked OAuth, token leakage, and user-edited sheet schema. Provide clear warnings and safe recovery.
