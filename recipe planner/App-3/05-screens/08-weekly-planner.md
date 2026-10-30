# Screen 08 — Weekly Planner

## Layout
Locale-aware week header; horizontal or compact week selector; day sections; meal slots for breakfast, lunch, dinner, and optional snacks. Recipe cards use small index-card treatment.

## Behavior
Support adding, moving, replacing, and removing meals. Week start follows user preference. Empty slots provide Add meal. Planner data is stored only in SQLite.

## Motion
A newly assigned recipe card can slide a short distance into the chosen slot. Drag-and-drop is optional; provide explicit move controls as an accessible alternative.

## States
Empty week, partly planned, full week, offline, and no matching recipe.

## Acceptance
Do not assume meal names/times are universal; allow optional snack slots and editable meal labels where feasible. Date and weekday order follow locale.
