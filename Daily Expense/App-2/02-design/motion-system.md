# Motion System

Motion confirms actions, explains changes, or orients users. It must never delay a save or navigation.

## Timing
Micro feedback 100–160 ms; control 160–220 ms; sheets 220–280 ms; screen transitions 220–320 ms; chart reveal 350–550 ms; Lottie moments 1–2 seconds, skippable and non-blocking.

## Patterns
Subtle button response; short navigation fade/slide; amount-first transaction entry; small save confirmation after SQLite commit; budget progress interpolates to new value; chart draws once; sync indicator loops only while a sync is active.

## Accessibility
Honor OS reduced-motion and app preference. Replace movement with instant state or short opacity transition. Decorative animation excluded from semantics; announce meaningful result once. Provide static fallbacks.

## Performance
Local optimized vector assets, bounded dimensions/layers, pause off-screen animations, dispose controllers, avoid continuous controllers and multiple simultaneous Lottie players. Profile low-memory Android devices.
