# Architecture and Data Strategy

Flutter UI → Riverpod controllers/providers → domain use cases → repositories → SQLite. Google Sheets is a separate optional adapter.

SQLite via sqflite is authoritative. All writes commit locally first; core screens never require network. Sync reads a local outbox only after consent and authorization.

Entities: Transaction, Account, Category, Budget, Transfer, RecurringRule, SavingsGoal, SyncMetadata, ChangeLog. Use UUIDs, UTC timestamps plus intended local transaction date, revisions, tombstones, migrations and indexes.

Money: integer minor units + ISO currency; respect currency exponent. Never use floating point or sum unlike currencies without explicit conversion. Transfers are not income/expense.

Google Sheets: idempotent UUID upserts, local outbox, conflict snapshots, explicit conflict resolution, retry/backoff, manual sync. No server-side token vault or guarantee of background sync.

OAuth tokens only in platform secure storage. Exclude tokens and finance values from logs/analytics. Animation widgets are presentation-only; animation completion never controls business state. Lazy-load charts/Lottie and pause off-screen.
