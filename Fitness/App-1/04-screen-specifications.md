# Screen-by-Screen Specifications — Form & Flow

This is the implementation contract. The image requirements below are mandatory, not optional suggestions.

## 01 Welcome and privacy
Brand promise, offline-first/no-account explanation and Continue. Use `ff-onboarding-athlete.png` as a full-bleed/large editorial visual with a readable text panel. Returning users bypass setup.

## 02 Setup preferences
Optional experience, home/gym, equipment, training days and kg/lb. Use `ff-onboarding-equipment.png` as a supporting illustration. Skip is always available; settings remain editable.

## 03 Today dashboard
Greeting/date; large image-led today's-workout hero using `ff-hero-today-strength.png`; Start/Resume; weekly activity strip; next session; concise consistency insight. Empty state uses `ff-empty-today.png` and offers Browse plans/Create plan. Do not use a generic icon in place of the hero.

## 04 Plan library
Search/filter by goal, duration, level, location and equipment. Cards use the relevant plan cover from the asset manifest and show days/week, duration and equipment. Distinguish bundled from user-created plans. Include an accessible list alternative.

## 05 Plan detail
Large plan cover, summary, level, weekly schedule, exercise preview thumbnails, equipment, adaptation notes and Start/Save/Customize actions. No guaranteed outcome claims.

## 06 Exercise library
Search, muscle-group chips, equipment and difficulty filters. Every exercise item includes its mapped thumbnail, name, primary muscle and equipment. Provide accessible list alternative and text labels.

## 07 Exercise detail
Large demonstration image, target-muscle illustration, equipment, difficulty, numbered steps, breathing cue, common mistakes, substitutions and safety notes. Use image refs from the asset manifest; do not render an empty placeholder or fitness icon as the main media. Defaults are editable suggestions.

## 08 Workout builder
Plan/session name, exercise search with thumbnails, selected list with thumbnails, drag reorder, sets/reps/load/duration/rest configuration, validation and save draft/plan.

## 09 Active workout
Current exercise image and concise instructions remain visible above the set table. Show a thumbnail in the previous/next queue, large input controls, completed state, rest action, pause and finish. Persist state across backgrounding. The exercise image must not disappear when the user logs a set.

## 10 Rest timer
Large countdown, progress arc, +15/-15 seconds, skip, pause/resume and optional sound/haptic. Use `ff-rest-breathing.png` as a subtle static fallback/visual, not as the timer itself. Announce milestones, not every second.

## 11 Workout completion
Duration, exercises/sets completed, optional perceived effort and notes. Use `ff-completion-celebration.png` and a calm completion animation; no shame for partial sessions.

## 12 Workout calendar
Month/week completed, planned and rest days; day selection opens sessions. Include agenda list alternative. Use small custom state illustrations only when needed.

## 13 Progress overview
Range selector; sessions, training time, consistency and performance trends. Charts include units, legend, date range and text summary. Use custom achievement artwork only for verified milestones.

## 14 Body measurements
Manual weight and optional circumference entries, dated history, unit conversion and charts. Use `ff-empty-measurements.png` when empty. Hide-sensitive-values option; no diagnosis.

## 15 Goals
Weekly sessions, consistency or user-defined performance target. Use `ff-goal-milestone.png` for a verified goal milestone. Progress, edit, pause and delete; avoid prescriptive body-weight goals.

## 16 Workout history
Chronological sessions with date, plan, duration and status; search/filter; use `ff-empty-history.png` for the empty state.

## 17 Session detail
Logged sets/reps/load/duration/notes and records. Show the session's exercise thumbnails. Allow corrections while preserving timestamp and edit transparency.

## 18 Reminders
Local schedule, day/time, quiet hours and permission education. Use a small custom reminder illustration in the permission education panel. Graceful denied-permission state.

## 19 Profile and preferences
Units, theme, language, equipment, training days, haptics, sound, reduced motion and privacy. Use a consistent custom illustration for profile header; controls remain native and accessible.

## 20 Data and backup
Export JSON/CSV; validate import and preview counts; explain merge/replace behavior and sensitive file contents. No cloud upload.

## 21 Language selection
English, Hindi, Bengali, Gujarati, Kannada, Marathi, Nepali, Punjabi, Tamil and Telugu in native scripts, no flags, instant preview.

## 22 Exercise content updates
Optional manual GitHub catalog check; version, size and changelog; consent before download; validate before apply; retain bundled fallback and rollback.

## 23 Search
Search exercises, plans and history; categorized results with relevant thumbnails and locally stored recent searches.

## 24 Shared states
No plans/history/measurements, invalid import, storage error, notification denied, reset confirmation and unsaved workout. Localize every state and use the mapped illustration for each empty state.

## Screen approval checklist
- Required image asset is present and loads from the bundled asset directory.
- The image depicts the actual content/action of the screen.
- No required image is replaced by a Material icon, emoji or empty color block.
- Text, controls and images match the supplied visual reference.
- Loading, error, empty and populated states are all designed.
- Image has an accessible label or is explicitly decorative.
