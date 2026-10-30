# Motion System — Gentle Growth

## Character
Organic, calm and tactile: leaf-like easing, soft card elevation, gentle draw-on illustrations, short slide/fade transitions, progress fill, and small success moments. Avoid springy overshoot and perpetual motion.

## Durations
Micro feedback 100–150 ms; control 160–220 ms; sheet 220–280 ms; screen 220–300 ms; chart/progress 300–500 ms; Lottie feedback 0.8–1.6 s, skippable and non-blocking.

## Interaction
- Cards subtly lift on press.
- Selected categories settle with a tiny scale/outline transition.
- Save confirmation uses a small sprout/check animation after SQLite commit.
- Budget bars animate only when values change.
- Charts reveal once on entry or range update.
- Sheets rise gently; dismiss naturally.
- Sync motion loops only while user-started sync is active.

## Accessibility and performance
Honor system/app reduced-motion. Provide static alternatives. Decorative animation excluded from semantics; announce state text once. Lazy-load, pause off-screen, dispose controllers, limit layers/size and profile on entry-level devices.
