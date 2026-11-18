# Architecture and Data Strategy

## Architecture
Flutter presentation → Riverpod providers/controllers → domain services → repositories → local Drift/SQLite + read-only remote content cache.

## Suggested packages
Riverpod; Drift; Dio or http; Freezed/json_serializable; cached_network_image or controlled image cache; flutter_local_notifications + timezone; share_plus; file_picker; google_mobile_ads; user-messaging-platform. Use intl/timezone packages for dates and local display.

## Source of truth
Local SQLite is authoritative for personal preferences, birth date, journal, favorites, history and reminders. GitHub provides public read-only editorial datasets. No backend, Firebase, account, authentication, cloud database, or cloud sync. Never send birth data, journal text or user identifiers to GitHub.

## Local entities
- UserProfile: id, selected_sign_id, birth_date nullable, date_precision, locale, created_at, updated_at.
- ReadingPreference: categories_enabled, reminder_time, quiet_hours, preferred_period, content_locale.
- JournalEntry: id, entry_date, sign_id, prompt_id nullable, body, mood_label nullable, tags, created_at, updated_at.
- Favorite: id, content_type, content_id, created_at.
- ReadingHistory: content_id, viewed_at, completion_state.
- Reminder: id, type, local_time, weekdays, timezone_id, enabled, next_fire_at.
- ContentCache: content_id, content_type, version, downloaded_at, stale_at.
- ManifestState: manifest_version, etag, last_checked_at, last_success_at.
- BackupMetadata: schema_version, exported_at, app_version.

## Remote entities
ZodiacSign, Horoscope, CompatibilityArticle, LunarEvent, LearningArticle, DailyPrompt, ShareCardTemplate, AssetMetadata, ContentManifest. Stable IDs, schema versions, date ranges, content period and publication state required.

## GitHub fetch policy
- Small manifest check at most once per configured interval (default 24h) or user-triggered.
- Fetch only changed files; use ETag/If-None-Match where supported.
- Split readings by date/period and sign so the app fetches only needed packs.
- Bound JSON size and total download; cache locally.
- Validate schema, date coverage and checksum before atomic update.
- Bounded exponential backoff; no polling or tight retry loops.
- Offline/rate-limit: serve cached readings and show last update.
- GET only; no writes, user data, journal or birth details.

## Date and timezone correctness
Store event timestamps in UTC and retain the source timezone basis. Daily horoscope content uses explicit date keys and a documented editorial timezone policy (recommended America/New_York for US editorial publication) while the UI displays the user's local date and clearly handles when a new reading becomes available. Avoid silently showing tomorrow's reading due to UTC conversion. Lunar event times convert from UTC to device local time and retain source metadata.

## Zodiac calculation boundary
MVP sun sign selection uses common date ranges as a convenience only. For cusp dates, prompt manual choice and disclose ambiguity. Do not calculate ascendant, houses, planetary positions or natal charts. A future chart engine would require a validated ephemeris, precise birth time/location, privacy review and separate product scope.

## Database integrity
Stable UUIDs, indexes for date/sign/content type, versioned migrations and transactional imports. Deleting journal entries is permanent after confirmation; export is user-controlled.
