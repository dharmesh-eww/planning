# Screen 03 — Home Dashboard

## Purpose
Answer: how much came in, how much went out, and how much budget remains?

## Layout
- Period selector (today/week/month/custom).
- Income, expense, and net summary in selected currency/account context.
- Budget progress and remaining amount.
- Spending category highlights.
- Recent transactions.
- Clear Add Expense and Add Income actions.

## Behavior
Totals update immediately from SQLite. If multiple currencies/accounts exist, show selected scope and never silently combine currencies. Allow hide/show balances. Tap summary/category to open filtered transactions.

## Visual direction
Calm, high-contrast financial summary. Simple charts with accessible text summaries. No distracting animation.

## Acceptance
Useful offline, empty state guides first transaction, and no personal finance data is sent to a server.
