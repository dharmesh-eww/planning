# Screen 07 — Ingredient Finder (“What Can I Cook?”)

## Purpose
Find recipes that can be made with ingredients the user has.

## Layout
- Headline: “What’s in your kitchen?”
- Searchable ingredient field.
- Selected ingredients as removable chips.
- Common ingredient suggestions grouped by category.
- Optional toggle “Include pantry staples”.
- Primary “Find recipes” action.
- Results preview or navigation to matched results.

## Behavior
- Ingredient catalog search is local.
- Support multi-select and deselection.
- Match score = matched required ingredients / total required ingredients × 100.
- Show matched count and missing ingredients; rank by match percentage, then fewer missing items, then time.
- Do not treat optional garnishes as required.
- Allow “show recipes missing up to N ingredients” setting.
- Add missing ingredients to grocery list from recipe result/detail.

## Empty and error states
- No ingredients selected: explain and suggest common ingredients.
- No matches: suggest removing an ingredient or allowing more missing items.
- Offline: works from locally downloaded recipes.

## UI prompt
Create a friendly ingredient-matching screen that makes the core action instantly understandable. Show a searchable ingredient picker, selected ingredients as removable chips, a few visually grouped common ingredient choices, and a prominent “Find recipes” button. Keep it practical and low-friction. Design the matched recipe state with clear match percentage, ingredients available, and missing ingredients. Avoid gamified scores or implying exact match when optional items are involved.
