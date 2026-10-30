# Google Sheets Workbook Template

The app may create a workbook with these tabs. Stable machine column IDs should be used internally; localized header labels are presentation only.

## Transactions
transaction_id, type, amount_minor, currency_code, currency_exponent, transaction_date, category_id, account_id, note, merchant, tags_json, created_at, updated_at, deleted_at, revision.

## Accounts
account_id, name, account_type, currency_code, opening_balance_minor, archived_at, updated_at.

## Categories
category_id, type, parent_id, default_name_key, custom_name, icon_key, archived_at, updated_at.

## Budgets
budget_id, name, period_type, start_date, end_date, category_id, limit_minor, currency_code, rollover_policy, updated_at.

## Transfers
transfer_id, from_account_id, to_account_id, amount_minor, currency_code, transfer_date, note, updated_at, deleted_at.

## AppMetadata
schema_version, app_export_version, exported_at, device_generated_id, last_sync_revision.

## Important
Do not export OAuth tokens, device secrets, app lock credentials, or unnecessary personal identifiers. Warn the user that anyone with access to their Google Sheet can view its financial contents. Keep headers and IDs stable across app languages.
