# Screen 07 — Categories Management

## Layout
Separate Income and Expense categories; category icon; localized display name; optional subcategory; add/edit/reorder/archive actions.

## Behavior
Default categories use translation keys. Custom categories store user-entered names locally and are not automatically translated. Prevent deleting a category still used by transactions; offer reassignment or archive.

## Acceptance
Category IDs remain stable across language changes. Changing app language changes default labels but not user data or transaction identity.
