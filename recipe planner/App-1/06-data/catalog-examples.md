# Catalog JSON Examples
Illustrative starter structures. Finalize IDs and localization strategy before creating a large catalog.

## categories.json
```json
{
  "categories": [
    {"id": "breakfast", "name": "Breakfast", "sort_order": 1, "image": "images/categories/breakfast.webp"},
    {"id": "lunch", "name": "Lunch", "sort_order": 2},
    {"id": "dinner", "name": "Dinner", "sort_order": 3},
    {"id": "snacks", "name": "Snacks", "sort_order": 4},
    {"id": "desserts", "name": "Desserts", "sort_order": 5}
  ]
}
```

## cuisines.json
```json
{
  "cuisines": [
    {"id": "gujarati", "name": "Gujarati", "region": "India"},
    {"id": "punjabi", "name": "Punjabi", "region": "India"},
    {"id": "south_indian", "name": "South Indian", "region": "India"},
    {"id": "italian", "name": "Italian", "region": "Europe"}
  ]
}
```

## ingredients.json
```json
{
  "ingredients": [
    {"id": "tomato", "name": "Tomato", "category_id": "produce", "aliases": ["tomatoes"]},
    {"id": "besan", "name": "Gram flour", "category_id": "pantry", "aliases": ["besan", "chickpea flour"]},
    {"id": "curd", "name": "Curd", "category_id": "dairy", "aliases": ["yogurt", "dahi"]}
  ]
}
```

## units.json
```json
{
  "units": [
    {"id": "g", "name": "gram", "abbreviation": "g", "dimension": "mass"},
    {"id": "kg", "name": "kilogram", "abbreviation": "kg", "dimension": "mass"},
    {"id": "ml", "name": "millilitre", "abbreviation": "ml", "dimension": "volume"},
    {"id": "cup", "name": "cup", "abbreviation": "cup", "dimension": "volume"},
    {"id": "tsp", "name": "teaspoon", "abbreviation": "tsp", "dimension": "volume"}
  ]
}
```

## Authoring rules
Use canonical ingredient IDs across recipes. Keep labels localizable. Do not convert mass to volume without ingredient-specific density. Represent “to taste” and “as needed” as amount types, not numeric zero. Validate image paths and licences before publishing.
