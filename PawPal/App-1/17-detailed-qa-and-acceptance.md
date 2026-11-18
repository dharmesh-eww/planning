# PawPal — Detailed QA and Acceptance Matrix

## Pet profiles
Test one/many pets, unknown breed, mixed breed, estimated age, leap-day birthday, invalid/future dates, missing photo, permission denied, photo removed externally, archive/restore, permanent delete and dependent-data preview.

## Records and logs
Test vaccination and vet records with/without attachments, duplicate dates, future follow-up date, missing clinic, attachment deletion, feeding quantities and units, activity duration/distance, timeline sorting and filters. Confirm no medical interpretation or health score.

## Reminders
Test every recurrence, monthly 29th/30th/31st behavior, DST gap/overlap, timezone travel, reboot, app upgrade, permission denied/revoked, notification limit, snooze, skip, pause, completion, undo and overdue backlog.

## Checklists and sitter export
Test checklist duplicate/reset/custom items; sitter sheet field selection, preview, attachment handling, file export cancellation, sensitive-field warning and share target failure. Confirm no automatic sharing.

## Emergency resource behavior
Test offline fallback, stale verification date, unavailable URL, phone formatting, regional caveat, no ad placement and clear “contact a veterinarian” language.

## Backup/import
Test old/new schema, oversized file, malformed JSON, deep nesting, duplicate IDs, orphan references, unsafe attachment paths, partial attachment failure, merge conflicts, replace rollback, low storage and interrupted import.

## Remote content
Test offline first launch, manifest 304, rate limit, wrong host, path traversal, unexpected redirect, invalid checksum, oversized file, unsupported schema, minimum app version, missing asset and rollback. Confirm no personal data in network requests.

## Privacy, ads and accessibility
Verify no personal pet data in logs, analytics or ad targeting; contextual permissions; all app-owned surfaces light-only; TalkBack, text scaling, contrast, keyboard, reduced motion, touch targets and small/large screens. Ads never appear in emergency or medication flows.

## Release gate
No critical safety/privacy defects; all safety content has appropriate review; local data migration and restore verified; emergency fallback available; privacy policy, asset licenses, UMP/AdMob disclosures, store data-safety answers and support contact ready.
