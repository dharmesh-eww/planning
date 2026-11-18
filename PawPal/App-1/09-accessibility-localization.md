# Accessibility and Localization

## Accessibility
- Aim for 48dp touch targets and support Android font scaling.
- Add meaningful semantics for pet photos, buttons, icons, reminder states and charts.
- Provide text summaries for charts and visible labels for all primary actions.
- Maintain readable contrast, logical focus order, keyboard visibility and reduced-motion support.
- Never communicate urgency, completion, or species through color alone.

## Localization
Initial release: en-US. Externalize every user-facing string; use pluralization and locale-aware date/number formatting. Store normalized values with explicit units. Future candidate: es-US, with professional review for safety-related translations.

## Units
Default: lb, in, °F, mi. Optional: kg, cm, °C, km. Persist raw value and unit; convert only for display with tested conversion logic.
