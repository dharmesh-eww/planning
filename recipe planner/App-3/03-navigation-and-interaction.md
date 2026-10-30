# Navigation and Interaction

## Primary navigation
Five labelled destinations styled like restrained cookbook chapter tabs:
1. Today — daily overview and next planned meal.
2. Recipes — discovery, categories, search, ingredient finder.
3. Plan — weekly calendar and meal slots.
4. Groceries — generated and manual lists.
5. Kitchen — saved recipes, collections, pantry, history, settings.

## Secondary navigation
Recipe detail opens from any card and returns to its origin. Add-to-plan opens a date/meal selector. Saved recipes, collections, pantry, history, settings, and content updates live under Kitchen.

## Behavior
- Preserve scroll position and filters when returning from details.
- Back closes the topmost sheet/dialog before leaving a screen.
- Confirm destructive actions.
- No account or server-backed personal state.
- Cards have one primary action; secondary actions use explicit controls.
- Do not rely on gestures alone.
- Use color plus shape/underline/check for selection.
- Loading states are quiet and do not block unrelated navigation.
- Empty states offer one clear next action.

## Motion
Use short page-leaf transitions only for top-level context changes; use simple fades or immediate changes when reduced motion is enabled. Avoid animating every list row and avoid auto-playing motion.

## Accessibility
Expose semantic labels and selected/disabled states. Support screen readers, text scaling, sufficient contrast, focus order, and system reduced-motion preference. See [WAI guidance](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions).
