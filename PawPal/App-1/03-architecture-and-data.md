# Architecture and Data Strategy

## Architecture
Flutter presentation → Riverpod providers/controllers → domain services/use cases → repository interfaces → local SQLite and read-only content cache.

Recommended packages:
- Riverpod for state and dependency injection.
- Drift over SQLite for typed queries and migrations.
- Dio or http for bounded GitHub JSON requests.
- Freezed + json_serializable for immutable remote models.
- cached_network_image or a controlled image cache.
- flutter_local_notifications + timezone for local reminders.
- image_picker for local pet photos.
- file_picker/share_plus for backup and sharing.
- google_mobile_ads and user-messaging-platform for consent-aware advertising.
- connectivity_plus may inform UX but must not be treated as proof of internet availability.

## Data ownership
SQLite is authoritative for personal data. GitHub is an optional public read-only source for editorial content. Never send local pet profiles, reminder contents, logs, notes, preferences, or identifiers to GitHub. No account, backend, Firebase, cloud database, or cloud sync.

## Local entities
- Pet: id, name, species, breed_id nullable, custom_breed, birth_date nullable, age_is_estimated, sex nullable, weight_value nullable, weight_unit, photo_local_path, adoption_date, notes, vet_name, vet_phone, created_at, updated_at, archived_at.
- Reminder: id, pet_id, title, category, schedule_rule, next_fire_at, timezone_id, notification_enabled, active, owner_entered_instructions, created_at, updated_at.
- CareLog: id, pet_id, event_type, event_at, value nullable, unit nullable, note, attachment_paths, created_at.
- Favorite: id, content_type, content_id, created_at.
- Collection and CollectionItem: local named groups of content IDs.
- ReadingHistory: content_id, last_opened_at, progress_position.
- UserPreference: locale, weight_unit, temperature_unit, distance_unit, notification settings, content version.
- ContentCache: content_id, content_type, schema_version, content_version, downloaded_at, stale_at.
- ContentManifestState: manifest_version, etag, last_checked_at, last_success_at.
- BackupMetadata: schema_version, export timestamp, app version.

## Remote content entities
Category, Article, Breed, TrainingProgram, TrainingLesson, SafetyResource, FAQ, RelatedContent, AssetMetadata, ContentManifest. Every record uses a stable string ID and explicit schema version.

## GitHub fetch policy
- Fetch a small manifest on app launch only when cache age exceeds the configured check interval (for example 24 hours), or when the user taps Check for updates.
- Download only changed content files and only after validating the manifest.
- Use ETag/If-None-Match where supported; respect 304 responses and cache headers.
- Keep a conservative request budget; do not poll, loop, or repeatedly retry.
- Limit individual JSON file size and total content pack size; paginate large catalogs by category or content pack.
- Cache validated JSON locally. Update content atomically only after schema and integrity checks pass.
- Use bounded retries with exponential backoff and jitter; never retry continuously.
- If GitHub is unavailable, show cached content and last successful update.
- Remote data is read-only; there are no write requests.

## Images
Prefer optimized WebP/AVIF/JPEG assets with explicit dimensions, attribution, and licensing. Lazy-load images, cache with size limits, and show local placeholders. Do not put personal photos in remote content.

## Notifications
Schedule on device. Store timezone-aware recurrence rules. Rebuild schedules after reboot, time-zone change, permission change, or app update. If exact alarm permission is unavailable, use supported inexact scheduling and disclose expected behavior.

## Database integrity
Use stable UUIDs, foreign keys, indexes for pet/date/type and content IDs, transactional writes, and versioned migrations. Deleting a pet must preview dependent reminders/logs and offer archive/export before permanent removal.
