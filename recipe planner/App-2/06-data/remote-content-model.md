# Global Remote Content Model
Public GitHub is a read-only static catalog; user data is never written there.

Entities: Recipe (stable ID, localized title/description, cuisine/category IDs, dietary tags, difficulty, prep/cook time, servings, ingredient references, ordered steps, image refs, optional sourced nutrition/allergen data, publication state); Ingredient (stable ID, locale-keyed names, aliases, category, canonical unit guidance); Unit (stable ID, localized labels, dimension and safe conversions); Cuisine/category/diet (stable IDs and localized labels); Manifest (schema/content version, timestamp, paths, versions, checksums).

## Internationalization
Use language-independent IDs and BCP 47 locale tags (e.g. en, en-GB, fr, ar). Fallback exact locale → base language → default language. Never use translated names as IDs.

## Measurements
Keep source amount/unit. Convert only compatible dimensions. Mass-to-volume needs ingredient-specific density and should be avoided unless curated. Support fractions, ranges, to_taste and as_needed as distinct amount types. Preserve precision and locale formatting.

## Quality
Track recipe source and image licence/creator. Allergen/nutrition optional and verified with serving basis. Original/licensed assets only; no medical claims.
