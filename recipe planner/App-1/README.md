# Recipe Planner — App-1

> Product and UI/UX planning document. This is a product plan, not a Flutter codebase or Flutter folder structure.

## 1. Product vision
Build a modern, welcoming, easy-to-understand personal cooking companion. It should help people decide what to cook, discover recipes, use ingredients already available, plan meals, and shop without friction. The interface must feel calm and practical: food photography creates appetite, typography makes instructions readable, and common actions remain obvious.

**Product promise:** Decide what to cook, plan the week, and know what to buy — in one simple app.

## 2. Product requirements

### Primary goals
1. Discover recipes by keyword, cuisine, category, dietary type, cooking time, and difficulty.
2. Find recipes from ingredients the user already has.
3. Understand a recipe before starting: servings, time, ingredients, equipment, and clear steps.
4. Plan breakfast, lunch, dinner, and snacks across a week.
5. Generate a grocery list from planned recipes and combine duplicate ingredients.
6. Save favorites and personal collections.
7. Cook confidently using a focused step-by-step mode and timers.
8. Work offline after recipe content has been downloaded.

### Target audience and usability
- Home cooks, beginners, students, families, and people who plan meals.
- A first-time user should understand the five main destinations without a tutorial.
- Use plain language, familiar food imagery, clear labels, and consistent icons.
- Never rely on color or icon alone to communicate meaning.
- Large touch targets (aim for 48dp), readable contrast, and scalable text.
- Keep the primary action visible and avoid crowded screens.

### Out of scope for App-1
- User accounts, login, social feed, comments, chat, and cloud sync.
- Custom API server, Firebase, or backend database.
- Uploading personal preferences, pantry contents, meal plans, favorites, or grocery lists.
- Online grocery checkout or delivery integrations.
- Medical-grade nutrition advice or diet prescriptions.

## 3. Technical/product constraints
- Flutter client; Riverpod state management; SQLite local persistence.
- Public GitHub repository supplies curated static JSON content and recipe images.
- No custom backend and no Firebase.
- User-created data stays on the device in SQLite.
- Fetch content manifest and changed JSON files from GitHub; cache downloaded content for offline use.
- AdMob may monetize selected discovery surfaces. Ads must not interrupt cooking mode, timers, grocery interactions, or critical actions.
- GitHub requests expose ordinary network metadata such as IP address. AdMob may process advertising-related device data. Privacy disclosures must be accurate; do not send personal app data to ads.

## 4. Main navigation and screen count

### Bottom navigation — 5 destinations
1. **Home** — personalized entry point, categories, popular and recently viewed recipes.
2. **Explore** — search, filters, cuisines, categories, and ingredient finder entry.
3. **Planner** — weekly meal calendar and planned meals.
4. **Grocery** — generated and custom shopping lists.
5. **My Kitchen** — favorites, collections, cooking history, pantry, and settings.

### Planned mobile screens — 19
| # | Screen | Main purpose |
|---|---|---|
| 01 | Splash & First Launch | Brand entry, initialization, first-use routing |
| 02 | Onboarding & Preferences | Optional simple setup for dietary/cuisine preferences |
| 03 | Home | Quick discovery and key actions |
| 04 | Explore & Search | Search and browse recipes |
| 05 | Search Results | Results, filters, sorting, empty states |
| 06 | Recipe Details | Recipe overview, ingredients, steps, save and plan |
| 07 | Ingredient Finder | Match recipes to available ingredients |
| 08 | Weekly Meal Planner | Plan meals by day and meal slot |
| 09 | Add Meal / Recipe Picker | Choose a recipe for a planner slot |
| 10 | Grocery List | View, group, check off and edit items |
| 11 | Grocery List Details | Manage a named list and its items |
| 12 | Cooking Mode | Focused step-by-step cooking |
| 13 | Timer | Run one or more cooking timers |
| 14 | Favorites | Saved recipes |
| 15 | Collections | Create and manage recipe collections |
| 16 | Collection Details | Recipes inside a collection |
| 17 | Kitchen Inventory | Optional local pantry inventory |
| 18 | Cooking History | Recently cooked recipes and history |
| 19 | Settings & Content Updates | Preferences, units, offline content, privacy, app info |

**Supporting screen states:** loading, offline, empty, error, permission denied, no search results, no planned meals, no grocery items, and content update available. These are states within screens, not separate screens.

## 5. Dialogs and bottom sheets

### Dialogs — 10 reusable patterns
1. Confirm remove recipe from plan.
2. Confirm delete grocery list / collection.
3. Confirm clear checked grocery items.
4. Discard unsaved changes.
5. Change servings with compact stepper (or use a sheet if more controls are needed).
6. Timer finished alert.
7. Offline / content update failure notice.
8. Permission explanation before notification permission request.
9. Restore/reset local app data confirmation.
10. Generic destructive-action confirmation.

### Bottom sheets — 12 reusable patterns
1. Recipe quick actions (favorite, add to plan, add to collection, share).
2. Recipe filters.
3. Sort options.
4. Select cuisine/category/dietary type.
5. Add recipe to a planner slot.
6. Select planner date and meal slot.
7. Add grocery item.
8. Grocery item quantity/unit editor.
9. Grocery grouping options.
10. Ingredient selection and quantity.
11. Choose collection / create collection.
12. More actions / contextual menu.

