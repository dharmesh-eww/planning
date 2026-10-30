# Navigation and Interaction Model
## Bottom navigation
- Today: at-a-glance next meal, continue cooking, quick actions.
- Discover: search, browse, filters, ingredient finder entry.
- Plan: weekly calendar and meal slots.
- Groceries: current shopping lists and progress.
- You: saved recipes, collections, pantry, history, settings.

## Navigation behavior
Recipe Details opens from any source and returns to that source context. Cooking Mode is full-screen and distraction-free. Add-to-plan is available from Recipe Details and planner. Grocery generation is reachable from Plan and Groceries. Preserve search query, filter, scroll position, and selected planner week when returning.

## Interaction rules
- Every icon-only action has a semantic label.
- Tapping a row opens its detail; overflow menu is reserved for secondary actions.
- Swipe gestures are optional shortcuts, never the only way to perform an action.
- Bottom sheets have a visible title and clear close behavior.
- Do not stack sheets or dialogs.
- All Lottie animations are non-blocking and have a static fallback.
