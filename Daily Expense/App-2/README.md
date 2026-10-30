# Daily Expense & Budget Tracker — App-2: Motion Ledger

A motion-led, premium personal finance tracker with a distinct dark-first visual system, expressive data visualization, smooth transitions, and purposeful Lottie feedback.

## Inherited product constraints
- Flutter; SQLite via sqflite is the primary/source-of-truth local database.
- Offline-first: transactions, accounts, budgets, reports, and goals work without internet.
- Optional user-owned Google Sheets integration, only after explicit user authorization and confirmation.
- No developer server, API backend, Firebase, app-owned cloud database, or mandatory login.
- No personal finance data sent to developer infrastructure.
- Google Sheets sync is best-effort; do not promise guaranteed sync while app is closed.

## Features
Dashboard, expense/income/transfer entry, categories, accounts, budgets, reports, calendar, recurring transactions, savings goals, search, export/import, local backup, optional Google Sheets, and language selection.

## Languages
English, Hindi, Bengali, Gujarati, Kannada, Marathi, Nepali, Punjabi, Tamil, Telugu. Every app-owned UI string, error, notification, chart summary, accessibility label, and sync message must be localized.

## Design
See 02-design. Lottie assets are planned and specified in 07-assets; actual licensed JSON assets must be sourced and verified before implementation. Respect reduced-motion settings.

## Data integrity
Money is integer minor units + ISO currency code. No binary floating point; no implicit cross-currency aggregation. Transfers are not income/expense. User notes/custom names are not auto-translated.
