# Screen 01 — Splash & Initialization
## Goal
Provide a brief brand moment while initializing local storage.
## Layout
Small centered symbol and wordmark on plain neutral background. No large illustration, marketing copy, or progress spinner unless initialization visibly takes time.
## Behavior
Initialize local database and preferences. Route first-time users to onboarding; returning users to Today. Do not block on GitHub. Offline launch uses cached data.
## States
First launch, returning launch, initialization, local error with Retry.
## UI generation prompt
Create a minimal mobile splash screen for a global recipe planner. Use a quiet neutral background, small memorable geometric food-inspired mark, clean wordmark, and restrained green accent. Keep it fast, calm, and uncluttered. No login, promotional content, or large illustration.
