# Localization Strategy

## Required languages
- English — en
- Hindi — hi
- Bengali — bn
- Gujarati — gu
- Kannada — kn
- Marathi — mr
- Nepali — ne
- Punjabi — pa
- Tamil — ta
- Telugu — te

Use BCP 47 locale identifiers and a localization framework with generated typed accessors. English is the fallback language; missing translations must be caught during CI/release validation, not silently shipped as hardcoded strings.

## Language selection
Provide a dedicated searchable language selection screen during onboarding and in Settings. Show each language in its own script and its localized self-name. Do not use flags. Preview common financial values and date formatting.

## No hardcoded user-facing text
Every app-owned visible string must be localized:
- Screen titles, navigation labels, buttons, menus, tabs.
- Field labels, hints, helper text, validation errors.
- Empty states, loading states, offline states, and error messages.
- Dialogs, bottom sheets, confirmation text.
- Notification titles/bodies and reminder text.
- Accessibility labels, tooltips, semantics, and chart summaries.
- Google OAuth pre-permission explanations, sync statuses, and error messages.
- Export/import headings and generated report labels.
- Default category names and recurring frequency labels.

Developer logs and internal identifiers are not UI strings. User-entered names/notes are stored verbatim and never auto-translated.

## Formatting
Use locale-aware date, time, decimal, grouping, currency, and plural formatting. Do not concatenate currency symbol and amount manually. Currency selection is independent from language. Store canonical ISO currency codes and minor units. Respect RTL for Punjabi if user chooses a right-to-left locale variant; test mixed-direction currency and digits.

## Translation quality
Use native-language review for financial terminology. Keep source English strings short and context-specific. Avoid ambiguous generic keys. Use placeholders with named arguments and plural rules for counts and amounts.

## Testing
- Pseudo-localization and overflow checks.
- Long translated strings on small screens.
- RTL and mixed-script rendering.
- Screen reader labels in every supported locale.
- Currency/date/decimal formatting.
- Missing-key detection and duplicate-key detection.
- Verify all 10 language files have identical key sets.

## Starter translation resources
The adjacent JSON files provide a starter glossary for core navigation, transaction, budget, and Google Sheets terms. They are a translation baseline, not a substitute for native-speaker review.
