# Screen 09 — Add Meal / Recipe Picker

## Purpose
Choose a recipe for a specific day and meal slot.

## Entry context
Opened from a planner slot. Display selected date and meal type at the top so context is never lost.

## Layout
- Context header: “Add lunch · Tue, 12 Nov” (example format localized).
- Search field.
- Suggested recipes, recently viewed, and browse categories.
- Compact recipe rows with thumbnail, title, time, dietary label.
- Optional “Add without recipe” custom meal entry.

## Behavior
- Selecting a recipe adds it to the exact slot and returns to Planner.
- If slot already contains a recipe, ask whether to replace or add another.
- Avoid losing search/filter context if user opens a recipe preview.
- Custom meal stores title and optional note locally.

## UI prompt
Create a focused recipe picker launched from a meal-planner slot. Keep the date and meal type visible in the header, provide a search field, and show compact recipe rows with thumbnail, title, and cooking time. Make selection feel immediate and clear. Include a simple custom meal option, but do not turn this into a complex form.
