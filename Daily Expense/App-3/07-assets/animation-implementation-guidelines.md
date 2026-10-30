# Animation Implementation Guidelines

Use a maintained compatible Lottie Flutter package after checking current compatibility and license. Reusable wrapper accepts asset key, mode (once/loopWhileActive/paused), trigger version, reduced-motion flag, semantic label and fallback.

Lottie is presentation-only; domain logic never waits for completion. Lazy load, pause off-screen/covered routes, dispose controllers, handle invalid JSON and fallback to static icon/illustration. Do not replay on unrelated rebuild. Validate size/layers/frame rate, offline availability, accessibility and low-end device performance.
