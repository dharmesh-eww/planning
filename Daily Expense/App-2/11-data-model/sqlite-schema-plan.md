# SQLite Schema Plan

Tables: transactions, accounts, categories, budgets, transfers, recurring_rules, savings_goals, sync_metadata, change_log, app_preferences.

Use UUID text primary keys; integer minor-unit amounts; ISO currency codes; ISO dates/timestamps; nullable deleted_at tombstones; revision and sync state. Add indexes for date/category/account/type/updated_at. Enforce foreign keys, migrations and atomic transactions. Store locale/currency/theme/reduced-motion/privacy preferences locally. OAuth tokens remain outside SQLite in secure storage.