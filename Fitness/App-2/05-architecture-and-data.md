# Architecture and Data — PULSE

Flutter + Riverpod + feature-first Clean Architecture. SQLite remains authoritative. Bundled content guarantees offline use. GitHub is optional read-only public content distribution.

Packages: sqflite, path, flutter_riverpod, freezed, json_serializable, go_router, fl_chart, flutter_local_notifications, shared_preferences, intl, uuid, file_picker, share_plus, csv, lottie.

Tables: exercise, program, program_week, program_session, program_exercise, workout_session, session_exercise, exercise_set, body_measurement, goal, reminder, app_setting, content_pack. UUID keys; foreign keys; indexed timestamps. Persist units with values. Store weights in scaled integer units and preserve unit context.

Workout session records are immutable snapshots of what was performed; editing a program never rewrites history. Save set entries transactionally and persist active session plus timer deadline. Recompute countdown on resume.

Backup is versioned JSON/CSV. Validate schema, IDs, relationships, size and version before import. Explain merge/replace and confirm. GitHub packs use manifest, schema version, checksum and changelog; stage and validate before applying, preserve last-known-good cache.

No remote user profile, analytics, account or sync. Export files may contain sensitive fitness information; make the destination and risks clear.
