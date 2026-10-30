# Screen 13 — Timer

## Layout
Large tabular countdown; timer label and source step; start/pause/resume/reset; optional preset durations; clear completion state.

## Behavior
Timer should remain logically accurate across app navigation and backgrounding within platform capabilities. If notifications are permitted, notify at completion; otherwise retain an in-app completion state. Multiple timers are optional; if supported, each has a distinct label.

## Motion
A restrained progress ring may update without distracting movement. No pulsing/flashing. Reduced motion uses a static progress indicator.

## Acceptance
No ads. Time is legible at a glance. Explain notification limitations without blocking timer use. Controls expose state to assistive technology.
