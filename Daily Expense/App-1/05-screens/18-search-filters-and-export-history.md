# Screen 18 — Advanced Search and Export History

## Search
Search transactions by note, merchant, category, amount range, account, and date. Filters combine predictably and can be reset individually or all at once.

## Export history
Show local export file name, date, format, record count, and completion/error status. Do not retain exported copies inside app storage unless user explicitly chooses.

## Behavior
Exports use a stable documented schema and include currency codes, IDs, dates, and type. Import validates schema, duplicate IDs, and currency precision before writing. Preview additions/updates/skips before confirmation.

## Acceptance
Never silently replace local records. Keep export and import entirely user-initiated.
