# SQLite Schema Plan

## Tables
- transactions
- accounts
- categories
- budgets
- transfers
- recurring_rules
- savings_goals
- sync_connections
- sync_outbox
- sync_conflicts
- app_preferences
- schema_migrations

## Key constraints
- UUID primary keys.
- Foreign keys enabled.
- amount_minor integer and currency_code text required.
- Transaction type constrained to income/expense.
- Transfers stored separately.
- Index transactions(transaction_date), transactions(category_id), transactions(account_id), transactions(updated_at).
- Use soft delete for synced entities.
- Use a transaction for operations that update multiple rows or tables.

## Migration policy
Increment schema version. Test upgrade from every supported released version. Back up before destructive changes. Never silently drop or reset user records. Validate row counts and foreign keys after migration.

## Money storage
Use integer minor units and currency exponent metadata. Do not assume all currencies have two decimal places. Use safe integer ranges and validate overflow.
