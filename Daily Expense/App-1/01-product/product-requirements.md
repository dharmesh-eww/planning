# Product Requirements

## Vision
Make everyday money tracking simple, understandable, private, and dependable—even without an internet connection.

## Target users
Individuals and households who want to record cash/bank income and expenses, monitor budgets, and review spending. Avoid assuming a specific country, currency, bank, or financial literacy level.

## Core user jobs
- Record an expense or income in a few seconds.
- Know how much was spent today, this month, and by category.
- Track spending against a budget.
- Compare income and expenses across periods.
- Search and correct past transactions.
- Keep records locally and optionally export/sync to a personally owned Google Sheet.

## Functional requirements
- Create, edit, duplicate, and delete transactions.
- Transaction fields: type, amount, currency, date/time, category, account, note, optional merchant, optional tags, optional attachment reference.
- Category management with default and custom categories.
- Multiple accounts with opening balances and account transfers.
- Budgets by period and category; configurable rollover policy.
- Dashboard date range and currency context.
- Reports by category, account, time, and income/expense.
- Search by note, merchant, amount range, category, and date.
- Recurring transaction templates and local reminders.
- CSV export/import and local backup/restore.
- Optional Google Sheets export and sync.
- All personal records remain accessible offline.

## Money correctness
- Store amount as integer minor units with currency code and currency exponent/metadata.
- Do not use double for persisted financial amounts.
- Keep original currency on each transaction.
- Never add different currencies into one total without a user-selected exchange-rate source and timestamp.
- Distinguish transfer between accounts from income/expense to avoid double-counting.
- Define rounding rules and preserve exact values through edit/export/import.

## Non-functional requirements
Fast transaction entry and dashboard load. Database migrations preserve user records. Reliable writes and crash-safe import/sync. Clear empty, loading, error, offline, and permission-denied states. Accessible labels, touch targets, contrast, text scaling, and RTL. No critical flow depends on network availability.

## Privacy
No mandatory account, no app server, no Firebase, no developer-hosted storage. The app does not collect or transmit transaction content to the developer. Google Sheets connection is optional and user-authorized. Explain exactly which spreadsheet/file is accessed and what data is written.

## Monetization
If ads are later used, keep them away from add/edit transaction, account balances, budget alerts, reports, export, and Google authorization screens. Never use financial records for ad targeting.
