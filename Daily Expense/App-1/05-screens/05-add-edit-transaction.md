# Screen 05 — Add/Edit Transaction

## Purpose
Record an expense or income quickly and accurately.

## Fields
Type (Expense/Income), amount, currency, category, account, date/time, optional note, optional merchant, optional tags.

## Layout
Prominent amount field with locale-aware decimal separator and numeric keypad. Clear category and account selectors. Save action remains visible.

## Behavior
Validate positive amount, supported currency precision, required category/account rules, and date. Save transaction in a SQLite transaction and update UI immediately. Edit preserves ID and created_at while updating updated_at. Confirm delete.

## Important
Transfers use a separate flow and must not be recorded as expense/income. Persist money as integer minor units, not floating point.

## Acceptance
All labels, validation messages, hints, and accessibility descriptions are localized. Offline save always works.
