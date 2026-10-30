# Daily Expense & Budget Tracker — App-3: Bloom Ledger

## Concept
Bloom Ledger is a warm, nature-inspired financial planner. It uses an editorial paper-like canvas, forest-green navigation, soft botanical illustrations, rounded tactile cards, and calm progress storytelling. This is a third visual direction, distinct from App-1's calm utility and App-2's dark motion-led instrument panel.

## Product and technical constraints
- Flutter app; SQLite via sqflite is the local source of truth.
- Offline-first; all core tracking and reporting works without internet.
- Optional user-owned Google Sheets connection, only with explicit authorization and transfer confirmation.
- No developer server, API backend, Firebase, app-owned cloud database, or mandatory account.
- No financial data sent to developer infrastructure.
- Best-effort Sheets sync only; no promise of guaranteed background sync when app is closed.

## Feature scope
Dashboard, expense/income/transfer entry, accounts, categories, budgets, reports, calendar, recurring transactions, savings goals, search, export/import, local backup, optional Google Sheets, and language selection.

## Localization
English, Hindi, Bengali, Gujarati, Kannada, Marathi, Nepali, Punjabi, Tamil, Telugu. Every app-owned string, validation, empty state, chart summary, notification, accessibility label, and Sheets sync state must be localized.

## Visual assets
- [UI showcase SVG](08-visual-assets/app3-ui-showcase.svg)
- [Illustration assets SVG](08-visual-assets/illustration-assets.svg)
- [Motion storyboard SVG](08-visual-assets/motion-storyboard.svg)
- [Image reference board](08-visual-assets/image-reference.md)

These are vector concept assets for planning and can be opened directly on GitHub. They are illustrative references, not production Flutter screenshots.

## Core integrity rules
Money is integer minor units plus ISO currency code. Never use binary floating point or aggregate unlike currencies without explicit conversion. Transfers are not income/expense. User-entered notes/custom names remain verbatim.
