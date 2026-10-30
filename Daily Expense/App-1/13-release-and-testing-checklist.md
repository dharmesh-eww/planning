# Release and Testing Checklist

## Financial correctness
- Integer minor-unit storage and currency exponent tests.
- No cross-currency totals without explicit conversion.
- Transfers do not affect income/expense totals.
- Refund and budget rollover rules tested.
- Date boundaries, leap years, month-end recurring rules, and time zones tested.
- Import/export round-trip preserves exact amounts and IDs.

## Local data
- Offline create/edit/delete.
- Database migration from every supported version.
- Interrupted writes and app termination.
- Backup/restore validation.
- Large transaction history performance.

## Google Sheets
- Permission accepted, denied, partially granted, revoked, expired.
- Spreadsheet created, selected, deleted, unshared, and manually edited.
- Network loss during batch write.
- Quota/rate limit and retry.
- Duplicate prevention and idempotency.
- Conflicts and tombstones.
- Disconnect retains local data and leaves remote sheet untouched.
- Tokens absent from logs, SQLite, and exports.

## Localization
- All ten locale resources have identical keys.
- No hardcoded user-facing strings.
- Native review of financial terms.
- RTL, long strings, decimal separators, currency placement, pluralization.
- TalkBack/VoiceOver labels and chart summaries.
- Language switch does not alter stored financial data.

## Privacy and accessibility
- No financial payloads in crash logs or analytics.
- Clear consent before Google transfer.
- Screen reader and large text.
- Contrast and color-independent status.
- Reduced motion.
- App lock claims match actual protection.

## Release readiness
- Privacy policy describes local storage and optional Google Sheets processing.
- OAuth consent screen, scopes, verification requirements, and platform clients reviewed.
- Google branding/permission explanations comply with current policies.
- Test on supported Android/iOS versions and low-storage/offline scenarios.
