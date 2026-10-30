# Screen 15 — Data Backup and Google Sheets

## Sections
- Local export: CSV and app backup.
- Local restore: validate and preview before merge/replace.
- Google Sheets: connect/disconnect, selected spreadsheet, sync mode, last sync, pending changes, errors.
- Privacy explanation and permission details.

## Google connection
Show a clear explanation before OAuth: which spreadsheet/file is accessed, what fields are written, that the app does not operate a server, and that local data remains primary. User must explicitly select or create a spreadsheet and confirm first export.

## Sync controls
Manual sync, optional automatic sync while app is active/online, pause, retry, resolve conflicts, change spreadsheet, disconnect. No sync until user opts in.

## Acceptance
No broad Drive permission by default. Do not store tokens in SQLite. Disconnect does not delete local records or the user's spreadsheet.
