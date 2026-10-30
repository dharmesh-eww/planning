# Google Sheets Integration

Optional user-owned export/sync, no developer backend. SQLite is source of truth. User-initiated native OAuth; prefer narrow drive.file scope and validate picker compatibility. No permission prompt during onboarding. Preview selected workbook and exact fields before first transfer.

Local outbox, stable UUID idempotent upserts, revisions, tombstones, explicit conflict resolution, retry/backoff and manual sync. Tokens in platform secure storage, never SQLite/logs. No server-side refresh-token storage or guaranteed background sync when app is closed.

Disconnect stops sync, clears local credentials/metadata, keeps SQLite and leaves remote Sheet untouched. Explain collaborators can see spreadsheet contents.