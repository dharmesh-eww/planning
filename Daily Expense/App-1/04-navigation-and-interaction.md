# Navigation and Interaction

## Primary navigation
1. **Home** — current-period overview, quick add, budget snapshot.
2. **Transactions** — history, search, filters.
3. **Budgets** — monthly/weekly/custom budgets and progress.
4. **Reports** — category and time-based insights.
5. **More** — accounts, categories, recurring items, goals, export, Google Sheets, settings.

## Global actions
Add Expense and Add Income should be reachable from Home and Transactions. Consider a prominent floating action with an explicit choice, not an ambiguous plus icon alone.

## Navigation rules
- Preserve filter and scroll state when returning to transaction detail.
- Transaction form can open from dashboard, list, budget category, or calendar; preserve origin context on save/cancel.
- Use confirmation for irreversible delete and reset.
- Back closes sheets/dialogs before leaving the current screen.
- No login gate; Google connection lives under optional data/export settings.

## Interaction patterns
- Amount entry uses numeric keypad and locale-aware decimal separator.
- Date selection uses locale-aware calendar and first weekday.
- Category selection supports search and custom category creation.
- Account selection is explicit when multiple accounts exist.
- Reports include text summaries so charts are not the only way to understand data.
- Budget status includes amount remaining and period dates.
- Sync state is visible in Google Sheets settings and export history.

## Accessibility
All icons have labels; color is never the sole status indicator. Support text scaling, screen readers, RTL, focus order, and reduced motion.
