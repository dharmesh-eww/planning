# Screen 17 — Category and Currency Preferences

## Purpose
Manage default/custom categories and the currencies available to the user.

## Layout
Category management entry; preferred display currency; per-account currency; add/edit currency preference; decimal display preview.

## Behavior
Currency preference is not an exchange-rate conversion. Existing transactions retain their original currency. Category translations use stable keys for built-in categories; custom names remain user-entered.

## Acceptance
Do not infer currency from language or device region without user confirmation. Currency exponent and symbol formatting come from currency metadata.
