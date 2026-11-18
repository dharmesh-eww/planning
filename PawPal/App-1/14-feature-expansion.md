# PawPal — Expanded Feature Specification

This document extends App-1 with additional useful, fully local functionality. All features must preserve the light-only appearance and no-backend architecture.

## 1. Pet health-record organizer (record keeping, not medical advice)
Add a private record vault per pet:
- Vaccination record: vaccine name entered by owner, date administered, next appointment date if supplied by vet, clinic, optional document/photo attachment, notes.
- Vet visit record: visit date, clinic, owner-entered reason, veterinarian-provided follow-up notes, attachment.
- Preventive-care record: owner-entered grooming, dental cleaning, flea/tick or other preventive product record, date and vet-supplied follow-up date. Do not recommend a product or interval.
- Allergy/condition information may be entered only as optional owner notes with a clear privacy warning; do not generate advice or use it for advertising.
- Medical document storage remains local, with per-file and total-storage limits, preview, replace, delete and export controls.
- Clearly label every entry as user-entered; do not imply the app verifies records.

## 2. Feeding and nutrition journal
- Record meal time, food brand/name (free text), amount, unit, meal type and optional note.
- Record treats and water observations as optional logs.
- Allow owner-defined meal reminders; never recommend a diet, calorie target, portion size or food for a medical condition.
- Allow a simple history view and user-entered food list. No automatic nutritional scoring.
- Provide an explicit warning that food changes and special diets should be discussed with a veterinarian.

## 3. Activity and enrichment tracker
- Record walks, play, training and enrichment sessions with duration, optional distance, activity type and notes.
- Weekly summaries show recorded activity only; no fitness score or prescriptive target.
- Include reviewed enrichment idea cards by species and life stage. Make activities adaptable and include supervision/safety notes.
- Optional user-defined goals are personal reminders, not health recommendations.

## 4. Care checklists and life-stage journeys
Provide reusable, editable checklists:
- Bringing a new pet home.
- First-week setup.
- Puppy/kitten basics.
- Adult routine review.
- Senior-pet comfort and home adjustments.
- Grooming preparation.
- Travel preparation.
- New adoption transition.
Checklist items can be checked, skipped or customized. Store completion locally and allow reset/duplicate. Avoid medical schedules; vet-specific follow-ups remain owner-entered.

## 5. Vet and emergency information card
- Local vet contact: clinic name, phone, address and opening-hours note entered by owner.
- Optional emergency contact and trusted caregiver contact.
- Emergency information card can be viewed offline and exported/shared by explicit user action.
- Include curated US animal emergency and poison-control resource links in the editorial content repository, with source, verification date and region notes.
- Do not make calls automatically or infer the user's location. Show that phone numbers and service availability must be verified.
- Emergency content must load from bundled fallback text where practical and must never be ad-gated.

## 6. Pet-sitter handoff
Generate a printable/shareable care sheet selected by the owner:
- Pet name/species/photo (optional).
- Feeding instructions and schedule as entered by owner.
- Walk/activity routine.
- Reminder list and next due times.
- Vet and emergency contacts selected by owner.
- Behavioral notes and access instructions are opt-in and clearly sensitive.
- Preview every field before export. Do not share by default. Export is a user-controlled file; explain it may contain private information.
- No remote caregiver accounts, live updates or multi-device sync.

## 7. Calendar and routine overview
- Month/week agenda of local reminders and appointments.
- Filter by pet and task type.
- Optional Android calendar export only after user action; do not request calendar permission if file export is sufficient.
- Distinguish reminders from completed care logs.
- Avoid claiming a missed task means the pet is harmed.

## 8. Home dashboard improvements
- Multi-pet summary with clear selected-pet context.
- Today, overdue and upcoming groups.
- Quick actions: add reminder, log care, add feeding entry, open emergency card.
- Optional compact weekly care summary based only on recorded data.
- User can reorder or hide nonessential dashboard modules; preferences local.

## 9. Household use boundary
The app may support multiple pets and a single-device household handoff mode. It does not support simultaneous users, identity verification, cloud collaboration, or automatic sharing. Add an optional app-lock using device authentication only if implemented through supported Android APIs; never build custom password storage.

## 10. Feature priority
Core release: health-record organizer, feeding/activity logs, checklists, emergency contacts, calendar agenda. Follow-up release: sitter handoff, richer dashboard customization, optional device-auth app lock. Keep all features usable offline after their required content has been cached.
