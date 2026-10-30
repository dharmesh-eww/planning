# Animation Implementation Guidelines

Use a maintained compatible Lottie Flutter package after verifying current support and license. Wrap playback in reusable presentation component with asset key, mode (once/loopWhileActive/paused), trigger version, reduced-motion flag, localized semantic description and fallback icon.

Animation is presentation-only; domain logic never awaits completion. Load lazily, pause when route is covered, dispose controllers, catch decode failures, and show fallback. Do not replay on unrelated rebuilds. Validate asset size/layers/frame rate, offline availability, semantics, reduced motion and memory/frame performance.
