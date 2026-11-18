# AstroDaily — App-1: Complete Product Plan

## Product concept
AstroDaily is a bright, approachable zodiac and horoscope companion for US adults interested in astrology as entertainment, reflection and lifestyle content. It offers dated daily/weekly/monthly readings, 12 zodiac profiles, compatibility explainers, a sourced lunar calendar, a reading archive, private journaling, share cards and local reminders. It does not claim scientific certainty, guaranteed predictions or professional advice.

## Product promise
A thoughtful daily astrology check-in with clear, enjoyable content and useful ways to explore zodiac traditions.

## Audience
US adults interested in horoscopes, zodiac personality content, relationships and self-reflection. Initial locale en-US. Sun-sign readings are generalized editorial content, not personalized birth-chart calculations.

## Hard constraints
- Flutter Android-first app.
- No custom backend/server, Firebase, mandatory account, remote database, cloud sync, chat or public user-generated feed.
- Public GitHub repository supplies limited, read-only horoscope/editorial JSON, sign metadata, compatibility content, lunar events and optional sourced calendar datasets.
- Birth date, selected sign, journal, favorites, reading history, preferences and reminders stay local.
- Never send personal birth details, selected sign or journal text to GitHub, analytics or ad targeting.
- Light appearance only: no dark theme, dark palette, theme switch or theme preference.
- Astrology is entertainment/self-reflection, not medical, financial, legal or guaranteed predictive advice.

## Navigation
Today · Zodiac · Explore · Saved · Settings.

## Complete functionality
1. Onboarding with manual sign selection or optional common sun-sign selection from month/day; cusp override and local-only birth date.
2. Today dashboard with daily reading, general/love/career/wellbeing categories, daily theme, reflection prompt, save/share and content date.
3. 12 sign profiles with traditional element, modality, ruling planet and sign associations.
4. Daily, weekly and monthly readings with explicit coverage dates and publication dates.
5. Reading archive and calendar navigation for available historical content.
6. Compatibility between any two signs, including same-sign, using non-deterministic themes and prompts—not scores.
7. Precomputed lunar calendar with source, dataset version and local-time display.
8. Explore library: astrology basics, elements, modalities, symbols, planets, history, chart glossary and sourced retrograde explainers.
9. Private local journal, prompt library, favorites, reading history and optional reading streak/weekly recap.
10. On-device share-card studio with preview and user-controlled sharing.
11. Configurable daily/weekly/lunar notifications and quiet hours.
12. Offline cached content, manual updates and versioned local export/import.

## Truthfulness boundaries
Static sign horoscopes are editorial readings, not individualized birth-chart calculations. Common sign date ranges are approximate; cusp users can choose manually. Moon and retrograde events must be precomputed from documented sources; no simplistic client-side astronomy formula. No natal chart, ascendant, houses, planetary positions or live transit engine in MVP.

## Architecture and data ownership
Flutter + Riverpod + repository pattern. Drift/SQLite stores personal data. GitHub JSON is public read-only content with bounded fetch, validation and local cache. Local notifications only. No account/backend/Firebase/cloud sync.

## Monetization
Consent-aware AdMob in Explore/learning feeds and optionally zodiac directory after organic content. No ads inside reading bodies, journal, compatibility result, lunar detail, onboarding, settings or share-card flow. Interstitial disabled in MVP.

## Appearance
Refined daylight editorial light-only design; subtle constellation line art, cream/white surfaces, pale lavender, ink-plum text and clear indigo actions. No dark cosmic backgrounds or dark theme.

## Detailed plan index
- `01-product/product-requirements.md` — product scope.
- `02-design/` — visual direction.
- `03-architecture-and-data.md`, `06-data/`, `15-content-scale-and-data-contracts.md`, `19-daily-pack.example.json` — architecture, JSON schemas and publishing pipeline.
- `04-navigation-and-interaction.md`, `05-flows/`, `05-screens/`, `18-screen-matrix-and-acceptance.md` — navigation and complete screen behavior.
- `14-feature-expansion.md` — archive, share cards, notifications and engagement.
- `07-privacy-and-security.md`, `16-engagement-privacy-and-content-ethics.md` — privacy and ethical engagement.
- `08-monetization-and-ads.md` — advertising.
- `09-date-time-and-content-operations.md` — dates and editorial operations.
- `10-accessibility-localization.md`, `11-testing-and-release.md`, `17-detailed-qa-and-acceptance.md` — accessibility, QA and release.
- `12-ui-reference-prompts.md`, `13-roadmap-and-acceptance.md` — UI direction and roadmap.

## Definition of done
Users can read clearly dated horoscopes without an account; archived content is never misrepresented as current; local personal data never leaves the device; GitHub access is bounded/read-only; timezone handling is correct; content has editorial review; disclaimers are visible; light-only design and ethical ads are enforced.
