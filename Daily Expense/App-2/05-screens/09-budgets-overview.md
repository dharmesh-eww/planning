# Budgets Overview

## Purpose
Overall/category budgets, spent/remaining amounts, period selector and warnings. Animate progress only when values change; overspending uses calm warning language, never celebration.

## Design and states
Use the Motion Ledger visual tokens and restrained motion. Include default, loading, empty, validation, success, offline and reduced-motion/large-text variants where relevant. Localize all labels, hints, errors, notifications and accessibility descriptions. Core behavior uses SQLite and works offline.
