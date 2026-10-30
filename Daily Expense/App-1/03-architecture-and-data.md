# Architecture and Data Strategy

## High-level
Flutter UI → Riverpod state/controllers → domain use cases → repositories → SQLite local data source. Optional Google Sheets integration is a separate data-source adapter behind a repository interface.

## Primary data store
SQLite via sqflite is authoritative for app behavior. Every transaction is written locally first. UI reads from local repositories; no network call is required to create, edit, delete, categorize, budget, or report.

## Suggested domain entities
- Transaction: id, type, amount_minor, currency_code, transaction_date, category_id, account_id, note, merchant, created_at, updated_at, deleted_at, sync_status.
- Account: id, name, account_type, currency_code, opening_balance_minor, archived_at.
- Category: id, name_key/custom_name, type, icon_key, parent_id, is_default.
- Budget: id, period_type, start_date, end_date, category_id nullable, limit_minor, currency_code, rollover_policy.
- Transfer: id, from_account_id, to_account_id, amount_minor, currency_code, date, note.
- RecurringRule: id, template fields, frequency, next_occurrence, reminder settings, active.
- SavingsGoal: id, title, target_minor, current_minor, currency_code, target_date.
- SyncMetadata: provider, spreadsheet_id, worksheet_id, schema_version, last_sync_at, cursor/version, status.
- ChangeLog: entity_type, entity_id, operation, changed_at, revision, sync_state.

## IDs and timestamps
Use stable UUIDs generated locally. Store timestamps in UTC and transaction dates with intended local date/time/time-zone context. Keep created_at and updated_at separate. Use soft deletion/tombstones for records that may have been synced.

## Money
Persist integer minor units and ISO 4217 currency code. Currency exponent comes from maintained currency metadata; do not assume every currency has two decimals. Do not convert currencies implicitly.

## Repository behavior
Local repository operations commit to SQLite first. Sync is an explicit background/foreground task that reads a local outbox and writes to Google Sheets when authorized and online.

## Database safety
Use schema versioning and migrations. Use SQLite transactions for multi-table operations. Add indexes for date, category, account, and common filters. Back up before destructive migration where feasible. Never clear user data to recover from migration errors.

## Attachments
Avoid uploading receipt images in App-1. If receipt attachments are added later, store local file references and explain that Google Sheets sync will not automatically upload image files.
