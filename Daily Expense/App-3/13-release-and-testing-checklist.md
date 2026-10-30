# Release and Testing Checklist

## Core
- [ ] Offline CRUD, budgets, reports, search, goals.
- [ ] SQLite migrations, transaction integrity, backup/restore.
- [ ] Integer money arithmetic and currency isolation.
- [ ] Transfers excluded from income/expense totals.

## Sheets
- [ ] OAuth only after explicit intent.
- [ ] Scope and fields explained; spreadsheet chosen; first transfer confirmed.
- [ ] Outbox, idempotency, retries, conflicts, revocation tested.
- [ ] Disconnect retains local DB and remote Sheet.
- [ ] No guarantee of sync when app is closed.

## Localization/accessibility
- [ ] Ten locale files with identical keys and native review.
- [ ] No hardcoded app-owned strings, including charts/Lottie.
- [ ] RTL, mixed scripts, large text, screen readers and contrast.
- [ ] Reduced-motion behavior and static fallbacks.

## Visual/motion
- [ ] SVG assets render correctly and scale.
- [ ] Lottie source/license documented and JSON bundled locally.
- [ ] Animation never gates save/navigation.
- [ ] Off-screen controllers pause/dispose.
- [ ] Profile frame time and memory on low-end Android.
