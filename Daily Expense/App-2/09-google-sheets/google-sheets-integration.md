# Google Sheets Integration

Optional user-owned export/sync; no developer backend. SQLite remains source of truth and app works when declined.

Flow: explain scope/data → user taps Connect → native OAuth → user creates/selects spreadsheet → preview tabs/columns → choose one-time export or ongoing sync → confirm first transfer.

Prefer narrow `drive.file` scope and verify picker support. Avoid broad Drive/Sheets scopes by default. Do not request access during onboarding. Handle denied permissions. Tokens stay in platform secure storage, never SQLite/logs.

Use local outbox, stable UUID idempotent upserts, revision metadata, tombstones, conflict snapshots and explicit resolution, quota-aware batches and retry/backoff. Never silently overwrite. No server-side refresh-token storage or guaranteed background sync when app is closed.

Disconnect stops sync, clears tokens/metadata, retains local DB and leaves remote Sheet untouched. Explain that anyone with spreadsheet access can view the finance data.