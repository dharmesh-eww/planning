# Core User Flows

## First launch
Splash → local database initialization → optional onboarding → language/units/week start and optional cooking preferences → starter content download if online → Today. Offline users continue with bundled starter content.

## Find a recipe
Recipes → search/category → filters → results → detail. Returning preserves result position and filters. Empty results offer reset and ingredient finder.

## Cook with available ingredients
Recipes → Ingredient Finder → include/exclude ingredients → matching results → detail. Distinguish exact matches from recipes requiring additional items.

## Plan the week
Plan → choose date and meal slot → Add recipe → search/saved recipes → confirm → meal appears. Support move, replace, and remove with undo where practical.

## Build groceries
Groceries → generate from planned meals → review aggregated ingredients → edit/remove pantry-owned items → check items. Incompatible units remain separate.

## Cook
Recipe detail → Start cooking → prep summary → step mode → optional timer → mark steps complete → finish. Keep screen awake only when user enables it and platform allows.

## Save
Recipe detail → save → choose collection or create one. All changes stay local.

## Pantry
Kitchen → Pantry → add/edit item and optional expiry → optionally exclude pantry items from grocery generation. Pantry is not required for core use.

## Update content
Settings → Content updates → check manifest → show version, size, and summary → confirm → download temporary bundle → validate → atomically activate. Interrupted/invalid updates retain previous content.

## Failure branches
Network unavailable: use cache. Invalid manifest: retain current dataset. Missing image: show illustration placeholder. Migration failure: protect existing data and provide recovery guidance. Notification permission unavailable: keep an in-app timer and explain platform limits.
