# Screen 06 — Transaction Details

## Layout
Formatted amount and type; category; account; date/time; note; merchant; tags; created/updated metadata where useful.

## Actions
Edit, duplicate, delete, and optionally mark as recurring template. If synced, show sync status and last sync; do not expose raw access tokens.

## Behavior
Delete uses confirmation and a recoverable tombstone if the record exists in Google Sheets. Editing a synced record creates a pending update.

## Acceptance
Show original currency. Never show a converted amount without identifying rate/source/date.
