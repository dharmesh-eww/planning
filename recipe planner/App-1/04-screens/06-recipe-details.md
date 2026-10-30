# Screen 06 — Recipe Details

## Purpose
Help the user decide whether to cook the recipe and provide everything needed to start.

## Layout
- Large hero image with back and favorite controls.
- Recipe title, short description, cuisine/category tags.
- Metadata row: total time, difficulty, servings.
- Primary CTA: Start Cooking.
- Secondary action: Add to Plan.
- Ingredients section with quantities and serving adjuster.
- Equipment section only if data exists.
- Numbered preparation steps preview.
- Tips/substitutions/storage and optional nutrition with clear source/basis.

## Interactions
- Servings stepper recalculates ingredient quantities proportionally.
- Ingredient checkbox can mark prep progress but does not change pantry inventory automatically.
- Add to Plan opens date/meal selection sheet.
- Save toggles Favorites; collection action is available in quick actions.
- Start Cooking opens Cooking Mode at step 1.

## Data requirements
Recipe identity, image, description, servings, prep/cook time, difficulty, ingredients, units, ordered steps, tags, optional equipment/tips/nutrition, and publication status.

## UI prompt
Design a beautiful recipe detail screen for a modern cooking companion. Lead with a full-width appetizing food photograph, then clear title and compact time/difficulty/servings metadata. Make “Start Cooking” the strongest action and “Add to Plan” secondary. Present ingredients with adjustable servings and readable quantities, followed by clean numbered steps and optional tips. Use a sticky CTA only if it does not obscure content. Avoid excessive badges and tiny metadata.
