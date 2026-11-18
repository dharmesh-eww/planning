# Product Requirements — PawPal

## Vision and outcomes
Help dog and cat owners organize everyday care, keep private records, remember routines and find understandable, trustworthy educational information. Useful without an account or network.

## User jobs
1. Keep multiple pet profiles and care information organized privately.
2. Remember recurring tasks, appointments and owner-entered follow-ups.
3. Record feeding, activity, grooming, training and vet visits.
4. Find safe care, training, breed and life-stage education.
5. Prepare for adoption, travel, grooming and pet-sitter handoff.
6. Keep emergency and veterinary contact details accessible offline.
7. Save guides and export/restore local data manually.

## Functional requirements

### Pet profiles
Create, edit, archive, restore and delete multiple dog/cat profiles. Fields: name, species, breed/mix/unknown, birth date or estimated age, optional sex, weight/unit, local photo path, adoption date, notes and optional vet contact. Unknown/approximate values allowed. Do not require microchip number, diagnosis, allergy or condition fields. If an owner chooses to record sensitive information in free text, explain it remains local and should be minimized.

### Reminders and calendar
User-defined one-time/repeating feeding, water, walk, litter/yard cleanup, grooming, nail trim, dental routine, training, appointment, vaccination follow-up, medication (owner-entered from vet instructions only) and custom tasks. Repeat: daily, selected weekdays, weekly, monthly, interval and one-time. Support complete, undo, snooze, skip, pause, reschedule, edit, delete and history. Snooze must not change the recurrence rule. Calendar agenda supports week/month, pet/type filters and overdue history. Permission denial leaves in-app schedule usable.

### Care records
Local vaccination, vet visit and preventive-care records with owner-entered title, date, follow-up date, clinic, notes and optional attachments. Clearly label as owner-entered, not verified. No vaccine recommendation or due-date inference.

### Feeding and activity
Log food label, amount/unit, meal type and note; walks/play/training/enrichment duration and optional distance. Show history and simple descriptive summaries only. Never calculate diet plans, calories, ideal weight, activity prescriptions or medical scores.

### Care logs
Weight, feeding note, activity, grooming, training, behavior observation, vet visit, medication administered (owner-recorded) and custom entries. Optional local attachments with storage limits. Charts are descriptive and never diagnose.

### Checklists and handoff
Editable checklists for new-pet setup, puppy/kitten basics, adoption transition, life-stage home review, grooming prep and travel prep. Optional pet-sitter handoff sheet includes only owner-selected fields after preview; no automatic sharing or live caregiver sync.

### Emergency contacts and resources
Owner-entered vet, emergency clinic and caregiver contacts. Curated US animal emergency/poison-control resource directory with source and verification date. Offline fallback for key safety guidance. No symptom checker, automatic location lookup or medical triage. Emergency content is never ad-gated.

### Educational content and breed library
Articles, positive-reinforcement training lessons, FAQs, breed profiles, life-stage guides, enrichment, travel and seasonal safety. Content includes species, tags, reviewer/source metadata, review date, safety tier, update date and related content. Breed descriptions are tendencies, not guarantees.

### Discover, saved and sharing
Search cached title, summary, body, tags, breed and species. Filters: dog/cat, life stage, topic, reading time and content type. Favorites, collections, reading history. Share public editorial content only by default.

### Data portability
Versioned JSON export/import. Preview selected records; optionally include attachments in a documented archive. Import validates schema, size, IDs, references and attachment paths; supports merge/replace and conflict handling; creates a pre-import backup; performs transactional restore. Never trust filesystem paths from backup files.

## Non-functional requirements
Local-first startup; offline pet records/reminders; bounded content and image cache; database migrations; atomic remote content updates; safe attachment cleanup; accessible text scaling/TalkBack/contrast/reduced motion; locale-aware dates and unit conversion; no personal data in network requests, logs, analytics or ad targeting.

## US defaults
en-US, lb, in, °F, mi and US date conventions. Metric units configurable. Store values with explicit units.

## Monetization
Native/banner ads only on non-critical browse surfaces. Interstitial disabled in MVP. No ads in emergency guidance, vet contacts, records, reminders, medication, profile forms, care logs, sitter handoff or backup/import. No sensitive local-data targeting.

## Explicit exclusions
Diagnosis, symptom checker, treatment planner, dosage calculator, medicine advice, vet marketplace, telehealth, social network, public uploads, live lost-pet network, location tracking, payments, accounts, server, Firebase and cloud sync.
