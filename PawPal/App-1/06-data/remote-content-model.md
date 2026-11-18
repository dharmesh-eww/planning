# Remote Content Model — GitHub JSON

## Principles
Public, read-only, versioned editorial data only. No personal pet data, owner identifiers, reminders, care logs, favorites, or analytics are sent to GitHub. Stable IDs are required. Optional fields must be nullable and schema-versioned.

## Suggested repository layout
```
pawpal-content/
  manifest.json
  config/app-config.json
  categories/categories.json
  articles/index.json
  articles/dog/*.json
  articles/cat/*.json
  breeds/dogs/*.json
  breeds/cats/*.json
  training/programs/*.json
  training/lessons/*.json
  safety/resources.json
  faqs/index.json
  assets/asset-manifest.json
```

## Manifest fields
schema_version, content_version, published_at, minimum_app_version, files[{path, version, size_bytes, sha256, locale, species}], image_base_url, changelog.

## Article fields
id, schema_version, title, summary, body_blocks, category_ids, species, life_stages, tags, reading_minutes, hero_image, reviewed_by, reviewed_at, updated_at, sources, safety_level, safety_notice, related_ids, status.

## Breed fields
id, name, species, aliases, size_range, coat, grooming_level, activity_level, descriptors, care_considerations, image, updated_at, sources, editorial_notice.

## Training lesson fields
id, program_id, title, goal, prerequisites, steps, positive_reinforcement_notes, safety_notes, species, life_stage, review_metadata.

## Content lifecycle
Draft → editorial review → veterinary review when health claims apply → publish → versioned manifest. Withdrawn content must be hidden from discovery but retained in local cache only when needed for graceful references; show unavailable state and never surface withdrawn safety advice as current.
