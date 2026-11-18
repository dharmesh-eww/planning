# Privacy and Security

## Local personal data
Birth date, selected sign, journal entries, favorites, reading history, preferences and reminders remain in app-private local storage. Never transmit them to GitHub, analytics, crash reporting or advertising SDKs. No account, backend, Firebase, remote database or cloud sync.

## Network boundary
GitHub requests contain only public content paths and ordinary network metadata. Never include birth date, journal text, selected sign, device ID or user identifier. Only read public static JSON; no write endpoints.

## Permissions
Notifications are optional and requested after a user enables a reminder. No contacts, location, microphone or broad storage permissions are needed for MVP. Use system file picker for export/import.

## Data safety
Avoid personal content in logs. Explain OS backup behavior. Provide journal delete/export and delete-all-local-data. Do not claim encryption unless implemented and verified. Shared/exported files are controlled by the user after leaving the app.

## User trust
Show entertainment/self-reflection disclaimer in onboarding, reading detail and settings. No guarantees, diagnosis, medical/financial/legal advice or claims of scientifically proven predictions. Publish clear privacy policy and content correction contact.
