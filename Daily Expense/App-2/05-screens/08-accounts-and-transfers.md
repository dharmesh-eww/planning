# Accounts and Transfers

## Purpose
Account balances, create/edit/archive accounts, transfer between accounts. Transfers are atomic and excluded from income/expense totals; validate currency.

## Design and states
Motion Ledger midnight/elevated surfaces, high-contrast hierarchy and short purposeful transitions. Include default, loading, empty, validation, success, offline and reduced-motion/large-text variants where relevant. All labels, hints, errors and accessibility descriptions are localized. Core data is local SQLite; screen works offline.
