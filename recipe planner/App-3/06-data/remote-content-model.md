# Remote Content Model

## Source model
The app may fetch read-only static JSON, manifest metadata, and image assets from a public GitHub repository. No user-specific content is ever written to this source.

## Manifest fields
- schema_version: integer
- content_version: stable string
- generated_at: ISO-8601 UTC timestamp
- default_locale: BCP 47 tag
- supported_locales: array of BCP 47 tags
- recipe_index: path and checksum
- ingredient_index: path and checksum
- category_index: path and checksum
- asset_base: relative asset path
- files: list of path, byte_size, checksum, and content_type

## Recipe content
Use stable language-independent recipe IDs. Localized fields include title, description, ingredient display names, instruction text, category/cuisine labels, and search aliases. Keep source quantities structured: amount, unit, optional range/fraction, and qualifier (to taste/as needed).

## Ingredient identity
Stable ingredient IDs with locale-specific names and aliases. Never use translated labels as primary keys.

## Update safety
Fetch manifest; validate schema/version; show size and summary; download to temporary storage; verify checksums; validate required fields; atomically activate. Retain previous valid content on any failure.

## Offline behavior
Bundle a small starter dataset. Keep last valid dataset and cached images. Never block local planner, saved recipes, grocery lists, or cooking mode because a content endpoint is unavailable.

## Privacy
No personal data, identifiers, pantry contents, favorites, history, or meal plans in remote requests. Static source is read-only from the app's perspective.
