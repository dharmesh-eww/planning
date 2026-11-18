# AstroDaily — Complete Screen Matrix and Acceptance

This matrix extends the original screen set. All screens use the Celestial Daylight light-only design system.

## Navigation and screens

| Area | Screen | Primary content and actions | Empty/error/edge states |
|---|---|---|---|
| Onboarding | Welcome | Explain entertainment positioning and local privacy | Skip, returning user |
| Onboarding | Sign setup | Manual sign, optional month/day, cusp override | No birth date, ambiguous date |
| Today | Today dashboard | Selected sign/date, daily theme, categories, prompt | Missing reading, late publication |
| Readings | Reading detail | Body, period, date, prompt, save/share | Stale, withdrawn, offline |
| Readings | Category selector | General/love/career/wellbeing preferences | Disabled category |
| Readings | Archive calendar | Available historical dates, month navigation | No archive, expired range |
| Readings | Archive detail | Historical reading with original date | Missing date |
| Readings | Weekly/monthly | Coverage period, category, archive | Year/week boundary |
| Zodiac | Sign directory | 12 accessible sign names and glyphs | Search no results |
| Zodiac | Sign profile | Traditional associations and related content | Missing editorial profile |
| Explore | Compatibility setup | Choose sign A and B, including same sign | Incomplete selection |
| Explore | Compatibility detail | Themes, strengths, friction, prompts | Missing pair content |
| Explore | Moon calendar | Month/list, phase, local time and source | No event pack, timezone |
| Explore | Moon event detail | Source, dataset, educational note, reminder | Stale verification |
| Explore | Learning library | Articles, glossary, elements, modalities | Empty category |
| Explore | Learning detail | Sources, updated date, related content | Withdrawn article |
| Search | Search results | Cached content, filters, recent query | No results, offline |
| Journal | Journal list | Entries, date filter, search | Empty |
| Journal | Journal editor | Prompt, text, tags, optional mood | Unsaved draft, large text |
| Saved | Saved items | Favorites, signs, readings, history | Empty/withdrawn |
| Share | Share-card studio | Template, preview, save/share | Unsupported share target |
| Settings | Preferences | Sign, categories, reading length, text size | Invalid preference |
| Settings | Notifications | Daily/weekly/lunar/favorite sign, quiet hours | Permission denied |
| Settings | Content updates | Manifest, last check, manual refresh | Rate limit, invalid pack |
| Settings | Privacy/data | Journal delete/export, backup/import | Corrupt/old backup |
| Settings | About/legal | Disclaimer, sources, privacy, correction route | Link unavailable |

## Important screen-level rules
- All readings display their actual covered date or period and publication state.
- The archive calendar marks only available published content; no fabricated future content.
- Compatibility has no numeric score, “perfect match” badge or deterministic verdict.
- Lunar event details show source and dataset version; event time is converted from UTC to device local time.
- Journal is private and local. Sharing excludes journal content unless the user deliberately selects it and previews the result.
- Share cards include date, sign and entertainment disclaimer.
- Streaks are optional, non-punitive and can be disabled/reset.
- Notifications never contain birth date, journal text or alarming predictions.

## Global UI states
Loading, offline, stale, missing date, not-yet-published, withdrawn, archive-expired, invalid schema, notification denied/revoked, export/import failure, unsaved journal draft and unsupported share target.

## Acceptance
Users can browse historical readings without changing the current date; missing readings are never replaced with misleading text; local journal works offline; no birth/journal data is transmitted; all astronomy dates have provenance; all screens and overlays remain light-only.
