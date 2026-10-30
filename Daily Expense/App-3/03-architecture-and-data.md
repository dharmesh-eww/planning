# Architecture and Data

Flutter presentation → Riverpod state/controllers → domain use cases → repositories → SQLite. Google Sheets is a separate optional adapter.

SQLite via sqflite is authoritative. Commit locally first. Core features never require network. Sync consumes a local outbox only after explicit consent.

Entities: Transaction, Account, Category, Budget, Transfer, RecurringRule, SavingsGoal, SyncMetadata, ChangeLog. UUIDs, timestamps, revisions, tombstones, indexes, foreign keys and migrations.

Money is integer minor units plus ISO currency code; no float arithmetic or implicit multi-currency aggregation. Transfers are not income/expense.

Sheets sync uses idempotent UUID upserts, local outbox, conflict snapshots, explicit resolution, bounded retries and manual sync. No server token vault or guaranteed background sync.

OAuth tokens stay in platform secure storage. No financial values or tokens in logs/analytics. Animation is presentation-only and never controls business state.
