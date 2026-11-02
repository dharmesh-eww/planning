# Visual Direction — Form & Flow

## Concept
Bright Athletic Editorial: a premium, image-led training journal for everyday athletes. The interface must feel like a finished consumer fitness product, not a wireframe made from cards and generic icons.

## Palette
Canvas #F7F8FA; surface #FFFFFF; ink #17202B; secondary #687381; cobalt #315FEA; progress lime #C8F169; success #187A55; caution #B66A22; error #C64F4F. Use semantic colors with labels and accessible contrast.

## Typography
Use a clear geometric sans for headings and a highly legible body face. Use tabular numerals for sets, reps, durations and measurements. Maintain a strong hierarchy; large numbers are reserved for meaningful metrics.

## Layout
Use an 8pt spacing system, 20–24pt page gutters and restrained 16–22pt radii. Avoid dense dashboards, excessive gradients, glassmorphism and decorative metric rings. Keep active-workout controls legible at arm's length.

## Required image-led UI
Images are a first-class part of the design, not optional decoration:
- Today dashboard: wide photographic workout hero with a real exercise subject; overlay only short title and CTA.
- Plan library: image-led plan cards with distinct strength, mobility, cardio and beginner artwork.
- Exercise library: every exercise row/card has its own relevant thumbnail; no icon-only exercise catalogue.
- Exercise detail: large demonstration image, secondary muscle-group illustration and numbered written instructions.
- Workout builder and active workout: current movement image remains visible above set controls; use a smaller thumbnail for queued movements.
- Empty states: custom illustrations for no plans, no history and no measurements.
- Goals and completion: custom achievement/progress artwork used sparingly.
- Onboarding: original fitness lifestyle illustration/photo panels, not generic colored blocks.

## Iconography
Do not use Flutter Material Icons as the primary visual language or as substitutes for imagery. Use a consistent custom PNG icon family for feature/category illustrations and a small, consistent outline icon set for utility actions. Utility icons must remain secondary to text labels and accessible semantics. Never use a PNG icon where a meaningful exercise photo or illustration is required.

## Components
Image-led workout hero, image plan card, thumbnail exercise row, exercise detail media panel, muscle-group illustration, weekly activity strip, metric tile, set-entry grid, sticky session controls, timer sheet, chart with text summary and illustrated empty state.

## Accessibility
Dynamic type, touch targets of at least 48 logical pixels, semantic colors, chart legends, reduced motion, screen-reader labels, kg/lb and km/mi preferences, RTL-ready layouts. Every image requires meaningful alternative text or decorative semantics.

## Image direction
Use original or properly licensed exercise photography/illustration. Accurate posture and equipment, inclusive representation, uncluttered backgrounds, consistent lighting and camera angles. Keep the subject clear at small thumbnail sizes. Never rely on imagery alone for exercise instructions.

## Acceptance gate
A screen is not ready for approval if a required image is missing, replaced by a Material icon, represented by an empty colored container, or shown as a broken network image. Bundled fallback images must render offline.