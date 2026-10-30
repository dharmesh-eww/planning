# Add and Edit Transaction

## Purpose
Amount-first expense/income/transfer form with category, account, date, merchant and note. Validate then save to SQLite immediately; show compact success Lottie only after commit.

## Design and states
Motion Ledger midnight/elevated surfaces, high-contrast hierarchy and short purposeful transitions. Include default, loading, empty, validation, success, offline and reduced-motion/large-text variants where relevant. All labels, hints, errors and accessibility descriptions are localized. Core data is local SQLite; screen works offline.
