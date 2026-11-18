# Visual Direction — Celestial Daylight

## Design concept
A refined, optimistic celestial editorial style. Think morning light, paper-like surfaces, subtle constellation line art, warm metallic accents used sparingly, and generous readable typography. Avoid the stereotypical dark-purple starfield look.

## Appearance rule
Single light appearance throughout the app. Flutter theme is fixed to `ThemeMode.light`. No theme selector, dark appearance, dark color tokens, or dark-mode assets. App-owned dialogs, sheets, cards, navigation and share-card previews use the same light system.

## Palette
- Canvas: soft daylight cream `#FFF9F0`
- Main surface: white `#FFFFFF`
- Secondary surface: pale lavender-grey `#F1EFF8`
- Primary text: ink plum `#332D40`
- Secondary text: muted mauve-grey `#746D80`
- Primary action: clear indigo `#6557B8`
- Secondary accent: warm champagne `#D6B66D`
- Supporting accent: soft coral `#E9A18E`
- Calm info: pale sky `#E4F1F5`
- Divider: light warm grey `#E9E4EC`
Use readable foregrounds and verify contrast. Gold is a decorative accent, never body text on white.

## Typography
Use a polished, highly legible sans-serif for UI and an optional restrained serif for editorial horoscope headings. Keep body copy accessible and avoid ornate astrology fonts for instructions or dates. Use consistent numerals and localized date formats.

## Layout and imagery
- Light backgrounds with subtle line-art constellations, zodiac glyphs and circular motifs.
- Use small illustrations or editorial sign art, not full-screen dark galaxy imagery.
- Daily reading should prioritize date, sign, period and readable text.
- Compatibility uses side-by-side sign symbols and clear explanatory sections, not a misleading score gauge.
- Lunar calendar uses a simple, clearly labelled phase timeline.

## Components
White reading cards, pale lavender secondary cards, indigo primary actions, outlined chips, simple iconography, clear sign selector, share-card templates with sufficient contrast, and accessible disclaimer callouts.

## Motion and accessibility
Short 160–240ms transitions, subtle zodiac carousel movement, reduced-motion support, 48dp touch targets, scalable text, screen-reader labels, and text descriptions for phase icons.
