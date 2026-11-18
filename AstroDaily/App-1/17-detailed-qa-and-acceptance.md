# AstroDaily — Detailed QA and Acceptance Matrix

## Sign selection
Test all 12 signs, no birth date, month/day only, full birth date, cusp dates, manual override, invalid date, leap day and profile reset. Confirm birth data never appears in network traffic or logs.

## Reading experience
Test all categories, reading length preference, date navigation, previous/next day, weekly/monthly boundaries, archives, mark-as-read, favorite, share-card rendering, text scaling, missing date, late publication, stale cache, withdrawn content and archive retention cutoff.

## Content coverage and publishing
Test exactly 12 signs per published category/date, duplicate IDs, missing sign/category, empty body, invalid period, wrong timezone, future published_at, unapproved disclaimer, malformed source metadata, invalid checksum and asset reference. Ensure placeholder hashes cannot pass production validation.

## Calendar and lunar data
Test month/year boundaries, leap year, event ordering, UTC conversion, device timezone travel, DST, source timezone disclosure, missing source and stale verification date. Never calculate moon phase using a rough client-side formula.

## Notifications
Test daily and weekly schedules, selected weekdays, quiet hours across midnight, DST, timezone change, permission denial/revocation, disable all, app update, reboot and duplicate schedule prevention.

## Journal and export
Test create/edit/delete/search, large text, Unicode/emoji, tags, local lock if enabled, delete all, export preview, import validation, merge/replace, duplicate IDs, corrupt file, low storage and rollback. Confirm journal text excluded from share and ad/analytics data.

## Remote content and offline
Test first launch without network, bundled sign metadata, no daily file, rate limit, 304, wrong host, oversized pack, malformed JSON, checksum mismatch, unsupported schema, stale content, withdrawn content, archive expiry and rollback. Cached readings and journal remain accessible.

## Ads, accessibility and release
Ads never interrupt reading or private flows; consent and regional behavior verified; no personal targeting. Verify light-only surfaces, contrast, TalkBack, full sign labels, text scaling, keyboard, reduced motion and screen sizes. Release requires disclaimer, privacy policy, content sources, asset licenses, UMP/AdMob disclosure, store data-safety accuracy, offline verification and a content publishing checklist.
