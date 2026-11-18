# Monetization and Advertising

## Principle
Monetization must not interfere with pet care, safety information, or user-created task workflows.

## AdMob placements
- Native ad: after several organic cards in Discover or article lists; label as Ad/Sponsored.
- Banner: optional on low-risk browsing surfaces only, with reserved layout space.
- Interstitial: disabled in MVP by default; if later enabled, only at a natural navigation break with strict frequency caps and never after completing a care task.
- Rewarded: optional cosmetic extras or nonessential bonus content only. Never gate emergency information, care reminders, core guides, or pet profiles.

## Prohibited placements
No ads in urgent safety/poisoning pages, medication reminders, vet contact screens, pet profile editor, care-log entry, export/import, permission dialogs, or during notification interactions.

## Consent and privacy
Use Google UMP where applicable; request consent before loading personalized ads where required. Provide non-personalized ads when permitted. Do not use pet profile fields, health notes, medication details, or behavior logs for ad targeting.

## Measurement
Use aggregate, privacy-conscious metrics only if needed and disclosed. Track placement performance without recording personal pet data. Define frequency caps and monitor retention, crashes, and accidental clicks.

## Release checklist
AdMob app/ad unit IDs configured per environment; test ads during development; UMP flow tested by region; app-ads.txt published where applicable; store privacy/data-safety declarations reviewed; no accidental production test IDs.
