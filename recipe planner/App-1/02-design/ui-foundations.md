# UI Foundations and Visual Direction

## Design character
A modern, warm, editorial cooking companion. The app should feel inviting and trustworthy rather than like a generic admin dashboard. Use food photography as the visual anchor and simple typography/layout for utility tasks.

## Color roles (choose final values during visual design)
- Canvas: warm off-white / very light cream.
- Surface: white or subtly warm surface.
- Primary text: deep charcoal/green-black with strong contrast.
- Secondary text: muted neutral, still readable.
- Primary accent: fresh herb/leaf green for primary actions and selected states.
- Warm accent: restrained tomato/terracotta for small highlights, not warnings.
- Success: accessible green; warning and destructive states use semantic colors.
- Dark theme: deep neutral surfaces, adjusted text and accents; do not simply invert colors.

## Typography
- One highly legible sans-serif family with distinct weights.
- Screen title: 26–32sp, semibold/bold.
- Section title: 18–22sp, semibold.
- Body: 15–17sp, regular with comfortable line height.
- Metadata: 12–14sp; never use low contrast.
- Cooking instruction: 20–24sp default, scalable.

## Layout
- 8dp spacing rhythm.
- 16–20dp horizontal page padding.
- 12–20dp card radius; avoid rounding every tiny element.
- Full-width hero image on recipe details.
- Recipe cards use consistent 4:3 or 3:2 imagery; compact rows for dense search results.
- Sticky bottom CTA only when it improves task completion and does not obscure content.
- Keep bottom navigation persistent on top-level tabs only.

## Components
- Primary, secondary, text, and destructive buttons.
- Search field with clear affordance.
- Filter chips with selected state and removable tokens.
- Recipe card (large, compact, horizontal).
- Time/difficulty/servings metadata.
- Ingredient row with quantity and optional checkbox.
- Step row and cooking-step focus panel.
- Empty-state illustration/icon + concise message + one action.
- Skeleton placeholders, inline error/retry, offline indicator.
- Bottom navigation with icon and label.

## Interaction and motion
- Touch targets aim for 48dp minimum.
- Use 150–250ms transitions; preserve context when navigating back.
- Bottom sheets have clear title, close affordance, and sticky Apply when needed.
- Confirm destructive actions; don't confirm harmless actions.
- Avoid surprise auto-navigation and excessive toast messages.
- Haptics are optional and subtle.

## Accessibility
- WCAG AA contrast targets where applicable.
- Do not convey state through color alone.
- Meaningful semantics for icon-only controls.
- Respect system text scale and reduced motion.
- Screen reader order follows visual reading order.
- Provide text labels for timers and ingredient quantities.

## Image guidance
Use original or properly licensed food images. Crop consistently, prefer natural lighting and appetizing but believable styling. Every image needs alt/semantic text where meaningful and a graceful placeholder. Avoid text baked into recipe photography.
