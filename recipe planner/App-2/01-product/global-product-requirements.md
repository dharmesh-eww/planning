# Global Product Requirements
## Localization
- All user-facing copy comes from localization resources; no text embedded in Lottie or image assets.
- Support pluralization, gender-neutral phrasing where possible, long strings, RTL, and script-specific font fallback.
- Locale-aware date, week start, time, number, and decimal formatting.
- Language names are displayed in their native script.
## Measurement and ingredients
- Offer metric and US customary preferences; always display units explicitly.
- Convert mass to mass and volume to volume. Never convert cups to grams without ingredient-specific density.
- Preserve original recipe quantity and unit; clearly show converted values as approximate where relevant.
- Ingredient aliases are locale-aware and searchable.
- Do not assume ingredients are available in every country; allow substitutions only when reviewed and labelled as suggestions.
## Recipe safety and content quality
- Show allergen data only when verified and sourced. Do not infer allergen-free status.
- Provide serving basis for nutrition and clearly mark optional estimates.
- Avoid unsupported health claims and prescriptive medical diets.
- Use licensed/original recipe text and images; track source and rights.
## Calendar and planning
- Respect local first day of week and locale date formats.
- Meal slot names can be localized and configured; default Breakfast, Lunch, Dinner, Snack.
- Store dates in a stable local representation and avoid UTC date shifts for all-day meal plans.
## Offline and privacy
- No account or cloud sync. Personal data remains local.
- GitHub provides read-only public content. Network requests disclose ordinary connection metadata.
- Ads must not receive personal meal plan, grocery list, pantry, or selected ingredient data.
- Offline browsing, saved content, planner, and grocery lists remain usable.
