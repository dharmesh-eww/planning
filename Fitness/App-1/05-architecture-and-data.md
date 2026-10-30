# Architecture and Local Data

## Layers
Flutter UI → Riverpod application/use cases → domain models/repositories → SQLite and bundled asset data sources. SQLite is authoritative for personal data.

## Packages
sqflite, path, flutter_riverpod, freezed_annotation, json_annotation, go_router, fl_chart, flutter_local_notifications, shared_preferences, intl, uuid, file_picker, share_plus, csv and lottie.

## Tables
exercise; workout_plan; plan_day; plan_exercise; workout_session; session_exercise; exercise_set; body_measurement; fitness_goal; reminder; app_setting; content_pack. Use UUID text IDs, foreign keys and indexes. Store explicit units and timestamps consistently. Use scaled integers for loads/measurements where practical, not binary floating point.

## Integrity
Versioned migrations, foreign keys, transaction boundaries for finishing/importing, archive plans referenced by history, and snapshot plan details into sessions so plan edits do not rewrite history.

## Session reliability
Persist active session and timer deadline. On resume calculate remaining time from timestamp, not a stale in-memory countdown. Save every set immediately. Offer Resume/Finish/Discard after interruption.

## Backup
Versioned JSON with schema_version and exported_at. Validate size, schema, IDs, references and version before import. Confirm merge/replace; never silently overwrite.

## GitHub content
Read-only public exercise/plan JSON and images with manifest, schema/content version, checksum and changelog. Download only on user request; stage, validate and atomically apply; retain last-known-good pack. Never send personal data or analytics.

## Privacy
No account, server, cloud sync or remote telemetry by default. Explain platform backup behavior accurately. Provide local export and deletion.
