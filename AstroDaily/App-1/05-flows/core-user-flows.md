# Core User Flows

## First launch
Splash → initialize SQLite → welcome → select sign manually or enter optional birth date → explain local-only storage and entertainment disclaimer → Today. No account.

## Choose/update sign
Today → sign selector → choose sign or enter month/day → if cusp date, show ambiguity explanation and manual override → save locally → refresh reading selection.

## Read daily horoscope
Today → choose date/category → load cached content → show reading period and disclaimer → save/share/open reflection prompt. If unavailable, show previous cached reading with date clearly visible.

## Weekly/monthly reading
Today or Zodiac → period selector → fetch/cache matching period pack → show start/end dates → category tabs → save/share.

## Zodiac profile
Zodiac → choose sign → profile with date range, element, modality, ruling planet and traditional associations → related learning content.

## Compatibility
Explore → Compatibility → choose sign A and sign B → show traditional themes, strengths, friction points and conversation prompts → save/share. No compatibility score.

## Lunar calendar
Explore → Moon Calendar → month navigation → phase timeline → event detail with UTC source and local converted time → optional local reminder.

## Journal
Today prompt → write reflection → save locally → Saved/Journal → edit/delete/export. No cloud analysis or automatic sharing.

## Notifications
Settings → enable daily/weekly/lunar reminder → choose time/quiet hours → explain permission → request permission → schedule locally. If denied, show in-app reminder settings and continue.

## Content update
Settings → Content Updates → check manifest → validate date coverage/schema/checksum → download changed packs → transactional cache replacement → show success/last checked. On failure retain prior cache.

## Export/import
Settings → Data & Privacy → export selected local data → system share/save. Import → validate JSON → preview → merge/replace → backup existing local data → import transactionally.

## Failure and edge cases
Cusp birthdays; no birth date; manually selected sign; future date; missing daily reading; delayed content publication; timezone/day boundary; leap day; DST change; offline; stale cache; GitHub rate limit; malformed JSON/checksum; unsupported schema; missing image; denied notification; reminder timezone change; corrupt/old backup; duplicate journal IDs; insufficient storage; content withdrawn.
