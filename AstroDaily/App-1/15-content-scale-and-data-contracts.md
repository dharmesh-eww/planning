# AstroDaily — Content Scale, Data Contracts and Publishing Pipeline

## Editorial volume reality
A full daily catalog for 12 signs × 4 categories means 48 reading records per date. Weekly and monthly content adds more. Treat editorial capacity as a product constraint; never ship placeholder or duplicated readings as if they were unique.
Recommended staged scope:
- MVP: one daily general reading per sign (12/day), plus 2–4 daily categories only when editorial supply is reliable.
- Expansion: daily four-category set (48/day), weekly and monthly content.
- Archive retention: publish an explicit retention window and show dates outside it as unavailable.
- Use concise original content and a content calendar. No AI-generated bulk content without human editorial review.

## Suggested remote repository
```
astrodaily-content/
  manifest.json
  signs/zodiac-signs.json
  horoscopes/daily/YYYY/YYYY-MM-DD.json
  horoscopes/weekly/YYYY/YYYY-WW.json
  horoscopes/monthly/YYYY/YYYY-MM.json
  compatibility/index.json
  compatibility/pairs/*.json
  lunar/YYYY.json
  learning/index.json
  learning/articles/*.json
  prompts/index.json
  retrogrades/index.json
  assets/asset-manifest.json
  schemas/*.schema.json
```

## Daily pack contract
One date file contains metadata and a readings array. Each record includes id, schema_version, sign_id, period_type, period_start, period_end, editorial_timezone, category, title, body, prompt_id, optional lucky_color/number, published_at, updated_at, disclaimer_id, status and revision.
Required uniqueness: sign_id + period_type + period_start + category + locale.
Validation requires all 12 signs for the published categories, no duplicate combinations, valid date coverage, nonempty body, approved disclaimer and published status.

## Weekly/monthly contract
Include period key, explicit inclusive/exclusive date semantics, locale, editorial timezone, all covered signs/categories and publication timestamps. Define week numbering convention (ISO week or explicit start/end dates) and test year boundaries.

## Manifest contract
schema_version, content_version, published_at, minimum_app_version, editorial_timezone, archive_start_date, latest_available_date, files[{path,version,size_bytes,sha256,locale,date_range}], changelog.
Use exact byte sizes and checksums generated during release; placeholder checksum strings are never valid production data.

## Compatibility data
Store unordered pair IDs consistently (e.g. aries-taurus and canonical order) so duplicate reversed pairs cannot diverge. Same-sign pair is supported. Require themes, strengths, possible friction, prompts, disclaimer, sources and updated_at. Do not store numeric compatibility scores.

## Lunar data
Store event ID, phase, timestamp_utc, source_timezone, source_name, dataset_version, verified_at, educational_note and source URL. Validate chronological order, event uniqueness and supported date range.

## Content validation pipeline
A GitHub Actions workflow can run JSON Schema validation, duplicate-ID checks, required-sign/category coverage, date-period checks, timezone validity, source/disclaimer checks, asset existence, file-size budgets and checksum generation. It is a repository CI pipeline only, not a backend service.
