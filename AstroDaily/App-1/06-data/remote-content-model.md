# GitHub Remote Content Model

## Principles
Public read-only editorial content only. Never upload birth dates, journal entries, preferences, selected sign, reminders, favorites or device/user IDs. Use stable IDs, schema versions and publication dates.

## Suggested repository
```
astrodaily-content/
  manifest.json
  signs/zodiac-signs.json
  horoscopes/daily/YYYY-MM-DD.json
  horoscopes/weekly/YYYY-WW.json
  horoscopes/monthly/YYYY-MM.json
  compatibility/pairs/*.json
  lunar/YYYY.json
  learning/index.json
  learning/articles/*.json
  prompts/daily-prompts.json
  assets/asset-manifest.json
```

## Horoscope record
id, schema_version, sign_id, period_type, period_start, period_end, editorial_timezone, category, title, body, reflection_prompt_id, optional lucky_color/number, published_at, updated_at, disclaimer, status.

## Sign record
id, name, symbol, conventional_date_start/end, element, modality, ruling_planet, image, description, tradition_notice.

## Compatibility record
pair_id, sign_a, sign_b, traditional_themes, strengths, friction_points, conversation_prompts, disclaimer, updated_at.

## Lunar event
id, event_type, timestamp_utc, source_timezone, source_name, dataset_version, educational_note, updated_at.

## Manifest and lifecycle
Manifest has schema_version, content_version, published_at, minimum_app_version, files[path/version/size/checksum/locale/date coverage], changelog. Editorial readings must be reviewed for tone, date coverage, duplication and prohibited guarantees before publication.
