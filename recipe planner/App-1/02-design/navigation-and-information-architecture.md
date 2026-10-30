# Navigation and Information Architecture

## Primary navigation
Five persistent bottom destinations:
- Home
- Explore
- Planner
- Grocery
- My Kitchen

Use icon plus text label. Keep labels visible, selected state clear, and ordering stable.

## Navigation rules
- Recipe details can be opened from any tab and should return to the originating context.
- Ingredient Finder is reachable from Home and Explore, and appears as a prominent Explore action.
- Add-to-plan can be initiated from Recipe Details or Planner.
- Grocery generation is available from Planner and Grocery.
- My Kitchen groups personal content: Favorites, Collections, Pantry, History, Settings.
- Cooking Mode is a focused full-screen task and hides the main bottom navigation.
- Timer may be presented as a focused page or overlay; it must not lose its running state when navigating between cooking steps.

## Information hierarchy
Home: search/ingredient action → curated discovery → categories → popular/quick recipes → recently viewed.
Explore: search → quick filter chips → browse categories/cuisines → results.
Planner: week selector → day strip/calendar → meal slots → generate grocery list.
Grocery: active list selector → progress → grouped items → add item.
My Kitchen: favorites/collections/pantry/history/settings.

## Back behavior
- Preserve scroll and filter state when returning from details.
- Closing a sheet restores the previous screen unchanged.
- Back from Cooking Mode asks for confirmation only if needed (e.g. active timer or unsaved progress).
- Deep links are not required for App-1.
