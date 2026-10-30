# Screen 01 — Splash and Initialization

## Purpose
Introduce Modern Heritage Kitchen while preparing local storage and cached content.

## Layout
Centered wordmark with a small hand-drawn sprig/steam mark; warm parchment canvas; subtle ink-line border detail; compact progress indicator and plain status label. No promotional copy.

## Behavior
1. Initialize local database and migrations.
2. Load preferences and active content manifest.
3. Check cached content availability.
4. Route to onboarding on first launch, otherwise Today.
5. On failure, show retry/recovery state.

## Motion
A short line-draw may reveal the sprig once. Use a static mark under reduced motion. Never hold the user on splash for animation.

## States
Initializing, restoring local content, offline but ready, recoverable error.

## Acceptance
No account or network is required to start. Cached content works offline. No personal data is uploaded. Screen reader receives a concise loading status.
