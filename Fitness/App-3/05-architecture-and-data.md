# Architecture and Data — GROVE

Flutter + Riverpod + Clean Architecture. SQLite is the source of truth; bundled starter movement library guarantees offline access. No remote account or sync.

Packages: sqflite, path, flutter_riverpod, freezed, json_serializable, go_router, fl_chart, flutter_local_notifications, shared_preferences, intl, uuid, file_picker, share_plus, csv and lottie.

Tables: movement, routine, routine_day, routine_movement, activity_session, session_movement, activity_set, reflection, goal, measurement, reminder, app_setting and content_pack. UUID IDs, foreign keys, indexes and explicit units. Preserve historical session snapshots when routines are edited.

Persist active session and timer deadline; save each entry immediately; restore safely after process death. Store numeric measurements with scale/unit and avoid floating point for quantities requiring exactness.

Backup uses versioned JSON/CSV with schema validation, record preview and explicit merge/replace behavior. GitHub public content packs include manifest, schema version, checksum and changelog; download only on user request, validate and atomically apply, retain last-known-good version.

No personal information leaves device through app infrastructure. Exports can contain sensitive notes and measurements; explain before sharing.
