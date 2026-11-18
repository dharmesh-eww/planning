# Product Requirements

## User jobs
- Read a daily horoscope for a selected sign.
- Browse weekly/monthly readings and choose reading category.
- Learn traditional zodiac sign characteristics.
- Explore compatibility between two signs without deterministic claims.
- Check upcoming lunar events and learn what they traditionally represent.
- Save/share readings and keep private reflection notes.
- Receive optional local reminders.
- Use previously downloaded content offline.

## Sign and birth-date behavior
Support all 12 Western tropical sun signs: Aries, Taurus, Gemini, Cancer, Leo, Virgo, Libra, Scorpio, Sagittarius, Capricorn, Aquarius, Pisces. Store month/day and optional full birth date locally. Common date ranges are display guidance, not astronomical computation. Near boundary dates, show “Your sign may depend on birth year, exact time, and location” and offer manual sign selection. Never require birth time or birthplace for basic horoscopes.

## Horoscope content
Daily, weekly and monthly reading periods. Categories: general, love/relationships, career/work, wellbeing/reflection. Each reading has sign_id, period_type, period_start/end, timezone_basis, title, body, prompt, lucky_color/number only if editorially authored, content_version, published_at, disclaimer, status. Avoid guarantees and deterministic statements. Do not present wellness text as medical advice or career text as financial advice.

## Compatibility
Pair any two signs; support same-sign pairings. Provide traditional element/modality themes, strengths, possible friction, conversation prompts, and a reminder that real relationships depend on individuals. Never score a relationship as destined, doomed, or objectively compatible.

## Lunar calendar
Display precomputed new moon, first quarter, full moon and last quarter events. Store UTC timestamp, event name, source, calculation dataset/version and timezone basis. Convert to device local time; show source and “times may vary by location” where appropriate. Do not calculate phases from a simplistic formula in the client.

## Explore and learning
Explain elements, modalities, symbols, planets, zodiac wheel, astrology history, chart vocabulary, retrograde concepts and common misconceptions. Do not claim scientific validation. Keep learning content clearly separated from daily reading content.

## Journal and personalization
Private local journal entries with date, selected prompt, free text, mood label optional, tags and favorites. No remote sync, cloud analysis, or sharing by default. User can export/delete journal data. App personalization is based on locally selected sign and reading preferences only.

## Notifications
Optional daily horoscope, weekly reading, and lunar event reminders. User selects time, weekdays, quiet hours and categories. Local-only scheduling. Permission denial does not block content.

## Search and saved
Search cached learning articles, sign profiles and readings. Save readings, favorite signs/topics, reading history and share text/image cards. Share content only; journal notes are excluded unless explicitly exported by the user.

## Non-functional
Offline-first; clear stale/loading/error/empty states; locale-aware dates and time zones; accessible typography and controls; reliable local migrations; bounded network fetches; graceful fallback if GitHub content is unavailable.

## Explicit exclusions
No guaranteed predictions, psychic services, live astrologer chat, user-to-user social network, birth-chart/ascendant calculation in MVP, financial/investment/medical/legal advice, exact event prediction, user-generated public horoscope content, account, server, Firebase or cloud sync.
