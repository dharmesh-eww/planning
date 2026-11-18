# Screen 01 — Splash and Onboarding

## Purpose
Initialize local storage and introduce PawPal without forcing account creation.

## Splash
- Brand mark, warm light canvas, concise loading indicator.
- Initialize database and content cache; recover gracefully from migration errors.
- Never wait for GitHub before showing the app.

## Onboarding
1. Welcome and value proposition.
2. Explain local pet profiles and reminders.
3. Choose preferred units: US customary by default; metric available.
4. Optional content interests: dog, cat, both.
5. Notification explanation; permission request deferred until user creates first reminder.

## States
First launch, returning user, database migration, offline, migration failure, skipped onboarding.

## Acceptance
Onboarding can be skipped; no account/email/phone fields; all preferences editable later; no dark appearance or theme selector.
