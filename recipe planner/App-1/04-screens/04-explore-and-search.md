# Screen 04 — Explore & Search

## Purpose
A dedicated discovery hub for searching and browsing the recipe catalog.

## Layout
- Search input at top with clear button.
- Quick filter chips: Cuisine, Meal, Dietary, Time, Difficulty.
- “Browse cuisines” and “Browse categories” sections.
- Ingredient Finder entry point.
- Trending/popular search suggestions based on curated content, not user tracking.

## Behavior
- Submit search on keyboard action.
- Show recent searches only if stored locally; allow clearing.
- Tapping a filter opens the appropriate bottom sheet.
- Filter selections are summarized as removable chips.
- Search can match recipe title, description, tags, and ingredient names using local index.

## States
- Empty query: discovery modules.
- Active query: results view.
- Offline: search local cached catalog.
- No content: explain and provide clear filters action.

## UI prompt
Create an elegant Explore screen for a cooking app. Prioritize a prominent search bar, concise filter chips, attractive cuisine/category browsing tiles, and a clear ingredient-finder shortcut. Use an editorial food-magazine feel with warm neutrals and restrained green accents. Keep content scannable and bottom navigation persistent; avoid a dense filter form or generic analytics dashboard.
