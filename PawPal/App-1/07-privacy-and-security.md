# Privacy and Security

## Local personal data
Pet profiles, photos, notes, vet contact details, reminders, logs, favorites, and preferences stay in app-private local storage. Do not transmit them to GitHub, analytics, crash reporting, or advertising SDKs.

## Network boundaries
- GitHub requests contain only public content paths and ordinary network metadata.
- Do not attach pet IDs, pet names, device identifiers, or profile data to content requests.
- No developer server, remote database, authentication, account, or cloud sync.
- Ad SDK data processing must be disclosed accurately and consent handled where required.

## Permissions
Request notification permission only when the user creates a reminder and understands the benefit. Request photo/media access only when adding a pet image. Use Android photo picker where possible to minimize broad storage access.

## Local protection
Use app-private storage, avoid sensitive values in logs, and consider OS backup behavior. Do not claim database encryption unless implemented and verified. Allow users to export and delete local records.

## Data deletion and retention
Provide pet-level archive/delete, cache clear, reading-history clear, and delete-all-local-data. Explain exactly what is removed. User-selected exported files are outside app control after sharing.

## Safety/legal
Publish a plain-language privacy policy. Clearly state the app is educational and not veterinary care. Maintain a content correction/contact route without requiring an account.
