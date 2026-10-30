# Daily Expense & Budget Tracker — App-1

## Product concept
A privacy-first, offline-first personal finance tracker. Users record income and expenses, organize categories, set budgets, understand spending, and optionally connect a Google Sheet they own for backup/export or synchronization.

## Core architecture
- Flutter application.
- SQLite via sqflite is the source of truth on the device.
- Optional direct Google Sheets API integration using the user's explicit Google authorization.
- No custom backend/server, Firebase, mandatory login, or app-owned cloud database.
- No personal finance data is sent to the developer's infrastructure.
- All core tracking, budgets, and reports work offline.

## Main features
1. Dashboard with balances, income, expenses, remaining budget, and recent transactions.
2. Add/edit income and expense transactions.
3. Categories and subcategories.
4. Accounts/wallets/cash/bank accounts.
5. Monthly and custom-period budgets.
6. Reports and spending insights.
7. Calendar and transaction history.
8. Search, filters, and transaction detail.
9. Recurring transaction reminders/creation.
10. Savings goals (optional).
11. Export/import and optional Google Sheets connection.
12. Multi-language app localization and language selection.

## Initial localization languages
English, Hindi, Bengali, Gujarati, Kannada, Marathi, Nepali, Punjabi, Tamil, and Telugu. Every visible label, message, validation error, notification, accessibility label, empty state, and Google Sheets connection instruction must be localized. See 08-localization.

## Data ownership
SQLite is the primary local store. Google Sheets is an optional user-owned destination. The user chooses whether to connect, which spreadsheet to use, and whether to export or enable sync. Do not upload data without explicit consent. Explain that Google Sheets is controlled by the user's Google account and is not the app's private database.

## Google Sheets integration
- User-initiated connection; app remains fully usable when declined.
- OAuth authorization and Sheets API calls are made directly from the mobile app.
- Prefer the narrow drive.file scope for files created/opened by this app; do not request broad Drive access by default.
- User may create a new spreadsheet or select an existing spreadsheet through an appropriate Google file picker flow.
- Store tokens securely using platform secure storage; never store tokens in SQLite or logs.
- Queue pending sync operations locally and retry when online.
- Show sync state, last successful sync, conflicts, and disconnect/revoke controls.
- No server-side refresh-token storage or server-mediated offline access.

## Screens
See 06-screens for screen-by-screen specifications. Planning includes 18 primary screens plus dialogs and sheets.

## Technical and product constraints
- SQLite local-first, transactional writes, migrations, backup/export.
- Multi-currency data model; do not sum unlike currencies without explicit conversion rates.
- Store money as integer minor units (or exact decimal representation), never binary floating-point.
- Locale-aware date, number, and currency formatting.
- Support RTL and text scaling.
- Privacy by design: no account required, no cloud sync except optional user-authorized Google Sheets.
- Ad placement, if used, must never interrupt transaction entry or sensitive financial screens.

## Scope exclusions
No bank account scraping, open-banking aggregation, automatic SMS parsing by default, investment advice, credit scoring, financial product sales, or backend analytics containing financial data.
