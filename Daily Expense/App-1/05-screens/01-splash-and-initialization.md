# Screen 01 — Splash and Initialization

## Purpose
Open the app quickly and prepare the local database.

## Layout
Simple brand mark, short app name, compact progress/status label. Avoid showing financial figures before the user unlocks privacy settings.

## Behavior
1. Initialize SQLite.
2. Run safe migrations.
3. Load locale, currency, theme, and privacy preferences.
4. Load cached categories and dashboard summaries.
5. Route to onboarding on first launch or Home otherwise.

## States
Initializing, ready offline, recoverable database error. Never require network or Google authorization.

## Acceptance
No login. No remote dependency. Preserve existing records if migration fails; show a recovery path.
