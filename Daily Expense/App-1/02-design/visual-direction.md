# Visual Direction — App-1

## Concept
**Clear Ledger**: calm, trustworthy, modern personal finance UI. The visual language should feel organized and reassuring rather than bank-like, gamified, or overly decorative.

## Palette
- Canvas: soft neutral off-white.
- Surfaces: white or near-white.
- Primary ink: deep charcoal/navy.
- Positive/income: restrained teal/green.
- Expense: muted terracotta/red, never the only indicator.
- Budget warning: amber with icon and text.
- Dividers: cool light grey.
- Dark theme: deep slate surfaces with accessible text and semantic accents.

Use semantic color tokens and verify contrast. Do not rely on color alone to distinguish income, expense, warning, or sync state.

## Typography
Use a highly legible sans-serif. Tabular numerals for balances, amounts, and chart labels. Currency symbols and values must remain readable in RTL and narrow widths. Use locale-aware formatting, not manually concatenated currency strings.

## Layout
Dashboard prioritizes one clear financial summary and quick actions. Transaction rows show category icon, title, date/account, and amount. Forms use clear sections and numeric keypad-friendly amount input. Charts are simple, labelled, and accompanied by accessible summaries. Budget progress uses labels and values, not color alone.

## Motion
Use brief transitions for adding a transaction, updating a budget bar, and confirming export/sync. No celebratory confetti for spending. Avoid continuous chart animation. Respect reduced-motion preference.

## Interaction
- Add Expense and Add Income are distinct, obvious actions.
- Amount field is prominent and supports decimal/currency conventions.
- Destructive actions require confirmation and offer undo where practical.
- Sync status always uses text plus icon.
- Sensitive balances can optionally be hidden from casual view.

## Accessibility
Large text support, screen-reader summaries for charts, meaningful focus order, adequate touch targets, high contrast, RTL mirroring, and reduced-motion behavior.
