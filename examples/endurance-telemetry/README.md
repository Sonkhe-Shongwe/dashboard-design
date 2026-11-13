# Endurance Race Telemetry

**Open `index.html` in a browser from a local checkout.** Select Lap 18, 24 or 12 to compare with the fixed Lap 12 reference. Lap time, top speed, sector deltas, the speed trace and the summary update together.

![Generated hero artwork of a graphite endurance race car in a night pit lane](hero.webp)

## Design decisions

- The hero establishes the subject. Negative space keeps the title readable and the dashboard reserves its next section for the primary comparison.
- Charcoal surfaces, condensed numerals and a restrained yellow accent establish the theme. One outline icon family identifies repeated metric roles.
- The selected trace is solid and the reference is dashed. Sector bars diverge from zero and keep their signed values visible. A lower lap time is a gain.

## Data and verification

The vehicle, image and telemetry are illustrative. The image was generated for this study. Lap times are the sums of the three simulated sectors, and top speeds come from the selected lap’s simulated trace. The speed samples use a common distance grid.

| Selected lap | Lap time | Difference vs Lap 12 | Top speed |
|---|---:|---:|---:|
| 18 | 1:44.682 | −0.614 s | 318 km/h |
| 24 | 1:45.508 | +0.212 s | 315 km/h |
| 12 | 1:45.296 | 0.000 s | 312 km/h |

The selection logic and calculated outputs were checked in a JavaScript harness. The study is a browser prototype. [Endurance Dark theme starter](../../themes/endurance-dark.json)
