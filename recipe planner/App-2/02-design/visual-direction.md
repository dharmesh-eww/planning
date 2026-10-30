# App-2 Visual Direction — Quiet Utility
## Design keywords
Clean, minimal, calm, precise, friendly, accessible, global, lightweight.

## Difference from App-1
App-1 uses a warm editorial food-magazine look. App-2 should feel like a refined everyday utility: less visual decoration, smaller image footprints on utility screens, clearer rows, compact controls, more whitespace, and subtle motion.

## Palette roles
- Background: very light neutral / soft grey.
- Surface: white.
- Primary text: near-black charcoal.
- Secondary text: neutral grey with adequate contrast.
- Primary action: muted evergreen or deep teal.
- Accent: soft citrus/amber used sparingly for highlights.
- Semantic colors: accessible success, warning, and destructive roles.
Do not hard-code colors into assets; use theme-aware vectors or animations when possible.

## Typography
Use a highly legible neutral sans-serif with strong international glyph coverage. Suggested scale: screen title 24–28sp; section 17–20sp; body 15–17sp; metadata 12–14sp; cooking instructions 20–24sp. Avoid ultra-light weights and all-caps for long labels.

## Layout and components
- 8dp spacing grid; 16dp standard horizontal margin.
- Thin dividers and subtle surface elevation only where hierarchy requires it.
- Rounded corners 12–16dp; avoid excessive pill shapes.
- Recipe rows with thumbnail, title, time, and one compact descriptor.
- Search and filters remain immediately visible.
- Use compact chips with readable labels.
- Primary CTA has a clear verb.
- Bottom navigation: five destinations, icon plus text.
- Keep the top action and content hierarchy stable across screens.

## Motion
Use 150–220ms transitions for ordinary state changes. Lottie is reserved for onboarding accent, empty states, content sync, and success feedback. Avoid looping decoration on every screen. Respect reduced-motion settings and provide static alternatives.

## Photography
Use consistent, authentic food photography as supporting content rather than decorative wallpaper. Avoid culturally narrow stock-photo assumptions; recipe imagery must represent the recipe accurately.
