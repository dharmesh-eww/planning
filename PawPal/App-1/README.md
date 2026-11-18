# PawPal — App-1: Complete Product Plan

## Product concept
**PawPal** is a practical pet-care companion for US dog and cat owners. It combines local pet profiles, care schedules, health-record organization, feeding/activity logs, breed and training education, checklists, emergency contacts and optional pet-sitter handoff. It is an educational organizer, not veterinary diagnosis or telemedicine.

## Product promise
Keep everyday pet-care information and routines organized in one private, reliable place—even when offline.

## Target audience
- US dog and cat owners, prospective adopters and first-time pet parents.
- Multi-pet households and families using a shared device (not cloud collaboration).
- Initial locale: en-US; US customary units by default, metric equivalents available.

## Hard constraints
- Flutter Android-first app.
- No custom backend/server, Firebase, mandatory account, remote database, cloud sync, chat, social feed or public user-generated content.
- Public GitHub repository supplies a limited, read-only catalog of editorial content and metadata.
- Pet profiles, records, reminders, logs, favorites, journal-style notes and preferences stay on-device.
- GitHub content is cached and validated locally; local utility features work without network.
- No personal pet/owner data is sent to GitHub or ad targeting.
- Light appearance only: no dark theme, dark palette, theme switch or theme preference.
- No diagnosis, treatment recommendations, medicine dosage, symptom checker or emergency triage.

## Main navigation
Home · Discover · My Pets · Saved · Settings.

## Complete functionality
1. Multiple local dog/cat profiles, optional photos, breed/mix/unknown, age/date, weight and notes.
2. Home dashboard with pet switcher, today/overdue/upcoming tasks, quick actions and weekly recorded-activity summary.
3. User-defined reminders for feeding, water, walks, grooming, dental routine, training, appointments, vaccination follow-up, medication (owner-entered only) and custom tasks.
4. Care logs for weight, feeding, activity, grooming, training, behavior observations, vet visits and owner-recorded medication administration.
5. Private record organizer for vaccination, vet visits and preventive-care records, with optional local attachments.
6. Feeding and activity journals; no diet prescriptions, calorie targets or health scoring.
7. Reusable new-pet, life-stage, grooming, travel and home-preparation checklists.
8. Vet, emergency and caregiver contact cards; curated, verified US emergency resource directory.
9. Optional pet-sitter handoff sheet with explicit field selection, preview and user-controlled export.
10. Breed library, positive-reinforcement training lessons, care guides, search, filters, saved items, collections and reading history.
11. Calendar agenda, local notifications, quiet hours, offline cache and manual content updates.
12. Versioned export/import with validation, preview, merge/replace, attachment handling and recovery backup.

## Architecture and data ownership
Flutter + Riverpod + repository pattern. Drift/SQLite is the source of truth for personal data. A bounded local cache stores validated public GitHub JSON and licensed editorial assets. Notifications are local. No account is required. Never upload pet information.

## Content and safety
Veterinary claims require qualified veterinary review. Urgent safety resources must be verified, dated, available without ads and direct users to a veterinarian/emergency service. The app does not diagnose, prescribe, calculate medication doses or infer health risk.

## Monetization
Consent-aware AdMob on non-critical discovery/editorial surfaces only. No ads in emergency content, vet contacts, records, medication/reminder creation, profile editing, care logs, sitter export or backup/restore. Rewarded ads never gate essential care information.

## Appearance
Premium warm light-only design. See `02-design/`. No dark-mode tokens, dark assets or theme controls.

## Detailed plan index
- `01-product/product-requirements.md` — product scope and constraints.
- `02-design/` — visual and motion system.
- `03-architecture-and-data.md`, `15-data-model-and-local-workflows.md` — architecture, local entities, backup and sync boundaries.
- `04-navigation-and-interaction.md`, `05-flows/`, `05-screens/`, `18-screen-matrix-and-acceptance.md` — navigation, journeys and complete screen behavior.
- `06-data/`, `16-content-operations-and-safety.md` — GitHub JSON, editorial lifecycle and safety.
- `07-privacy-and-security.md`, `08-monetization-and-ads.md` — privacy and advertising.
- `09-accessibility-localization.md`, `10-assets-and-content.md` — inclusive UX and content.
- `14-feature-expansion.md` — additional product features.
- `17-detailed-qa-and-acceptance.md`, `11-testing-and-release.md` — QA and release gates.
- `12-ui-reference-prompts.md`, `13-roadmap-and-acceptance.md` — UI direction and delivery stages.

## Definition of done
All screens, data contracts, local workflows, edge cases, offline/update behavior, safety reviews, privacy, light-only appearance, ad placements, accessibility and release gates are specified. Core personal features work offline and no personal data leaves the device.
