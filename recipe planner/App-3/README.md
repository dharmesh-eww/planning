# Recipe Planner App-3 — Modern Heritage Kitchen

A third visual direction for the same global, offline-first Recipe Planner product in App-1 and App-2.

## Concept
A contemporary recipe journal: the familiarity of a handwritten family cookbook, the order of a kitchen index, and the clarity of a modern mobile app. Traditional in atmosphere, but not tied to any country, cuisine, religion, or historical culture.

- Warm parchment, ink, terracotta, olive, and spice-inspired accents.
- Recipe-card structures, chapter tabs, margin notes, ruled dividers, and hand-drawn food illustrations.
- Readable serif display typography paired with a clear sans-serif UI typeface.
- Expressive but purposeful Lottie and Flutter animations.
- Calm, high-contrast cooking and grocery workflows.

## Same product scope
Discover/search recipes; ingredient finder; recipe details; servings and units; weekly meal planner; meal picker; generated and aggregated grocery lists; favorites and collections; cooking mode, timers and optional text-to-speech; optional pantry/inventory and cooking history; settings and static content updates.

## Non-negotiable constraints
- Flutter, Riverpod, Clean Architecture, and local SQLite persistence.
- Offline-first; downloaded recipes and all personal data remain usable offline.
- Public GitHub repository may host read-only static JSON, manifests, and image assets.
- No Firebase, custom API server, accounts, login, or cloud sync.
- Personal plans, lists, favorites, pantry, history, and preferences stay on device and are never uploaded.
- AdMob only in discovery surfaces, never cooking mode, timers, grocery check-off, or task-critical flows.
- Global audience: localization, RTL, metric/US customary units, locale-aware dates/week starts, and ingredient aliases.
- Nutrition/allergen information must be verified; no medical claims.

## Navigation
Five primary destinations: Today, Recipes, Plan, Groceries, and Kitchen. Secondary areas: saved recipes, collections, pantry, cooking history, settings, and content updates.

## Screens
19 screens are specified in 05-screens: splash, onboarding, Today, discover/search, results, recipe details, ingredient finder, weekly planner, meal picker, grocery overview, grocery details, cooking mode, timer, saved recipes, collections, collection details, pantry, cooking history, settings/content updates.

## Design principles
1. Heritage without imitation: universal paper, ink, bookbinding, botanical, and kitchen-note cues only.
2. Legibility before atmosphere: decorative type never carries quantities, instructions, warnings, or controls.
3. Motion with meaning: animation communicates state, continuity, or completion.
4. Task-first cooking: cooking mode and timers stay calm and glanceable.
5. Respect local context: language, units, dates, ingredients, and week starts are locale/user-aware.
6. Offline integrity: all personal workflows work without network access.

## Asset notes
07-assets contains candidate animation references and original screen-mockup prompts. The prompts are not generated screenshots, and actual Lottie JSON files are not included. Check each asset's licence before bundling.

## Accessibility
Offer reduced motion and respect platform preferences. Replace page turns, parallax, and moving illustrations with immediate changes or subtle opacity transitions when motion is reduced. See [W3C animation guidance](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions).

## Exclusions
Planning only. No Flutter source code, exported Lottie JSON, or generated mockup images are included.
