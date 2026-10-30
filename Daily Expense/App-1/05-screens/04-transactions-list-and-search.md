# Screen 04 — Transactions List and Search

## Layout
Date-grouped transaction list; search field; filters for type, category, account, date range, and amount; sort options; Add action.

## Row content
Category icon and localized category name, note/merchant, date/account, formatted amount, and clear income/expense indicator.

## Behavior
Search note and merchant text. Preserve filters and scroll position when opening a transaction. Support empty results and clear filters. Use locale-aware currency formatting.

## Acceptance
Transactions are read from SQLite. No network required. Do not use color as the only type indicator.
