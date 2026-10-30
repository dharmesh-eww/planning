# Remote Content Model
## Source and ownership
Public GitHub repository is a read-only source of curated recipe content and images. The app never writes user data to GitHub.

## Entities
Recipe: stable ID, title, slug, description, image references, category IDs, cuisine ID, dietary tags, difficulty, prep/cook time, servings, ingredient list, ordered steps, publication state.
Ingredient: stable ID, localized name, category, canonical unit hints, aliases.
Category/cuisine: stable ID, localized name, optional image/icon, sort order.
Unit: stable ID, localized label/abbreviation, dimension, safe conversion metadata where applicable.
Manifest: schema/content version, timestamp, file paths, per-file version and optional checksum/size.

## Content rules
Stable IDs do not change when title/image changes. Ingredient quantities are numeric where possible; “to taste” uses explicit amount_type. Steps are ordered and independently readable. Optional ingredients are marked. Prep and cooking time are separate. Nutrition is optional and requires source and serving basis. Image attribution/licence metadata is required for third-party assets. Do not publish copyrighted recipes or images without permission.

## Sync rules
Local cache is authoritative for offline reads. Fetch manifest and changed files only. Validate schema before import. Import transactionally. Update version only after successful import. Preserve user-owned records. Unpublished remote recipes are hidden from discovery but must not erase user references.
