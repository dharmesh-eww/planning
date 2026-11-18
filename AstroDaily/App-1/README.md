# AstroDaily — App-1: Complete Product Plan

## Product concept
AstroDaily is a bright, approachable zodiac and horoscope companion for US adults interested in astrology as entertainment, reflection, and lifestyle content. It offers daily/weekly/monthly readings, 12 zodiac sign profiles, compatibility explainers, lunar calendar content, journaling prompts, saved readings, and local reminders. It does not claim scientific certainty, guaranteed predictions, or professional advice.

## Product promise
A thoughtful daily astrology check-in with clear, enjoyable content and useful ways to explore zodiac themes.

## Audience
US adults interested in horoscopes, zodiac personality content, relationships, and self-reflection. Initial locale en-US. Avoid presenting the app as a birth-chart engine unless a genuine calculation system is implemented and validated.

## Hard constraints
- Flutter Android-first app.
- No custom backend/server, Firebase, mandatory account, remote database, cloud sync, chat, or user-generated public feed.
- GitHub-hosted public JSON is a limited, read-only source for horoscope/editorial content, sign metadata, compatibility content, and lunar calendar datasets.
- Birth dates, selected sign, journal entries, favorites, preferences, and reminders stay locally.
- Never send personal birth details or journal entries to GitHub.
- Light appearance only. No dark theme, dark palette, theme switch, or theme preference.
- Astrology content is entertainment/self-reflection, not medical, financial, legal, or guaranteed predictive advice.

## Navigation
Today · Zodiac · Explore · Saved · Settings.

## Main functionality
1. Onboarding: choose zodiac sign manually or calculate a common sun sign from month/day; optional birth date stored locally only.
2. Today: daily horoscope, general/love/career/wellbeing categories, sign selector, daily reflection prompt, share/save.
3. Zodiac: 12 sign profiles with date ranges, element, modality, ruling planet, symbol, strengths/challenges framed as traditional associations.
4. Daily, weekly and monthly readings with clear publication date and content period.
5. Compatibility: pair two signs; explain traditional themes, communication prompts, and non-deterministic caveats.
6. Lunar calendar: new/full/quarter moon dates and educational notes from precomputed JSON; device-local date display.
7. Explore: astrology basics, elements, modalities, houses glossary (educational only), retrograde explainers, numerology-style entertainment only if separately scoped.
8. Journal: private local reflection entries and prompts; no AI or server analysis.
9. Saved readings, favorites, reading history, share cards and notifications.
10. Local reminders for daily check-in, weekly reading, and lunar event; user controls time and quiet hours.
11. Offline cached content and manual GitHub content updates.
12. Export/import local journal, preferences, favorites and reminders using versioned JSON.

## Important truthfulness boundary
Static sign horoscopes are editorial readings, not individualized birth-chart calculations. Sun-sign date boundaries can be ambiguous near cusps and depend on year/time/time zone; allow manual sign override. Do not imply moon phases are live calculations: publish precomputed dates and label the source/time-zone basis. No birth chart, ascendant, houses, transits, or planetary positions unless computed by a verified ephemeris engine and clearly scoped in a later release.

## Architecture
Flutter + Riverpod + repository pattern. SQLite via Drift stores personal data. GitHub JSON is read-only public content, fetched on a bounded schedule and cached locally. Local notifications are on-device. No login.

## Monetization
Consent-aware AdMob on Explore, zodiac directory, and reading feed after organic content. Keep ads out of journal entry, onboarding, settings, and reading share/export flows. Do not imply users must watch ads to receive essential content.

## Definition of done
Complete screen/flow specs, light-only design system, local/remote schemas, date/time handling, content publishing rules, privacy and disclaimer, ad policy, offline/update behavior, testing and release checklist.
