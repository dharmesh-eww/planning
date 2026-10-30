# Screen 08 — Weekly Meal Planner

## Purpose
Let users plan meals for a week with minimal taps.

## Layout
- Week title with previous/next week controls and Today shortcut.
- Compact horizontal day selector.
- Selected day shows four meal slots: Breakfast, Lunch, Dinner, Snacks.
- Filled slots display small recipe image/title and overflow actions.
- Empty slots show a light “Add meal” affordance.
- Bottom or top action: Create Grocery List.

## Behavior
- Default to current week, locale-aware first day.
- Add, replace, move, or remove meal entries.
- Multiple recipes per slot may be supported but should not clutter; default one primary recipe per slot.
- Show unsaved state only if edits are not persisted immediately.
- Grocery generation asks which days/meals to include if the plan is partially filled.

## Empty state
Show a sample explanation and one CTA to plan the first meal.

## UI prompt
Design a clean weekly meal planner for a phone. Use a compact horizontal week/day selector and four clearly labelled meal slots for the selected day. Empty slots should invite adding a recipe; filled slots should show a small food thumbnail, title, and simple edit menu. Make weekly navigation obvious and grocery-list generation easy to find. Prioritize legibility and fast interaction over a dense calendar grid.
