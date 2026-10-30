# Localization and Accessibility

Initial languages: English, Hindi, Bengali, Gujarati, Kannada, Marathi, Nepali, Punjabi, Tamil and Telugu.

Use Flutter gen_l10n with ARB and generated accessors. No hardcoded user-facing text: labels, errors, validation, onboarding, reminders, accessibility labels, exercise instructions, import/export messages and chart summaries must be localized. User-created plan names and notes remain as entered.

Use locale-aware dates, numbers and pluralization. Units are explicit user preferences, independent of language. Language picker uses native names and no flags. Test font coverage, line wrapping, large text, RTL-ready layout, TalkBack and VoiceOver.

Starter translations require native-speaker review, especially exercise terminology and safety copy. Do not ship unreviewed machine translations for safety-critical instructions.
