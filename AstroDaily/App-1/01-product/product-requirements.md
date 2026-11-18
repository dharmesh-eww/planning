# Product Requirements — AstroDaily

## User jobs
- Read a dated daily horoscope for a selected sign.
- Browse weekly/monthly readings and historical archive.
- Explore traditional zodiac sign characteristics.
- Compare two signs through reflective compatibility content.
- View sourced lunar events and educational material.
- Save/share readings, create private journal entries and receive optional reminders.
- Use cached content offline without an account.

## Sign and birth-date behavior
Support all 12 Western tropical sun signs. Users may select a sign manually or enter month/day; full birth date is optional and local-only. Common date ranges are approximate. For cusp dates, explain ambiguity and allow manual override. No birth time or birthplace is required for basic content. Do not infer ascendant or natal chart.

## Horoscope content and archive
Daily, weekly and monthly readings. Categories: general, love/relationships, career/work, wellbeing/reflection. Every reading has stable ID, sign, period type, explicit start/end, editorial timezone, category, title/body, prompt, publication/update timestamps, locale, disclaimer, status and version. Archive navigation only shows published dates and clearly labels missing, stale, withdrawn or expired content. Never relabel an old reading as today's.

## Reading experience and personalization
Daily theme, optional concise/expanded versions, category preferences, text-size/line-spacing controls, mark-as-read, favorites and prompts. Personalization is local to selected sign and categories. Reading streak is optional, disableable and non-punitive. Weekly recap summarizes local reading/journal activity without interpreting mood or mental health.

## Compatibility
Any pair, including same sign. Explain traditional element/modality themes, strengths, possible friction and conversation prompts. No numeric compatibility score, destiny labels or deterministic relationship claims.

## Lunar calendar and learning
Precomputed new moon, first quarter, full moon and last quarter events with UTC timestamp, source timezone, source, dataset version and verification date. Convert to device-local time. Learning library explains signs, elements, modalities, symbols, planets, zodiac history, chart vocabulary, retrogrades and misconceptions. Retrograde dates only appear when sourced/precomputed and reviewed. No simplistic client-side astronomy calculations.

## Journal and privacy
Private local journal with date, prompt, free text, optional mood label and tags. Create/edit/search/delete/export. Never share by default; share preview explicitly excludes journal text unless user chooses it. No cloud analysis or sync.

## Share cards
Generate cards locally from public reading content, sign, date, brand and disclaimer. Provide light templates, preview and platform share sheet. Never include journal entries by default.

## Notifications
Local daily, weekly and optional lunar/favorite-sign reminders. User controls time, weekdays, quiet hours and per-type toggles. Permission denial does not block content. Notification text must not expose journal or birth data and must not use alarming predictions.

## Search, saved and calendar
Search cached readings, signs, learning articles and compatibility content. Save favorites and reading history. Calendar/archive supports date navigation and explicit available-content indicators.

## Data portability
Versioned JSON export/import for profile/preferences, journal, favorites, reminders and history. Preview, validate, merge/replace, resolve duplicate IDs and create pre-import backup. No automatic cloud backup.

## Non-functional requirements
Offline-first startup; bundled sign metadata; bounded remote packs; strict manifest/JSON/schema/checksum validation; atomic cache replacement; locale/timezone correctness; database migrations; accessibility; no personal data in network traffic, logs, analytics or ad SDKs.

## Explicit exclusions
Guaranteed predictions, psychic services, astrologer chat, public social features, birth-chart/ascendant calculation in MVP, planetary position computation, financial/investment/medical/legal advice, exact event prediction, user-generated public content, account, backend, Firebase and cloud sync.
