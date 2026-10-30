# Screen 05 — Search Results

## Layout
Query title, result count, active filter chips, sort/filter controls, and a responsive recipe list/grid. Cards show image, title, duration, difficulty, and save action.

## Behavior
Preserve query, filters, sort, and scroll position when returning from detail. Sorting options should be understandable and locale-neutral. Empty state offers filter reset or ingredient finder.

## Motion
A short opacity transition for result refresh; do not animate every card. Reduced motion uses immediate replacement.

## Acceptance
Missing images use consistent placeholders. Offline results include cached recipes and clearly identify content availability if needed. Ad placement never masquerades as a recipe card.
