# PawPal — Complete Screen Matrix and Acceptance

This matrix extends the original screen set. All screens use the Sunny Companion light-only design system.

## Navigation and screens

| Area | Screen | Primary content and actions | Empty/error/edge states |
|---|---|---|---|
| Onboarding | Welcome and setup | Explain local-first value, units, species interests; skip | Returning user, migration failure |
| Home | Dashboard | Pet switcher, today's tasks, quick add/log, seasonal guide | No pets, no tasks, offline |
| My Pets | Pet list | Active/archived profiles, add, restore, sort | Empty, archived only |
| My Pets | Pet profile | Overview, records, care schedule, logs, feeding/activity, contacts | Incomplete profile |
| My Pets | Pet editor | Name/species, optional details, local photo | Invalid date, denied photo picker |
| Care | Reminder agenda | Today/week/month, overdue/upcoming/completed, pet/type filters | No tasks, many overdue |
| Care | Reminder editor | Task, pet, time, recurrence, owner notes | Permission denied, recurrence edge |
| Care | Reminder history | Completed/skipped/snoozed events | No history |
| Care | Care log editor | Weight, grooming, behavior, vet visit, custom | Invalid unit/value |
| Care | Feeding log | Food label, amount/unit, meal type, notes | Missing optional values |
| Care | Activity log | Activity, duration, optional distance | Invalid duration |
| Records | Health-record vault | Vaccination, vet visit, preventive-care records | No records, attachment unavailable |
| Records | Record editor/detail | Owner-entered details, follow-up date, attachment preview | Large file, unsupported file |
| Care | Checklist library | New pet, life stage, grooming, travel templates | No matching species |
| Care | Checklist detail | Check/skip/customize/duplicate/reset | Archived template |
| Contacts | Emergency card | Vet, emergency clinic, caregiver contacts | No contacts, offline |
| Contacts | Resource directory | Verified US resource, source and verified date | Stale resource, unavailable link |
| Sharing | Pet-sitter handoff | Select fields, preview, export/share | Export cancelled, sensitive warning |
| Discover | Discover/search | Topics, species/life-stage filters | No results, offline |
| Content | Article feed/detail | Body, sources, reviewer, safety callout | Withdrawn/stale/missing image |
| Breeds | Breed directory/detail | Filters, descriptors, care guides | Mixed/unknown, no matches |
| Saved | Saved and collections | Favorites, custom collections, history | Empty, removed content |
| Settings | Preferences | Units, quiet hours, dashboard, notification options | Permission revoked |
| Settings | Content updates | Version, last check, manual update | Rate limit, invalid manifest |
| Settings | Storage/privacy | Cache, attachments, local data deletion | Low storage |
| Settings | Backup/restore | Export selection, import preview, conflict resolution | Corrupt/old backup |

## Important screen-level rules
- Emergency resource directory and emergency card have no ad containers.
- Every owner-entered medical record is labelled “Entered by you”; the app does not verify it.
- Reminder screens never suggest a dose, treatment or medically appropriate schedule.
- Feeding and activity screens record only what the owner enters; do not calculate health scores.
- Sitter handoff requires field-by-field preview and explicit share action.
- Attachment export clearly states whether actual file bytes are included.
- Content freshness shows last successful update and does not disguise stale information.

## Global UI states
Loading, empty, offline, stale, error/retry, permission denied, permission revoked, unsupported schema, insufficient storage, unsaved changes, destructive confirmation, and partial export/import failure.

## Acceptance
Every personal-data screen works offline. No screen uploads pet data. All destructive operations preview affected records. Emergency content remains accessible without ads or network when bundled fallback is available. Light appearance is used by every page, sheet, dialog and system-bar configuration controlled by the app.
