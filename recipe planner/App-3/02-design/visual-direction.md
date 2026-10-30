# Visual Direction — Modern Heritage Kitchen

## Design idea
A contemporary recipe journal: warm printed-cookbook character, clear kitchen-index organization, and modern responsive controls. It should feel crafted, not antique, cluttered, rustic-heavy, or culturally specific.

## Palette
Use semantic tokens and verify contrast:
- Canvas: warm parchment/oat.
- Surface: soft ivory.
- Primary text: deep roasted brown.
- Secondary text: warm grey-brown.
- Primary accent: terracotta.
- Positive/ready accent: muted olive.
- Highlight: restrained golden ochre.
- Divider: pale toasted beige.
Dark theme uses deep cocoa/charcoal surfaces and warm readable text, not a simple inversion.

## Typography
- Distinctive readable serif for short page titles and editorial headings.
- Highly legible sans-serif for controls, metadata, quantities, and instructions.
- Tabular numerals for timers, quantities, and durations.
- Never use script/decorative fonts for ingredients, steps, warnings, or buttons.
- Avoid all-caps paragraphs and overly long line lengths.

## Composition
Modern index cards with subtle borders, small chapter tabs, ruled dividers, generous image crops, and compact metadata. Small hand-drawn botanical/utensil illustrations are accents only. Avoid faux stains, distressed textures, cluttered flourishes, and low-contrast beige text.

## Iconography
Use one consistent line-art family with rounded joins. Icons must remain recognizable at small sizes. Food illustrations must not be mistaken for controls. Use real recipe photography when it improves recognition.

## Motion language
- Brief page-leaf transitions for meaningful navigation only.
- Selection uses ink underline or stamped check feedback.
- Add-to-plan can animate a small recipe card into a day slot.
- Grocery completion can draw a check and soften the row.
- Cooking steps use a simple progress rail.
- Target 160–240 ms for micro-interactions and 240–420 ms for meaningful transitions.
- Never delay actions for animation; avoid large zoom, parallax, or continuous loops.
- Respect reduced-motion preference and provide static fallbacks.

## Avoid
Generic gradients, glassmorphism, excessive shadows, ornate vintage flourishes, culture-specific motifs, tiny labels, over-animated cards, auto-playing carousels, and decorative motion in cooking mode.

## QA
Test light/dark themes, small/large phones, tablets, text scaling, RTL, long translations, reduced motion, screen-reader order, high contrast, and text over imagery.
