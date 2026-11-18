# Core User Flows

## First launch
Splash → local database migration → load bundled starter content → optional onboarding → explain local-only pet profiles and notifications → Home. No account or sign-in.

## Add first pet
Home empty state / My Pets → Add Pet → name and species → optional breed/photo/birthday/weight → review → Save locally → pet becomes selected.

## Manage multiple pets
My Pets → Add Pet → create second profile → pet switcher updates Home, reminders, and logs. Filters always show which pet is selected.

## Create reminder
Pet profile / Home → Add Reminder → choose task type or custom title → set date/time/repeat → optional owner-entered notes → explain notification permission → request permission → schedule locally → confirmation. If denied, reminder remains visible in-app.

## Complete or reschedule reminder
Home schedule → mark done / snooze / skip → update local record → reschedule next occurrence. Undo is offered for accidental completion where safe.

## Record care activity
Pet profile → Care Log → select event → enter optional value/unit/note → save → timeline and relevant charts update.

## Discover care content
Discover → choose species/topic/life stage → browse list → article detail → save/share/related guide. Safety callouts and review metadata appear before or near relevant advice.

## Breed research
Discover → Breeds → filter dog/cat/size/coat/energy → breed detail → compare care considerations → optionally assign breed to a pet profile.

## Search
Search → enter phrase → local cached results → filter → open detail. Show recent searches locally and allow clearing them.

## Content update
Settings → Content Updates → show current version and last check → Check Now → fetch manifest → validate version/checksum/schema → download changed packs → transactional cache update → success. On failure, retain previous pack and show retry later.

## Backup/export
Settings → Data & Privacy → Export → explain included local data → choose JSON backup → system share/save sheet → success. No upload to developer servers.

## Import/restore
Select backup file → validate version and size → preview pets/reminders/logs → choose merge or replace → create pre-restore backup → import transactionally → show results and conflicts.

## Pet deletion
Pet profile → Delete/Archive → show associated reminders and logs → archive by default or confirm permanent delete → cancel notification schedules → update local DB.

## Failure and edge states
- Notification permission denied or later revoked.
- App updated while reminders are scheduled.
- Device reboot or time-zone/DST change.
- GitHub unavailable, rate limited, invalid JSON, stale manifest, missing image, or unsupported schema.
- Pet photo permission denied, file moved, or storage unavailable.
- Empty pet list, no reminders, no saved content, no search results.
- Backup invalid, duplicate IDs, older schema, partial import, or insufficient storage.
- Local notification limit reached; explain and retain in-app schedule.
