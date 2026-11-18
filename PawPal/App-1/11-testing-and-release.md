# Testing and Release Checklist

## Functional
Test multiple pet CRUD/archive/restore; pet switching; reminders across recurrence, reboot, DST, timezone, app update and permission revocation; care logs and unit conversions; favorites surviving content refresh; export/import merge/replace; search and filters.

## Remote content
Test fresh/unchanged manifest, ETag/304, offline, rate limit, malformed JSON, checksum mismatch, oversized file, missing pack, unsupported schema, minimum app version and atomic rollback. No personal data in request URL/headers/logs.

## Safety and privacy
Verify reviewer metadata for health claims; no diagnosis/dosage/treatment; emergency pages have no ads; medication reminders show owner-entered instructions only; local data absent from analytics/crash logs/ad targeting; permissions contextual.

## Accessibility and UI
Light appearance on every screen/overlay; text scaling, TalkBack, contrast, focus, 48dp targets, reduced motion; small phones/tablets, keyboard and insets. No dark palette, assets or settings.

## Release
Privacy policy, educational disclaimer, reviewer/source records, asset licenses, store listing, AdMob/UMP, app-ads.txt where applicable, Android permission/target compliance, migration tests, offline launch, restore test, support route.
