# Localization Strategy

Required locales: English (en), Hindi (hi), Bengali (bn), Gujarati (gu), Kannada (kn), Marathi (mr), Nepali (ne), Punjabi (pa), Tamil (ta), Telugu (te).

Provide a searchable language picker in onboarding and Settings. Display each language's native self-name; no flags. Language and currency preferences are independent.

Localize every app-owned string: navigation, labels, buttons, hints, validation, empty/loading/offline/error states, dialogs, notifications, accessibility labels, tooltips, chart titles/summaries, Lottie semantic descriptions, OAuth explanations, sync/conflict states, export/import headings and generated reports. No hardcoded UI strings. User-entered names/notes remain verbatim.

Use locale-aware date/time/number/currency/plural formatting; support text scaling, mixed scripts and RTL. CI must validate identical keys, placeholders, missing strings and malformed JSON. Native-speaker review required. Adjacent JSON files are starter resources copied from App-1, not the final complete catalog; add Motion Ledger-specific keys and review translations before release.