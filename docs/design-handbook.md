# Dashboard design handbook

## Start with the decision

Write the audience, the decision, the current context and the evidence needed. For a practice telemetry dashboard, the decision is which sector to investigate after a slower lap. The opening view needs the selected lap, a fixed reference, a signed lap delta and sector-level evidence. A portfolio risk analyst instead needs the population, the comparison period and a route from headline rates to their denominators.

## Arrange the page

1. Put the title, scope and high-use controls in predictable places. Give navigation and filters different visual treatments.
2. Make one metric or chart dominant through position, size and contrast. Group related items by proximity and use consistent alignment.
3. Put the next piece of evidence beside or beneath the headline. Use a wide chart for the main comparison and a smaller table or chart for explanation. Use equal panels and a shared scale when panels are meant to be compared directly.
4. Use a detail table, tooltip or drillthrough for exact values. Keep essential scope, findings and controls visible before hover.
5. For a 1280 px desktop concept, trial 24 px outer gutters, 16 px gaps and 12–16 px internal padding. Fit the largest realistic label and the intended screen before finalising dimensions. Use consistent spacing across pages.

## Specify the visual system

| Element | Design decision | Common failure |
|---|---|---|
| Typography | Use one readable family for the report and optionally a display family for headlines. Define roles for title, KPI value, visual heading, label and note. Right-align comparable numbers and use tabular digits when available. | Every text role has similar weight, chart labels become too small at Fit to Page, or currency and rate formats change across views. |
| KPI cards | Combine a concise label, value and unit with a useful denominator, time period, target or signed variance. Give the primary KPI a distinct type size or quiet fill. | Four equally loud cards, detached arrows, vague comparisons, or red and green sign rules that misstate business meaning. |
| Shapes | Use cards to group content, an underline for the current tab, chips for short labelled states, and bars or dots when shape or length encodes data. | Ornamental frames compete with the data, or an unlabeled shape acts like a hidden button. |
| Icons | Use one family, consistent stroke weight, and a repeatable size. Pair icons with labels for actions, important states and unfamiliar meanings. | Mixed filled and outline sets, large decorative circles, emoji where a consistent symbol is needed, and icon-only navigation with ambiguous meaning. |
| Imagery | Use a hero image to establish the subject, a portrait to identify an entity, or a domain image as an analytical reference layer. Keep a predictable crop and protect text contrast. Record creator, origin and usage terms where applicable. | Low-contrast text on a busy photo, imagery that consumes the analysis area, or a screenshot of a chart standing in for live values. |
| Colour | Define canvas, surfaces, text, muted text, boundaries, identity accents, series and semantic states. Repeat series mappings across pages. Reinforce meaning with text, marker shape, line style or order. | Colour shifts meaning across pages, too many saturated accents, or a red/green-only signal. |
| Data state | Define default, selected, cleared, no data, zero, missing and error states. Surface the reference period and active filter scope. | A filtered insight still describes the full sample without a scope label, or an undefined rate appears as zero. |

For WCAG AA contrast, target at least 4.5:1 for normal text, 3:1 for large text as defined by the criterion, and 3:1 for essential graphical or control boundaries against adjacent colours where applicable. Verify the final design on the actual backgrounds, including the weakest part of any image overlay. Use visible focus, meaningful alt text and keyboard-operable controls. [W3C text contrast](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) · [Non-text contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html) · [Use of colour](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html)

## Choose the chart for the comparison

| Question | Default visual | Check |
|---|---|---|
| Which category is largest? | Sorted horizontal bars | Start the value axis at zero and use clear category labels. |
| How does a measure move across time or distance? | Line chart | Show units and comparison basis. Keep meaningful gaps where observations are missing. |
| How do matched groups compare? | Grouped bars, dots or shared-scale small multiples | Preserve group order and use a common scale when magnitudes are meant to be comparable. |
| Where did we gain or lose versus a reference? | Diverging bars or a signed variance table | Align at zero and label the reference, sign and units. |
| How does a total break into components? | Stacked bars or a labelled table | Use meaningful part-to-whole categories and provide exact values where they matter. |
| What are the exact values? | Table or matrix | Align decimals and currency, check totals, and ensure key rows fit. |
| Where are points distributed in a real space? | Scatter on a meaningful spatial reference or a map | Confirm the data supports the geometry and geographic grain. |

[Financial Times Visual Vocabulary](https://github.com/Financial-Times/chart-doctor/tree/main/visual-vocabulary) · [IBCS Standards](https://www.ibcs.com/ibcs-version-2-0/)

## Evaluate the interaction

Pick one exploratory task that represents how the dashboard should be used. For telemetry, change the lap and verify that the headline time, speed trace and sector comparison update against the same baseline. For financial comparisons, carry the selected cohort across pages and verify that clearing filters restores the totals. Show selected and focus states, document which visuals filter which, and verify the result using the underlying figures.

For portfolio presentation, capture the initial view and one meaningful selected state. A short reveal can show the opening view, one interaction and the insight it uncovers. Review both screens at the size they will be seen.
