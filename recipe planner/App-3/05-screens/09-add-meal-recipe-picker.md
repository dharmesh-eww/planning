# Screen 09 — Add Meal / Recipe Picker

## Entry
Opened from an empty planner slot or an existing meal's replace action.

## Layout
Selected date and meal slot summary; search; tabs or filters for all recipes and saved recipes; compact recipe list; selected state; confirm action.

## Behavior
Selecting a recipe and confirming adds it to the target slot. Changing date/slot is explicit. Prevent accidental duplicate assignment only when product rules specify; otherwise allow the same recipe on multiple days.

## Motion
Selected row receives a checkmark and subtle ink underline. Confirm closes the picker promptly; no long card-flight animation.

## Acceptance
The target slot is always visible. Empty results link to Discover. Selection and confirmation are screen-reader accessible.
