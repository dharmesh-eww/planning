# Date, Time and Editorial Operations

## Editorial calendar
- Publish daily readings with a stable YYYY-MM-DD key and a documented editorial timezone (recommended America/New_York for initial US publication).
- Weekly and monthly content must carry explicit start/end dates and timezone basis.
- Do not derive a reading date from UTC midnight without converting through the configured editorial timezone.
- Show the reading's covered date/period to the user. If today's reading is not published yet, label the most recent available reading with its actual date; never relabel old content as current.

## Device-local behavior
- Store event timestamps in UTC; preserve source timezone metadata.
- Display lunar event times in device local time and provide source timezone in details.
- Daily reminder uses the user's local clock time; daylight-saving changes must not shift the intended wall-clock reminder unexpectedly.
- Handle leap day, year boundaries, locale-specific first weekday, timezone changes and travel.

## Cusp date behavior
Conventional sun-sign date ranges are a simplified guide. For boundary dates, show a clear notice and let the user manually select a sign. Do not claim exact sign determination without birth year, exact time, location and validated ephemeris data.

## Content operations
- Maintain one source-of-truth content calendar outside the app.
- Editorial review checks originality, repetition, tone, date coverage, reading category, disclaimer and prohibited claims.
- Publish JSON to the public content repository and update manifest version/checksums.
- Keep a changelog and a rollback path to the last valid manifest.
- Withdraw content by changing publication status and manifest references; the app should stop promoting withdrawn items.

## Static hosting limits
Use public raw GitHub files/CDN only for modest read-only datasets. Check manifest infrequently, fetch only required date/sign packs, honor ETag/cache headers, keep payloads small, and avoid request bursts. If content volume or traffic exceeds practical static hosting limits, reduce fetch frequency or split packs; do not silently introduce a server.
