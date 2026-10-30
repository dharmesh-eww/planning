# Screen 13 — Recurring Transactions

## Layout
List of recurring rules with amount, type, category, frequency, next date, and active state.

## Behavior
Create/edit/pause/delete rule. Frequency options include daily, weekly, monthly, yearly, and custom interval where feasible. Handle month-end dates explicitly. Provide local reminders. Make it clear whether occurrences are auto-created or require confirmation.

## Acceptance
Recurring rule does not silently create duplicate transactions after app restore or date/time changes. Store a last-generated occurrence marker.
