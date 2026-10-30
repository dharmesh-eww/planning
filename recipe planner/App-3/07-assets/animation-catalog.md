# Animation and Asset Catalog — App-3

## Motion identity
App-3 uses more expressive motion than App-1 and App-2, but every animation must clarify a state, teach an interaction, or make completion legible. The core app must remain fully usable without Lottie.

## Suggested Lottie discovery links
These are candidate discovery pages, not approved or bundled assets:
- [Cooking animation](https://lottiefiles.com/free-animation/cooking-ILTK2Njxtd)
- [Preparing food](https://lottiefiles.com/free-animation/preparingfood-h487unBrjJ)
- [Preparing food state animation](https://lottiefiles.com/free-animation/preparing-food-nIU3mvESuC)
- [Cooking animation](https://lottiefiles.com/free-animation/cooking-animation-Pt0qVDpNxK)

Before use, inspect the actual JSON/dotLottie file, preview it on-device, verify the current licence and attribution obligations, check file size, rendering performance, and compatibility with the selected Flutter player. Do not assume a free preview means unrestricted commercial use.

## Animation shortlist
| Asset concept | Placement | Purpose | Fallback |
|---|---|---|---|
| Hand-drawn sprig reveal | Splash | Brand introduction | Static sprig |
| Ingredient character/line-art sequence | Onboarding | Explain app flow | Static ingredient illustration |
| Recipe card entering a planner slot | Add-to-plan success | Show destination | Immediate card insertion |
| Ingredient check stroke | Grocery completion | Confirm check-off | Static checked state |
| Small simmering pot | Empty recipe/collection state | Encourage discovery | Static illustration |
| Content leaf/page update | Content update success | Confirm refresh | Text + check icon |
| Timer completion | Timer | Clear completion signal | Static completion icon and sound/haptic if enabled |

## Motion rules
- Use Lottie primarily in onboarding, empty states, and meaningful success states.
- Do not use Lottie in cooking mode or timer countdown.
- No infinite decorative animation on every screen.
- Never delay interaction until an animation completes.
- Respect system reduced-motion preference and provide an in-app motion setting.
- Stop off-screen animations and avoid unnecessary battery/network use.
- Bundle selected files locally so offline states do not lose their illustration.
- Provide static alternatives and ensure semantic labels communicate the same information.

## Accessibility reference
W3C notes that interaction-triggered animation should be disableable unless essential: [WAI — Animation from Interactions](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions). Also consider [MDN reduced-motion guidance](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Media_queries/Using_for_accessibility).

## Licence checklist
- Confirm exact asset author and licence for the downloaded file.
- Confirm commercial app use, modification, redistribution, and attribution conditions.
- Keep a local licence/attribution record.
- Do not bundle assets whose licence is unclear.
- Recheck licence before release.

## Status
No actual Lottie JSON/dotLottie files are committed in this planning directory. The links are research candidates only.