Prefer bottom sheets for choosing or editing a small set of values; use dialogs only for short decisions, warnings, and confirmations. Avoid stacking sheets or dialogs.

## 6. Core user journeys
- Discover: Home → category or Explore → results → recipe details → cooking mode.
- Search: Explore → enter query → results → filters → recipe details.
- Cook from pantry: Home/Explore → Ingredient Finder → select ingredients → matched recipes → details.
- Plan a week: Planner → choose day and meal → recipe picker → recipe selected → grocery list generated.
- Shop: Grocery → grouped list → check items → completed state.
- Save: Recipe details → favorite or collection → My Kitchen.
- Cook: Recipe details → adjust servings → start cooking → step navigation → timer → finish → cooking history.

## 7. Recipe detail information hierarchy
1. Hero food image and recipe title.
2. Short description and cuisine/category tags.
3. Prep time, cook time, total time, difficulty, servings.
4. Primary actions: Start Cooking, Add to Plan; secondary Save.
5. Ingredients with quantities and optional checkboxes.
6. Equipment (only when useful).
7. Numbered preparation steps.
8. Tips, substitutions, storage, and optional nutrition.
Keep important information above long-form content; use section anchors or sticky section tabs only if testing proves helpful.

## 8. Modern UI direction
- Warm, editorial food-app visual language; avoid generic dashboard cards everywhere.
- Light warm-neutral background, deep readable text, one fresh herb/leaf accent, and restrained warm highlight color.
- Large appetizing recipe photography with consistent aspect ratios and rounded corners.
- Strong typographic hierarchy: expressive screen titles, compact metadata, highly readable body text.
- Use whitespace and clear section grouping instead of excessive borders.
- Cards only where they help compare or select content; use horizontal carousels sparingly.
- Bottom navigation labels always visible; active destination clearly indicated.
- Primary CTA uses consistent placement and wording.
- Use skeletons for loading, helpful empty states with one next action, and retry controls for errors.
- Respect system text scaling, safe areas, keyboard, reduced motion, and accessibility semantics.
- Motion should be subtle: 150–250ms transitions, no decorative animation that delays tasks.

## 9. Data required

### Remote GitHub content
- Manifest and content version metadata.
- Recipe catalog and recipe detail data.
- Categories, cuisines, dietary types, tags.
- Ingredient catalog, ingredient categories, canonical units.
- Recipe ingredient quantities and preparation steps.
- Image paths, optional thumbnails, attribution/licence metadata.
- Optional cooking tips, substitutions, storage notes, nutrition values with source/serving basis.
- Localization strings or language-specific content.

### Local SQLite data
- Favorites and collections.
- Weekly meal plans and recipe-slot assignments.
- Grocery lists and grocery items, checked state, quantity, unit, category.
- Pantry inventory and expiry dates (optional feature).
- Recently viewed and cooking history.
- User preferences: language, units, dietary filters, theme, serving defaults.
- Downloaded recipe data, manifest version, file version, sync status.

### Data ownership rules
Remote recipe content is read-only from the app. User data is local-only. Content refresh must not overwrite favorites, meal plans, grocery lists, or pantry records. Use stable IDs. A removed remote recipe should be marked unavailable rather than cascading deletion of personal references.

## 10. GitHub JSON content plan
See `data/` for schemas and examples. Suggested content files:
- `manifest.json`
- `categories.json`
- `cuisines.json`
- `dietary_types.json`
- `ingredients.json`
- `units.json`
- `recipes/*.json` (grouped by cuisine or category)

Recipe JSON must include stable ID, title, description, image, category IDs, cuisine ID, dietary tags, difficulty, prep/cook time, servings, ingredient IDs and quantities, ordered steps, and publication state. Optional fields must be explicitly optional and validated.

## 11. Offline and content update requirements
1. Load the local database immediately; never block the home screen on network.
2. Check the GitHub manifest in the background or when user requests an update.
3. Download only changed files.
4. Validate schema and content before import.
5. Import each update transactionally; update version metadata only after success.
6. Keep existing valid content if network, parsing, or import fails.
7. Cache recipe images and show placeholders when unavailable.
8. Explain the last successful update and provide a manual retry.

## 12. Accessibility and quality acceptance criteria
- All primary actions have visible text labels.
- Touch targets aim for at least 48dp.
- Text remains readable at large system font sizes.
- Contrast meets WCAG AA targets where applicable.
- Screen reader labels describe buttons, images, quantities, and checked states.
- Keyboard does not hide search or grocery entry actions.
- Empty and error states explain what happened and what to do next.
- No user data is transmitted to GitHub or ad providers.
- Core browsing, favorites, planner, and grocery list work offline with cached data.

## 13. Definition of done for App-1 planning
- Every planned screen has its own detailed specification and UI-generation prompt.
- Shared dialogs and bottom sheets are documented.
- Main navigation and key user journeys are consistent.
- Required remote and local data are defined.
- JSON schemas/examples are included.
- No Flutter directory structure or source implementation is included in this planning package.
