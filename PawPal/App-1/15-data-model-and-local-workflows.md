# PawPal — Expanded Local Data Model and Workflows

## Additional local entities

### PetRecord
id, pet_id, record_type (vaccination, vet_visit, preventive_care, other), title, event_date, follow_up_date nullable, clinic_name nullable, owner_entered_notes, attachment_paths, created_at, updated_at.

### FeedingEntry
id, pet_id, occurred_at, food_label, amount nullable, amount_unit nullable, meal_type, note nullable, created_at.

### ActivityEntry
id, pet_id, activity_type, started_at, duration_minutes nullable, distance nullable, distance_unit nullable, note nullable, created_at.

### ChecklistTemplate
id, title, species, life_stage nullable, category, content_id nullable, sort_order, version.

### ChecklistInstance
id, pet_id nullable, template_id, title_snapshot, created_at, completed_at nullable, archived_at nullable.

### ChecklistItemState
id, checklist_instance_id, item_id, state (todo/done/skipped), note nullable, updated_at.

### ContactCard
id, pet_id nullable, contact_type (vet/emergency/caregiver), display_name, phone, address nullable, opening_hours_note nullable, is_emergency, created_at, updated_at.

### UserPreference additions
dashboard_layout, quiet_hours, default_pet_id nullable, calendar_start_day, backup_reminder_preference nullable, app_lock_enabled only if supported.

## Data relationships and deletion
- Pet deletion must show all dependent profiles, records, feeding/activity logs, checklists, reminders and attachments.
- Archive is the default safe action.
- Permanent deletion must remove local attachment files only after a successful database transaction or use a cleanup queue.
- Never leave orphaned attachment paths or silently delete a shared file referenced by another record.

## Reminder engine requirements
- Store recurrence rule separately from next scheduled timestamp.
- Define behavior for month-end dates (e.g. 31st): offer last day of month or skip months without that date.
- Handle DST gaps/overlaps, timezone travel, device reboot, app upgrade, notification permission revocation and Android notification limits.
- Completion creates a completion event and calculates the next occurrence; undo restores prior state safely.
- Snooze is a one-off override and must not mutate the underlying recurrence.
- Missed reminders should remain visible in an overdue/history section; never generate an unlimited notification backlog.
- Use exact alarms only if justified and permission is available; otherwise use inexact scheduling and explain it.

## Backup format
- Include schema_version, app_version, exported_at, selected sections and record arrays.
- Export attachments as a clearly documented optional archive or omit them with an explicit preview; never silently imply that photo/document bytes are included when only paths are exported.
- Import validates size, JSON depth, types, IDs, references, paths and supported schema before changing data.
- Never accept arbitrary filesystem paths from a backup as trusted paths.
- Import attachments into app-private storage using generated safe filenames.
- Merge conflict choices: keep existing, replace existing, or skip; show counts before commit.
- Create a recoverable pre-import backup; perform database changes transactionally; retain original data on failure.

## Offline startup and update workflow
- Bundle a minimal starter guide pack and emergency information fallback.
- Local database and reminders initialize before any network request.
- GitHub content is optional and cannot block pet profile, reminder or record functionality.
- Validate manifest schema, app compatibility, file allowlist, size limits and checksums before download.
- Use HTTPS allowlisted raw GitHub URLs; reject path traversal, unexpected hosts and redirects outside policy.
- Do not execute content, HTML, scripts or arbitrary remote configuration.
- Replace cached packs atomically; preserve last known good version on failure.
