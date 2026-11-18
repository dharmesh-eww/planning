# Navigation and Interaction

## Bottom navigation
1. Home
2. Discover
3. My Pets
4. Saved
5. Settings

## Global actions
- Add Pet is available from My Pets and the empty Home state.
- Add Reminder is available from a pet profile and the Home care schedule.
- Search is available from Discover and may be opened from Home.
- A selected-pet filter can be changed without losing the current screen's scroll/search state.

## Navigation rules
- Preserve search query, filters, and scroll position when returning from detail pages.
- Article links from a reminder or pet profile should return to the originating context.
- Back closes keyboard, menu, sheet, then screen in that order.
- Destructive actions require confirmation and explain what local data is affected.
- No sign-in, account gate, or account-related navigation.

## Interaction rules
- Pet selector always shows pet name and species.
- Forms use visible labels, inline validation, optional-field labels, and safe defaults.
- Reminder repeat rules must be summarized in plain language before save.
- Notification permission is requested only after explaining the value of reminders.
- Article safety notes and reviewer metadata remain visible.
- Share actions share public content only unless user explicitly selects a local export.
- Offline state never blocks viewing cached guides or editing local pet data.
- All important statuses use text and icon, not color alone.
