# Dialogs and Bottom Sheets

## Dialog patterns
1. Confirm delete recipe from collection.
2. Confirm delete collection.
3. Confirm clear grocery list.
4. Confirm clear cooking history.
5. Confirm discard unsaved edits.
6. Confirm content update download/install.
7. Explain offline/update failure with Retry.
8. Explain notification permission limitation.
9. Explain unavailable recipe content.
10. Confirm reset preferences.

Dialogs are compact, plain-language, and reserved for consequential decisions. Use explicit action labels; avoid vague “OK” for destructive actions.

## Bottom-sheet patterns
1. Add meal to date/slot.
2. Choose recipe for planner slot.
3. Edit meal slot/date.
4. Add ingredient to finder.
5. Filter recipes.
6. Sort recipes.
7. Change servings.
8. Edit grocery item.
9. Choose grocery category.
10. Add to collection / create collection.
11. Choose timer duration.
12. Choose content update details.

## Visual treatment
Use warm ivory surfaces, subtle ink divider, serif sheet title only when short, sans-serif controls, and clear drag handle. Sheets should not use faux parchment textures that reduce contrast.

## Interaction
- Sheets are dismissible with clear close/back behavior.
- Tapping outside dismisses only when no unsaved decision is at risk.
- Destructive actions require explicit confirmation.
- Preserve entered values when validation fails.
- Every sheet/dialog exposes accessible title, description, and focus order.
- Under reduced motion, present immediately or use a brief opacity transition.
