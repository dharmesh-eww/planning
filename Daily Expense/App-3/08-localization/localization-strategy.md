# Localization Strategy

Locales: English (en), Hindi (hi), Bengali (bn), Gujarati (gu), Kannada (kn), Marathi (mr), Nepali (ne), Punjabi (pa), Tamil (ta), Telugu (te).

Searchable language picker in onboarding and Settings; show native self-names, no flags. Language and currency are independent.

Localize all app-owned strings: navigation, labels, buttons, hints, validation, empty/loading/offline/error states, dialogs, notifications, accessibility descriptions, chart summaries, Lottie semantics, Google OAuth explanations, sync/conflict states, export/import headings and generated reports. No static strings in widgets or animations. User notes/custom names remain as entered.

Use locale-aware date/number/currency/plural formatting, text scaling, mixed scripts and RTL. CI validates identical key sets, placeholders and missing strings. Native-speaker review is required. Locale JSON files are starter copies from App-1; extend them with all Bloom Ledger-specific strings and review before release.