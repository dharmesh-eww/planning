# Dialog Specifications
Use dialogs for short decisions, confirmations, and alerts. Keep copy concise and state the consequence.

1. **Remove recipe from plan** — “Remove this meal?” Explain it removes the recipe from this slot but does not change the grocery list. Actions: Cancel / Remove.
2. **Delete grocery list** — Explain list and items are deleted from this device. Actions: Keep list / Delete list.
3. **Delete collection** — Explain recipes and favorites remain. Actions: Cancel / Delete.
4. **Clear completed grocery items** — Explain checked items will be removed. Actions: Cancel / Clear items.
5. **Discard unsaved changes** — Explain edits on this screen will be lost. Actions: Keep editing / Discard.
6. **Timer finished** — Show timer label and completion message. Actions: Dismiss / Add 1 minute.
7. **Content update failed** — Explain saved recipes remain available and offer retry.
8. **Notification permission explanation** — In-app explanation before OS permission request, only after user enables timer notifications; never imitate OS dialog.
9. **Reset local data** — Explicitly list favorites, plans, lists, collections, inventory, preferences, and downloaded content that will be deleted. Actions: Cancel / Reset data.
10. **Generic destructive confirmation** — Name the exact object and consequence; avoid vague “Are you sure?” copy.

## Design rules
Maximum two actions in standard dialogs. Destructive action visually distinct and not default-focused. Do not confirm reversible favorite toggles or checkbox taps. Follow platform back/focus/accessibility behavior.
