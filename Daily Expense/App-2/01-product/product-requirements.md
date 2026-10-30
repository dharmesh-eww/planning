# Product Requirements — Motion Ledger

## Vision
Make everyday money tracking clear, responsive, and rewarding without gamifying spending. Help users understand income, expenses, remaining budgets, and spending patterns.

## Scope
1. Home overview: balance, income, expenses, budget health, recent activity.
2. Expense, income, and transfer CRUD.
3. Accounts, categories/subcategories, custom categories.
4. Monthly/custom budgets and rollover settings.
5. Reports: cash flow, category breakdown, trends and comparisons.
6. Calendar, search, filters, recurring reminders, savings goals.
7. Local export/import/backup.
8. Optional Google Sheets export/sync with explicit consent.
9. Language picker and ten-language localization.

## Non-functional
Offline-first; SQLite authoritative; privacy by design; exact money arithmetic; accessible contrast; text scaling; RTL; screen readers; reduced motion; smooth performance on entry-level Android.

## Exclusions
No open banking, bank credential collection, automatic SMS parsing, investment advice, credit scoring, social leaderboards, or financial product sales.

## Acceptance
A user can select a language, create an account, record an expense, set a budget, and view reports offline. No Google access occurs until user explicitly requests it.
