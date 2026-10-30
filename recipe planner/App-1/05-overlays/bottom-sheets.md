# Bottom Sheet Specifications
Use sheets for contextual selection and lightweight editing. Each has a clear title, close affordance, and comfortable touch targets.

1. **Recipe quick actions:** Save/remove favorite, Add to planner, Add to collection, Share recipe.
2. **Recipe filters:** Cuisine, category/meal, dietary type, max total time, difficulty; Clear all and Apply.
3. **Sort options:** Recommended, Shortest time, Recently added (if date exists), Alphabetical. Do not claim popularity without data.
4. **Cuisine/category/diet selector:** Searchable list for long catalogs; selected state visible.
5. **Add recipe to planner:** Date and meal slot preselected from context; explicit replace behavior.
6. **Select planner date and meal slot:** Compact date picker plus Breakfast/Lunch/Dinner/Snack.
7. **Add grocery item:** Name required; quantity, unit, category optional; keyboard must not cover Save.
8. **Grocery quantity/unit editor:** Item name, quantity, unit, category; validate nonnegative values.
9. **Grocery grouping:** Category, recipe, or custom order; default category.
10. **Ingredient selection:** Search catalog, category shortcuts, selected count, Done action.
11. **Choose/create collection:** Existing collections plus Create collection without losing context.
12. **More actions:** Rename, duplicate, export, remove; destructive options separated and labelled.

## Shared behavior
Dismiss by close/swipe/back; preserve edits where possible; never stack sheets; sticky Apply/Save only when pending edits; respect keyboard and safe areas.
