# Visual Direction — PawPal App-1

## Concept
**Sunny Companion** — warm, optimistic, editorial, and trustworthy. The interface should feel like a modern pet-care journal: approachable photography, clear typography, soft neutral surfaces, and a fresh nature-inspired accent.

## Light-only appearance
- The app uses a single light appearance throughout.
- Flutter theme configuration is fixed to `ThemeMode.light`.
- Do not implement a theme selector, dark appearance, dark color tokens, or dark-mode assets.
- Ensure dialogs, bottom sheets, system bars, navigation bars, notifications, and embedded web content maintain the intended light presentation where platform controls permit.

## Palette tokens
- Canvas: warm ivory `#FFF9F1`.
- Primary surface: clean white `#FFFFFF`.
- Secondary surface: pale oat `#F5EFE5`.
- Primary text: warm charcoal `#26332D`.
- Secondary text: muted olive-grey `#68756B`.
- Primary action: leaf green `#39845A`.
- Supporting accent: sunny apricot `#F2B36D`.
- Calm info: sky blue `#DCEEF4` with dark readable text.
- Caution: soft amber `#FFF0CF` with explicit icon and label.
- Error: accessible muted coral `#B94D43` with text/icon.
- Borders/dividers: warm grey `#E8E1D7`.

Color is never the only signal for status or urgency. Verify text and control contrast.

## Typography
Use a friendly, highly legible sans-serif. Use expressive but restrained headings, readable body copy, clear metadata, and consistent line height. Prefer sentence case. Avoid novelty display fonts for care instructions.

## Layout and imagery
- Use generous whitespace and a clear content hierarchy.
- Editorial cards use real, licensed dog/cat photography with consistent crops.
- Pet profile images use circular or rounded-square crops.
- Use species and topic icons as supporting cues, not replacements for labels.
- Keep primary actions obvious; avoid stacking too many cards on the home screen.
- Article pages prioritize readable body text, source/reviewer metadata, and safety callouts.

## Components
Buttons: rounded, high-contrast leaf-green primary action; outlined secondary action.
Cards: white surfaces, subtle warm border/shadow, consistent radius.
Chips: pale neutral fill with readable text and selected state border.
Forms: grouped sections, persistent labels, inline validation, clear optional markers.
Reminders: task title, pet name, due time, repeat summary, and completion action.
Safety callout: pale amber or pale coral surface with icon, explicit heading, and direct next step.

## Motion
Short 160–240ms transitions, subtle card press feedback, progress transitions, and confirmation animations. Respect reduced motion. No looping decorative animations.

## Accessibility
Minimum 48dp touch targets, large text support, semantic labels, chart summaries, focus order, visible selected states, and no color-only meaning.
