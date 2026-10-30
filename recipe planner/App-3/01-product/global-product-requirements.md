# Global Product Requirements

## Promise
Help people decide what to cook, plan meals, prepare groceries, and follow recipes with confidence. Feel like a beautifully kept recipe notebook; behave like a dependable utility.

## Audience
Home cooks across countries, languages, skill levels, dietary patterns, devices, and connectivity levels. Do not assume a country, cuisine, family structure, kitchen equipment, or diet.

## Core jobs
- Find recipes by text, ingredient, cuisine, category, time, and difficulty.
- Discover meals using available ingredients.
- Understand ingredients, servings, timings, and ordered instructions.
- Plan meals across a week.
- Generate and combine grocery items from planned recipes.
- Save recipes and organize collections.
- Cook step-by-step with timers and optional spoken instructions.
- Optionally track pantry items and cooking history.

## Functional requirements
- Search supports partial terms; filters can be combined and cleared independently.
- Ingredient finder supports include/exclude ingredients and labels exact versus partial matches.
- Serving changes recalculate quantities only when source data supports scaling.
- Convert only compatible dimensions. Never convert mass to volume without ingredient-specific density.
- Grocery aggregation preserves units and never silently merges incompatible quantities.
- Meal plan uses configurable first day of week and locale-aware dates.
- Grocery items can be checked, edited, grouped, and retained locally.
- Timers provide remaining-time status and continue appropriately within platform limits.
- Cached content remains searchable/readable offline.

## Non-functional requirements
Fast startup, responsive scrolling, large touch targets, scalable text, screen-reader labels, sufficient contrast, and graceful handling of missing images or interrupted downloads. Motion is never required to understand an action or status.

## Privacy and data
SQLite stores personal data locally. Public GitHub may provide read-only recipe JSON, manifests, and images. Never upload plans, pantry, favorites, grocery lists, history, or preferences. No login, Firebase, custom API, or cloud sync.

## Monetization
AdMob only in low-interruption discovery placements. Never show ads in cooking mode, timer, grocery checklist interactions, or confirmation flows. Label ads clearly.

## Globalization
- BCP 47 locale IDs; fallback exact locale → base language → app default.
- Show language names in their own scripts; no flag-based language labels.
- Test RTL, mixed-direction quantities, and numerals.
- Support metric and US customary units.
- Dates, numbers, decimals, pluralization, and week start follow locale/user settings.
- Ingredient aliases may vary by locale; IDs remain language-independent.
- Avoid country-specific currency, holiday, or meal-time defaults.
- Model fractions, ranges, “to taste”, and “as needed” explicitly.

## Safety
Allergen and nutrition information only when verified. Dietary filters are discovery aids, not safety guarantees. No medical claims.

## Success
Evaluate successful discovery, meal assignment, grocery generation, and cooking-step completion in local usability testing. Do not upload personal activity analytics.
