# Release and Testing Checklist

## Data
- [ ] Offline CRUD, budgets, reports, search.
- [ ] SQLite migrations and backup recovery.
- [ ] Exact money arithmetic, currency isolation, transfers excluded from income/expense.
- [ ] Export/import behavior verified.

## Google Sheets
- [ ] No OAuth prompt before user intent.
- [ ] Scope/data explained, destination chosen, first transfer confirmed.
- [ ] Outbox, idempotency, retries, conflicts and revocation tested.
- [ ] Disconnect retains local DB and remote Sheet.
- [ ] No guarantee of sync when app is closed.

## Localization/accessibility
- [ ] Ten locales and identical keys.
- [ ] No hardcoded UI strings, including Lottie/chart descriptions.
- [ ] Native review, text scaling, RTL/mixed-script, screen reader and contrast.
- [ ] Reduced-motion and focus order.

## Motion/performance
- [ ] Assets licensed, optimized, local and have static fallbacks.
- [ ] Save/navigation never wait for animation.
- [ ] Off-screen controllers pause/dispose.
- [ ] Profile frame time and memory on entry-level Android.
