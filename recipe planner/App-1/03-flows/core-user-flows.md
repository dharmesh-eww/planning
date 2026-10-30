# Core User Flows

## Flow A — Discover and cook
1. User opens Home.
2. Taps a recipe card or category.
3. Reviews recipe details: time, servings, ingredients, and steps.
4. Adjusts servings if needed.
5. Taps Start Cooking.
6. Follows one step at a time and starts an optional timer.
7. Completes recipe; app adds it to cooking history if history is enabled.

Success: user can identify what is needed and begin cooking without confusion.

## Flow B — What Can I Cook?
1. User opens Ingredient Finder.
2. Searches/selects available ingredients.
3. Optionally chooses “include pantry staples”.
4. Taps Find Recipes.
5. Sees best matches first, match percentage, and missing ingredients.
6. Filters by time/dietary type or opens a recipe.
7. Adds missing ingredients to Grocery if desired.

Success: matches are transparent; no misleading 100% match.

## Flow C — Plan the week
1. User opens Planner.
2. Selects a day and meal slot.
3. Opens recipe picker.
4. Searches or browses recipes.
5. Adds a recipe; planner slot updates immediately.
6. Repeats for other slots.
7. Taps Create Grocery List.
8. Reviews aggregated items and saves the list.

Success: grocery list is generated without losing existing custom items.

## Flow D — Shop with Grocery
1. User opens Grocery and selects active list.
2. Items are grouped by aisle/category.
3. Taps checkbox while shopping.
4. Can add/edit custom items offline.
5. Clears completed items only after confirmation.

Success: controls are large, legible, and usable one-handed.

## Flow E — Save a recipe
1. User taps Save on a recipe.
2. Recipe is saved to Favorites immediately.
3. Optional collection sheet allows adding to an existing collection or creating one.
4. User finds saved content in My Kitchen.

Success: save state is obvious and reversible.

## Flow F — Update content
1. App loads cached content.
2. Background check fetches manifest.
3. If updates exist, app downloads and validates changed files.
4. Valid content imports transactionally.
5. On failure, old content remains and user sees a retry option in Settings.

Success: app remains useful offline and user data is never affected.
