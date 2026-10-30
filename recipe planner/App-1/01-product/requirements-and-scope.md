# Product Requirements and Scope

## Problem
People often struggle to decide what to cook, forget ingredients while shopping, and find meal planning cumbersome. App-1 reduces those steps with recipe discovery, ingredient matching, weekly planning, and a generated grocery list.

## Product principles
- Clarity before density.
- One obvious primary action per screen.
- Useful without account creation.
- Offline-first for previously downloaded content.
- Personal information remains on-device.
- Food imagery supports discovery; text supports confident cooking.

## Functional requirements
### Recipe discovery
- Browse curated recipes by category, cuisine, food type, and tags.
- Search by title and optionally ingredient.
- Filter by prep/cook time, difficulty, cuisine, dietary type, and availability.
- Open detailed recipe information and adjust servings.

### Ingredient matching
- Select ingredients from searchable catalog.
- Optionally mark pantry ingredients as available.
- Rank recipes by match percentage and missing ingredients.
- Let users include/exclude pantry staples.
- Clearly show missing ingredients; do not imply a recipe is fully cookable if key ingredients are missing.

### Meal planning
- Weekly view starts on the user's locale-preferred first day.
- Meal slots: breakfast, lunch, dinner, snack.
- Add, replace, move, and remove planned recipes.
- Generate grocery items from selected planned recipes.
- Prevent duplicate plan entries only when the user confirms; do not silently discard.

### Grocery
- Combine same canonical ingredient and compatible units.
- Preserve quantities and show when units cannot safely be combined.
- Add custom items, edit quantity, check/uncheck, group by aisle/category.
- Grocery list is usable with one hand and offline.

### Personal library
- Favorite/unfavorite recipes.
- Create, rename, and delete collections.
- Add/remove recipes from collections.
- View recently viewed and cooked history.

### Cooking mode
- One clear instruction at a time.
- Previous/next step, step progress, optional keep-screen-awake setting.
- Start timers from a step.
- Adjustable text size and optional speech.
- Prevent accidental exit with a simple confirmation when a timer is active.

## Non-functional requirements
- Fast cold start using local content.
- Network failure must not block local functionality.
- Transactional content sync and schema validation.
- Responsive layouts for common phone sizes.
- Localization-ready labels and units.
- Accessible semantics, contrast, and text scaling.
- No account or backend dependency.

## App-1 release boundary
Must-have: Home, Explore/Search, recipe detail, favorites, ingredient finder, weekly planner, grocery list, cooking mode, local settings, content sync.
Could-have: collections, pantry inventory, cooking history, reminders, nutrition, voice reading.
Do not build social, cloud sync, shopping checkout, or user-generated public content in this release.
