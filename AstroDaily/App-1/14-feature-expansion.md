# AstroDaily — Expanded Feature Specification

All features remain light-only, local-first and compatible with public read-only GitHub JSON. Astrology content is entertainment and reflection, never guaranteed prediction or professional advice.

## 1. Reading archive and calendar
- Browse previous daily readings by date and sign for as long as the content repository retains them.
- Calendar marks dates with published content; no fake future readings.
- Jump to today, previous/next day, month and available date range.
- Weekly/monthly archive with explicit coverage dates.
- When content is missing, distinguish not published, not downloaded, offline, withdrawn and outside archive retention.
- Saved readings remain locally bookmarked; if the remote record is withdrawn, show an unavailable notice rather than stale advice.

## 2. Richer daily reading experience
- Daily sections: general, love/relationships, work/career, wellbeing/reflection. Categories may be hidden in preferences.
- A short daily theme, one reflection prompt and optional “try this” action framed as a suggestion, not a prediction.
- Reading length preference: concise or expanded where editorial content exists.
- Optional text-size control, reading progress and mark-as-read.
- No generated content or AI claims; all readings are authored and dated editorial data.

## 3. Local personalization
- Remember selected sign and preferred categories.
- Optional favorite signs/topics.
- “Explore another sign” without changing the user's primary sign.
- Journal prompts can be filtered by theme.
- All preferences remain local; no birth details or selected sign sent to GitHub.

## 4. Share-card studio
- Generate share cards on-device from public horoscope text, sign glyph, date, brand and disclaimer.
- Multiple light templates, background/typography variants, preview and save/share.
- Respect platform share sheet; user explicitly chooses destination.
- No journal content included unless user deliberately selects and previews it.
- Keep quotations short enough to avoid copying entire editorial articles; use original app-owned content and maintain attribution if required.

## 5. Notification center
- Daily reading reminder at user-selected local time.
- Weekly reading reminder on selected weekday/time.
- Optional moon-phase reminders.
- Optional reminder for a favorite sign only if the user enables it.
- Quiet hours, per-category toggles, preview text, snooze and disable all.
- Notifications should not expose sensitive journal content or imply alarming predictions.
- Permission denial never blocks reading.

## 6. Engagement without manipulation
- Optional reading streak based only on opening a reading; allow disable/reset.
- Weekly reflection recap based on locally saved prompts/entries; no psychological or health interpretation.
- “Continue exploring” recommendations based on local favorites and cached metadata.
- Avoid guilt, countdowns, fear, artificial scarcity, gambling-like rewards or notifications claiming bad outcomes.

## 7. Lunar calendar enhancements
- Monthly and list views, phase labels, exact source timestamp and device-local time.
- Educational notes for new moon, quarter and full moon.
- Optional calendar reminder; never imply moon phase determines outcomes.
- Include source, calculation dataset/version and verification date.
- Do not implement simplistic client-side moon-phase calculations.

## 8. Astrology learning library
- Structured glossary for signs, elements, modalities, planets and chart terminology.
- Explain Western tropical zodiac as the chosen system.
- Clearly distinguish traditional belief, cultural history and scientific evidence.
- Explain that sun-sign readings are generalized, not natal-chart personalization.
- Retrograde calendar/explainers only if date data is sourced, precomputed and reviewed. Do not calculate planetary positions in the MVP.

## 9. Accessibility and reading controls
- Reading font-size controls, line spacing and high-contrast light palette option (still light).
- Full sign names with glyphs, semantic headings, screen-reader reading order.
- Share cards have text descriptions and adequate contrast.
- Reduced-motion support and no auto-advancing carousel.

## 10. Feature priority
Core release: date archive, reading calendar, local reading preferences, share-card studio, notification controls and learning library. Follow-up: optional streak, weekly reflection recap, richer lunar calendar and sourced retrograde calendar. Birth charts, ascendant, houses calculation and live transits remain out of scope without a validated ephemeris.
