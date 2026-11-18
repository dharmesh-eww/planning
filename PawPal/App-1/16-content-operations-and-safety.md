# PawPal — Content Operations, Safety and Editorial Governance

## Content catalog expansion
Recommended launch catalog:
- Species: dog and cat.
- Categories: getting started, feeding basics, grooming, dental care, training, behavior, enrichment, preventive-care awareness, travel, seasonal safety, senior care, adoption and emergency preparedness.
- Breed library with a balanced initial set; clearly label coverage and avoid implying every breed is included.
- Positive-reinforcement training programs with lesson sequence, skill level and safety notes.
- Editable checklist templates.
- US emergency-resource directory with verification metadata.

## Article metadata additions
id, schema_version, title, summary, locale, species, life_stages, category_ids, tags, reading_minutes, body_blocks, hero_asset_id, reviewer, review_status, reviewed_at, updated_at, sources[], safety_level, safety_notice, emergency_resource_ids[], related_ids[], status, minimum_app_version.

## Resource directory record
id, title, resource_type, country, state_or_region nullable, phone nullable, website nullable, instructions, source_url, verified_at, review_due_at, disclaimer, status.
Only publish resources whose contact information and coverage have been verified. Include a visible verification date. Do not infer local availability from GPS.

## Editorial safety tiers
- General: routine care and enrichment; editorial review.
- Veterinary-reviewed: claims about health, prevention, nutrition or medical topics; qualified veterinary review required.
- Urgent safety: poisoning, heat, cold, choking, trauma or emergency guidance; qualified review, prominent instruction to contact a veterinarian/emergency service, no ads.
Never include diagnosis trees, medicine dosage, treatment protocols or unverified remedies.

## Content lifecycle
Draft → factual/source review → qualified review where required → copy/accessibility review → JSON schema validation → image-license validation → manifest generation → publish → post-publication correction/withdrawal.
Withdrawn urgent/safety content must not remain visible as current advice. If a saved reference points to withdrawn content, show an unavailable notice and a safe replacement link where available.

## Automated repository validation
A GitHub Actions workflow may validate JSON schema, required metadata, duplicate IDs, broken local asset references, image size/dimensions, missing source/reviewer fields for safety tiers, stale resource verification dates, manifest checksums and file-size budgets. This is a static-content repository workflow, not an app backend.
