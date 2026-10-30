# Screen 13 — Timer

## Purpose
Run recipe-related or custom cooking timers reliably.

## Layout
- Large remaining-time display.
- Circular or linear progress visualization with accessible text equivalent.
- Start/Pause, Resume, Reset controls.
- Timer label (e.g. “Steam dhokla”).
- Optional preset duration or custom duration entry.
- Multiple timers may be supported later; App-1 can start with one active timer.

## Behavior
- Use monotonic/absolute end-time logic so countdown remains correct if app is backgrounded.
- Notify when finished only if notification permission is granted.
- Timer completion alert includes dismiss and add-time actions.
- Returning to Cooking Mode preserves the timer.

## UI prompt
Create a simple, reassuring cooking timer screen with a very large countdown, clear timer label, prominent Start/Pause control, and secondary Reset action. Use a calm warm surface and a subtle progress ring. The timer must remain readable at a glance; avoid decorative clutter and small controls.
