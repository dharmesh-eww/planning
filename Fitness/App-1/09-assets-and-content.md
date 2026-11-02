# Form & Flow — PNG Asset Manifest and Content Rules

## Non-negotiable asset policy
Form & Flow is an image-led fitness app. The PNG files listed here are required implementation assets. A colored box, emoji, Material icon, remote URL placeholder or repeated generic thumbnail does not satisfy an image requirement. The app must bundle its baseline images so the experience works offline.

## Asset production status
This manifest defines the approved filenames, dimensions, subjects and usage. Assets must be added to the repository at the exact paths below before the corresponding UI screen is marked complete. Do not mark a file as available until the PNG exists and has been visually reviewed.

## Brand and onboarding
| File | Target size | Subject / usage |
|---|---:|---|
| `assets/images/brand/ff-app-mark.png` | 512×512 | Original Form & Flow brand mark, transparent background |
| `assets/images/onboarding/ff-onboarding-athlete.png` | 1200×1600 | Editorial athlete portrait/action photograph, blue/cobalt environment |
| `assets/images/onboarding/ff-onboarding-equipment.png` | 1200×900 | Home/gym equipment still-life with clear silhouettes |

## Dashboard and plan covers
| File | Target size | Subject / usage |
|---|---:|---|
| `assets/images/hero/ff-hero-today-strength.png` | 1600×900 | Athlete performing a recognizable strength movement; dashboard hero |
| `assets/images/plans/ff-plan-strength.png` | 900×700 | Strength training plan cover |
| `assets/images/plans/ff-plan-cardio.png` | 900×700 | Cardio plan cover |
| `assets/images/plans/ff-plan-mobility.png` | 900×700 | Mobility plan cover |
| `assets/images/plans/ff-plan-beginner.png` | 900×700 | Beginner-friendly full-body plan cover |

## Exercise demonstration library
Every exercise must map to a distinct image that accurately shows the named movement. Initial minimum set:
| File | Target size | Subject |
|---|---:|---|
| `assets/images/exercises/ff-exercise-push-up.png` | 900×900 | Correct push-up start/mid position |
| `assets/images/exercises/ff-exercise-squat.png` | 900×900 | Bodyweight squat side view |
| `assets/images/exercises/ff-exercise-dumbbell-press.png` | 900×900 | Dumbbell chest press |
| `assets/images/exercises/ff-exercise-forward-lunge.png` | 900×900 | Forward lunge side/front three-quarter view |
| `assets/images/exercises/ff-exercise-plank.png` | 900×900 | Forearm plank alignment |
| `assets/images/exercises/ff-exercise-glute-bridge.png` | 900×900 | Glute bridge position |
| `assets/images/exercises/ff-exercise-jumping-jack.png` | 900×900 | Jumping jack movement |
| `assets/images/exercises/ff-exercise-bird-dog.png` | 900×900 | Bird-dog position |

## Instructional illustrations and muscle groups
| File | Target size | Subject / usage |
|---|---:|---|
| `assets/images/muscles/ff-muscles-front.png` | 900×1200 | Clear anterior muscle-group diagram |
| `assets/images/muscles/ff-muscles-back.png` | 900×1200 | Clear posterior muscle-group diagram |
| `assets/images/muscles/ff-muscles-upper-body.png` | 900×900 | Upper-body target area illustration |
| `assets/images/muscles/ff-muscles-lower-body.png` | 900×900 | Lower-body target area illustration |

## Empty states, progress and feedback
| File | Target size | Subject / usage |
|---|---:|---|
| `assets/images/states/ff-empty-today.png` | 900×700 | Friendly athlete preparing to start |
| `assets/images/states/ff-empty-history.png` | 900×700 | Open training journal with subtle fitness props |
| `assets/images/states/ff-empty-measurements.png` | 900×700 | Neutral measuring tape/record illustration |
| `assets/images/states/ff-completion-celebration.png` | 900×700 | Restrained celebratory athlete illustration |
| `assets/images/states/ff-goal-milestone.png` | 900×700 | Goal milestone artwork, no body-shaming imagery |
| `assets/images/states/ff-rest-breathing.png` | 900×700 | Calm breathing/rhythm illustration |

## Custom category artwork
| File | Target size | Subject |
|---|---:|---|
| `assets/images/categories/ff-category-strength.png` | 512×512 | Strength category |
| `assets/images/categories/ff-category-cardio.png` | 512×512 | Cardio category |
| `assets/images/categories/ff-category-mobility.png` | 512×512 | Mobility category |
| `assets/images/categories/ff-category-recovery.png` | 512×512 | Recovery category |

## Visual consistency and technical requirements
- PNG, sRGB, optimized for mobile; transparent backgrounds only where useful.
- Keep a consistent editorial photography style: natural light, uncluttered backgrounds, realistic anatomy, inclusive subjects and accurate equipment.
- Exercise images must depict the named movement and show safe, plausible posture. Do not use AI anatomy that is visibly malformed.
- Use the same crop and subject scale across exercise thumbnails.
- Keep focal subjects inside a central safe area so cards can crop responsively.
- Provide 1x source at the dimensions above; Flutter may decode/cache resized variants.
- Do not bake text, buttons, logos from third parties or UI controls into photography.
- Add source, creator, license, attribution requirement and review status to `assets/ASSET_CREDITS.md`. Do not use unlicensed scraped images.
- For remote GitHub catalog updates, images are public content only; personal workout data must never be uploaded.
- Provide local fallback PNGs for every network-distributed catalog image.

## Flutter integration contract
- Register `assets/images/` in `pubspec.yaml`.
- Create a typed asset catalog (for example `FitnessAssets.exercisePushUp`) rather than scattering raw paths.
- Use `Image.asset` with meaningful semantics, stable aspect ratios and explicit `BoxFit`.
- Use `errorBuilder` only as a final defensive fallback; it must not conceal missing required assets during development.
- Add widget tests that assert key dashboard and exercise-detail image widgets resolve to bundled assets.
- Add an asset audit that checks every manifest path exists before release.

## Definition of done
The manifest is not fulfilled by placeholders. All required PNGs must exist, be reviewed, be referenced by the relevant screen, load offline, and have documented licensing before the app is considered visually complete.
