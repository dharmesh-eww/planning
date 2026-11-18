# Testing and Release Checklist

## Product behavior
Test all 12 signs; manual sign override; optional birth date; cusp boundary dates; same-sign and mixed-sign compatibility; daily/weekly/monthly period boundaries; missing/future readings; save/share; journal CRUD; local reminders; export/import.

## Date/time correctness
Test America/New_York editorial day boundary, device timezone ahead/behind, travel, DST start/end, leap day, year/week/month rollover, UTC-to-local lunar event conversion, and reminder wall-clock stability.

## Remote content
Test fresh/unchanged manifest, ETag/304, offline, rate limit, malformed JSON, checksum mismatch, oversized file, missing date pack, unsupported schema, withdrawn reading and atomic rollback. Never expose birth date or journal text in requests/logs.

## Trust and safety
Disclaimer visible in onboarding/settings/reading detail. No guaranteed predictions or medical/financial/legal advice. Compatibility has no deterministic score. Journal excluded from sharing by default. Lunar source and timezone metadata available.

## Privacy and ads
No account/backend/Firebase/cloud sync; local personal data absent from ad targeting and analytics; contextual notification permission; ads excluded from journal, onboarding, export/import and disclaimer.

## Accessibility and release
Light appearance on every screen and overlay; scalable text, TalkBack, contrast, focus, touch targets, reduced motion; Android target/API and notification compliance; privacy policy, terms/disclaimer, content attribution, UMP/AdMob, test ad IDs, app-ads.txt where applicable, store listing and offline launch verification.
