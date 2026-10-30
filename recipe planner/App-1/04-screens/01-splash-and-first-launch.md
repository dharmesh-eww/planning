# Screen 01 — Splash & First Launch

## Purpose
Establish brand identity briefly, initialize local services, and route the user to onboarding or Home.

## Layout
- Centered app mark and wordmark.
- Optional short brand line: “Plan less. Cook happily.”
- Minimal progress indicator only when initialization genuinely takes time.
- Background uses the warm canvas color; no busy food collage.

## Behavior
- Load local preferences and database.
- Check whether first-launch onboarding is complete.
- Do not wait for GitHub network access to show the app.
- Route to Onboarding for first launch; otherwise Home.
- If initialization fails, show a recoverable error with Retry.

## States
- Normal launch.
- First launch.
- Local database initialization.
- Offline launch.
- Initialization error.

## UI prompt
Design a polished mobile splash screen for a warm, modern recipe planner. Use a restrained food-inspired identity, centered logo/wordmark, warm cream background, subtle herb-green accent, excellent spacing, and a tiny progress indicator only if needed. Avoid login fields, promotional banners, and unnecessary controls. Show the first-launch transition as a clean, friendly experience.
