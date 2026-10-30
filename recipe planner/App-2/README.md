# Recipe Planner — App-2
## Product and UI/UX Plan
**App-2 is a second visual concept for the same Recipe Planner product described in App-1.** Features and offline-first constraints stay consistent; visual language, navigation presentation, components, and motion are intentionally different.

## Product vision
A calm, clean, minimal cooking companion that makes recipe discovery, weekly planning, and grocery shopping feel effortless for a global audience. It should feel approachable on first launch and remain efficient for daily use.

**Promise:** Plan simply. Cook confidently.

## Audience and global requirements
Designed for a worldwide audience, not a single country:
- Support localization and RTL layouts; never bake UI text into illustrations.
- Support metric and US customary units, with explicit unit labels and careful conversion rules.
- Support 12/24-hour time and locale-aware dates, week starts, number formats, and decimal separators.
- Use internationally understandable food categories while allowing regional cuisines and local ingredient names/aliases.
- Dietary filters must be configurable and clearly defined; do not assume one country's diet labels or ingredients.
- Avoid country flags as language selectors; show language names in their own scripts.
- Recipe content should identify servings, ingredient quantities, preparation/cook time, and allergen information only when verified.
- Avoid region-specific currency, holidays, food safety claims, or default cuisine assumptions.
- Use plain language, scalable typography, accessible contrast, and icon-plus-label controls.

## App requirements
Same core product scope as App-1:
1. Discover/search recipes by title, ingredient, cuisine, category, dietary tags, cooking time, and difficulty.
2. Ingredient finder (“Cook with what you have”) with matched and missing ingredients.
3. Recipe detail with servings, quantities, prep/cook time, ordered instructions, and optional tips.
4. Weekly meal planner with breakfast, lunch, dinner, and snack slots.
5. Grocery list generation from selected planned meals; merge compatible units only.
6. Favorites and personal collections.
7. Focused cooking mode with step progress and timers.
8. Optional pantry inventory and cooking history.
9. Offline access to downloaded recipes and all personal data.
10. Optional AdMob monetization only in non-critical discovery contexts.

## Product constraints
Flutter + Riverpod + SQLite. Public GitHub repository is read-only static content source for JSON and images. No Firebase, custom API backend, login, account, or cloud sync. User-created data stays on-device. App must not upload favorites, ingredient selections, plans, shopping lists, inventory, preferences, or history.

## Main navigation
Five destinations: **Today**, **Discover**, **Plan**, **Groceries**, **You**. Use a clean compact bottom navigation with icon and text label. “Today” is the home dashboard; “You” contains saved recipes, collections, pantry, history, and settings. These are presentation labels; underlying capabilities remain the same as App-1.

## UI concept
- Minimal light-first design with optional dark theme.
- Soft neutral background, crisp white surfaces, near-black typography, one calm green/teal accent, and a tiny warm highlight.
- Flat surfaces and fine dividers rather than heavy card stacks.
- Strong typography hierarchy, generous spacing, restrained photography, simple line icons.
- Motion is purposeful: small transitions, state feedback, and a few lightweight Lottie illustrations for empty/loading/success states.
- Avoid excessive gradients, glassmorphism, giant hero banners, ornamental shapes, and animations that delay tasks.

## Screen inventory — 19 screens
01 Splash & Initialization; 02 Onboarding & Preferences; 03 Today/Home; 04 Discover & Search; 05 Search Results; 06 Recipe Details; 07 Ingredient Finder; 08 Weekly Planner; 09 Add Meal / Recipe Picker; 10 Grocery Overview; 11 Grocery List Details; 12 Cooking Mode; 13 Timer; 14 Saved Recipes; 15 Collections; 16 Collection Details; 17 Pantry; 18 Cooking History; 19 Settings & Content Updates.
Loading, offline, empty, permission, validation, and error conditions are states within these screens.

## Overlays
10 dialog patterns: remove planned meal, delete list, delete collection, clear completed items, discard edits, timer complete, content update failure, notification permission rationale, reset local data, generic destructive confirmation.
12 bottom-sheet patterns: recipe actions, filters, sort, cuisine/category/diet selector, add to plan, choose date/meal, add grocery item, edit quantity/unit, grocery grouping, ingredient picker, collection picker/create, contextual actions.

## Global design and accessibility
Use logical start/end layout direction; test long translated labels and plural forms. Support large text, screen readers, reduced motion, keyboard navigation where applicable, 48dp minimum targets, and contrast suitable for WCAG AA. No information communicated by color alone. Provide manual controls for all important animated feedback.

## Content and data
Remote GitHub content: manifest, recipes, ingredients, aliases/translations, categories, cuisines, dietary labels, unit metadata, images, attribution/licence records. Local SQLite: favorites, collections, meal plans, grocery lists/items, pantry, history, preferences, downloaded content, versions.
See `06-data/` for schema and examples. Use stable IDs, locale-keyed labels, canonical ingredient IDs, amount types, and unit dimensions.

## Motion and asset plan
See `07-assets/animation-catalog.md` for suggested Lottie assets, exact use cases, fallback behavior, licensing checks, and links to example assets. Use Lottie JSON for broad player compatibility or dotLottie where the chosen Flutter player supports the required features. Keep assets local in the shipped app; do not make core UI depend on a remote animation request.

## Quality bar
A first-time user should understand the five tabs quickly, find a recipe in a few taps, add a meal without a tutorial, and check groceries with one hand. All core flows work offline after content download. Motion never blocks interaction or creates a motion-only state.
