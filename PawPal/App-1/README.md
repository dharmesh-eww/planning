# PawPal — App-1: Complete Product Plan

## Product concept
**PawPal** is a practical pet-care companion for US dog and cat owners. It combines trusted educational care guides, breed profiles, training guidance, local pet profiles, user-created care schedules, and reminders. It is a personal utility, not a veterinary diagnosis or telemedicine product.

## Product promise
Keep each pet's everyday care information, routines, and learning resources organized in one friendly place.

## Target audience
- Primary: US dog and cat owners and prospective adopters.
- Secondary: first-time pet parents, multi-pet households, and families sharing care responsibilities on one device.
- Initial content locale: English (United States), US customary units and Fahrenheit, with metric equivalents available.

## Hard product constraints
- Flutter Android-first application.
- No custom backend/server, Firebase, mandatory account, remote database, cloud sync, chat, or user-generated public feed.
- Public GitHub repository supplies a limited, read-only catalog of editorial content and metadata.
- User-created pet profiles, reminders, favorites, notes, and logs remain on the device.
- GitHub content is cached locally; the app remains useful offline after first content download.
- No personal pet or owner data is sent to GitHub.
- No dark theme, dark palette, dark-mode switch, or theme preference. The product ships with a carefully designed light appearance only.
- No medical diagnosis, treatment recommendations, medicine dosage, or emergency triage.

## Main navigation
1. **Home** — selected pet, today's care tasks, quick actions, seasonal tips, and recently viewed guides.
2. **Discover** — search and browse care, training, health-awareness, behavior, nutrition, and breed content.
3. **My Pets** — local pet profiles, care history, schedules, and notes.
4. **Saved** — favorites, saved guides, and custom care checklists.
5. **Settings** — reminders, units, privacy, content updates, export/import, and app information.

## Feature coverage
- Multiple local pet profiles for dogs and cats.
- Pet details: name, species, breed/mix, birthday or estimated age, sex (optional), weight, photo, adoption date, microchip note (optional), allergies/conditions entered by owner (optional), vet contact details (optional).
- Breed directory and breed detail pages.
- Care guides, training lessons, behavior explainers, grooming, nutrition basics, enrichment, travel, seasonal safety, new-pet checklists, and senior-pet care.
- Owner-created feeding, grooming, walking, cleaning, appointment, vaccination, and medication reminders. Medication schedule details are entered by the owner or veterinarian; the app never proposes dosage.
- Local care logs: weight, grooming, walks, feeding notes, training sessions, and vet visits.
- Search, filters, bookmarks, share, reading history, and content freshness indicators.
- Local notifications with permission education and quiet-hour controls.
- Export/import of local data using a user-selected file.
- AdMob monetization with protected safety and task flows.

## Planned screens
See `05-screens/`. The plan covers onboarding, home, pet list/profile/editor, reminders, care logs, Discover, search, article feed/detail, breed directory/detail, saved items, notifications, settings, content updates, and local data export/import.

## Architecture summary
Flutter + Riverpod + repository pattern. SQLite (Drift) stores personal data; a small file cache stores validated GitHub JSON and downloaded editorial images. GitHub content is read-only and versioned. Local notifications are scheduled on-device. No account is required.

## Content quality and safety
Content must be written or reviewed by qualified veterinary professionals where it makes veterinary or health-related claims. Clearly distinguish general education from professional advice. Any urgent symptoms or suspected poisoning must direct users to contact a veterinarian or an appropriate US animal poison-control/emergency service immediately; do not attempt symptom diagnosis in-app.

## Monetization
Use consent-aware AdMob placements on suitable discovery and editorial surfaces. Do not place ads in pet emergency guidance, medication/reminder creation, vet-contact details, profile editing, or safety-critical instructions. Rewarded ads are optional and must never unlock essential care or safety information.

## Definition of done
All screens and key states specified; local data model and migrations defined; remote JSON schemas and example records included; offline/update behavior specified; light-only design system documented; privacy and safety boundaries explicit; release and QA checklist complete.
