# Product Requirements

## Vision and outcomes
Help pet owners confidently manage everyday routines and find understandable, trustworthy educational information. The app should be useful even if the device is offline and should not require account creation.

## User jobs
1. Keep information about each pet in one private local profile.
2. Remember recurring care tasks and appointments.
3. Learn practical, safe care and training techniques.
4. Find guidance by topic, pet type, breed, life stage, and keyword.
5. Record simple care activities and review history.
6. Save useful guides for quick access.
7. Export or restore personal app data manually.

## Functional requirements

### Pet profiles
- Create, edit, archive, restore, and delete multiple pets.
- Species: dog or cat for initial release; schema supports future species without promising content.
- Store name, species, breed/mix, birth date or estimated age, sex (optional), weight and unit, photo path, adoption date, notes, and optional vet contact.
- Allow unknown values and approximate dates; do not force sensitive or unnecessary fields.
- Pet profile is local and never uploaded to content hosting or advertising systems.

### Care routines and reminders
- User-defined one-time and repeating reminders: feeding, water refresh, walk, litter/yard cleanup, grooming, nail trim, dental care, training, appointment, vaccination follow-up, and custom task.
- Owner enters the schedule and any medication details from veterinary instructions.
- Repeat rules: daily, selected weekdays, weekly, monthly, interval, and one-time.
- Snooze, complete, skip, reschedule, pause, and edit.
- Notification permission denial must not block app usage; show in-app task list.
- Handle time-zone changes, daylight-saving transitions, reboot/rescheduling, and notification limits.

### Care logs
- Add dated entries for weight, feeding note, walk/activity, grooming, training, behavior observation, vet visit, and custom note.
- Optional attachment references remain local; set storage limits and allow deletion.
- Timeline filters by pet, event type, and date.
- Weight chart uses selected unit and clearly labels entries; never infer a diagnosis from trends.

### Educational content
- Article categories: getting started, preventive care awareness, nutrition basics, grooming, dental hygiene, behavior, training, exercise/enrichment, travel, seasonal safety, senior care, and adoption.
- Each article includes species applicability, life-stage tags, review metadata, update date, safety note, sources/reviewer fields where appropriate, and related content.
- Safety-sensitive pages use prominent professional-care guidance.
- Search and filters work on downloaded content.

### Breed library
- Breed cards and details with temperament descriptors, size range, grooming needs, exercise tendencies, coat type, common care considerations, and suitability caveats.
- Breed descriptions must avoid deterministic claims and stereotypes.
- Mixed-breed pets can select “Mixed / Unknown”.

### Saved and discovery
- Favorite articles and breeds; custom collections; recent history.
- Search title, summary, body, tags, breed, and species.
- Filters for dog/cat, life stage, topic, reading time, and content type.
- Share a public article link or plain-text summary; never include private pet data by default.

### Data portability
- Export pet profiles, reminders, logs, and preferences to a versioned JSON backup file.
- Import with schema validation, preview, duplicate handling, and merge/replace choice.
- Provide a backup-before-replace reminder.
- Do not promise automatic cloud backup or cross-device synchronization.

## Non-functional requirements
- Home and local pet records load without network.
- Graceful loading, offline, stale-cache, empty, parse-error, and retry states.
- Database migrations preserve user-created data.
- Efficient image caching and bounded storage.
- Accessible touch targets, text scaling, TalkBack semantics, contrast, and reduced motion.
- All dates, weights, heights, and temperatures are formatted using locale-aware utilities.

## US defaults
- English (US), Fahrenheit, pounds/inches, miles, and US date conventions by default.
- Offer metric units in settings.
- Do not hard-code assumptions into stored values; persist units explicitly.

## Monetization requirements
- AdMob banner/native placements only in non-critical content areas.
- Interstitial frequency cap and natural transition rules.
- No ads on emergency/safety articles, pet profile forms, reminders, logs, or data export/import.
- No targeting based on pet health notes, allergies, medication details, or other private local records.

## Explicit exclusions
No diagnosis, symptom checker, treatment planner, medicine dosage calculator, prescription reminders prefilled with medical advice, veterinarian booking marketplace, telehealth, social network, user-uploaded public content, location tracking, lost-pet live network, payments, or developer-operated server.
