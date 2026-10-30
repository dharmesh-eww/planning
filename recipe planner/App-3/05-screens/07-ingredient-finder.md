# Screen 07 — Ingredient Finder

## Purpose
Find recipes based on ingredients the user already has.

## Layout
Ingredient search/add field; selected ingredient chips; Have and Exclude groups; optional “allow missing ingredients” setting; result count and matching recipes.

## Behavior
Support localized ingredient aliases and stable IDs. Let users remove or move ingredients between groups. Explain exact versus partial matches and list missing ingredients on result cards. All selected ingredients remain local.

## Motion
Adding an ingredient can animate a small chip into its group. Reduced motion inserts it immediately.

## Empty/error states
No ingredients: suggest adding one or browsing recipes. No matches: offer remove exclusions or allow missing ingredients. Offline: search cached recipe index.

## Acceptance
Do not claim a recipe is safe for allergies based on ingredient matching alone.
