# From design to Power BI

## 1. Brief and prototype

Complete the [design brief](../templates/design-brief.md). Use representative data and include the longest plausible labels, a busy state, and an empty state. Wireframe the default view first, then show the sequence from a headline to its evidence. Explore an editorial direction when the subject benefits from imagery and a dense analytical direction when comparison and lookup dominate the task.

For a Figma handoff, specify the report canvas, grid, text roles, series mappings and layer order. Export only useful assets such as the background image and icon set. Keep value labels, filters and focusable controls editable in the report. [Figma-to-Power-BI workflow](https://www.linkedin.com/posts/zsolt-szabo-bln_powerbi-dataviz-reportdesign-activity-7422235917471543296-WuRV)

## 2. Assemble the report

| Design element | Power BI approach | Verify |
|---|---|---|
| Palette and typography | Start with a [theme JSON](../themes/README.md). Apply explicit visual settings for exceptions such as the main KPI or a fixed comparison scale. | Import the theme, review the report at Fit to Page, and check which formatting has been overridden. [Theme documentation](https://learn.microsoft.com/en-us/power-bi/create-reports/report-themes-create-custom) |
| Imagery | Use an image visual for a hero, portrait or reference layer. Use image fields for supported dynamic table, matrix or slicer cases. | Check crop, text contrast, external image access where applicable, alt text and appearance after publish. [Image visual](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-image-visual) · [Images in tables, matrices and slicers](https://learn.microsoft.com/en-us/power-bi/create-reports/power-bi-images-tables) |
| KPI cards | Use native cards and reference labels for a baseline, count or signed delta. Keep the unit near the value. | Compare the card with source totals and confirm the label uses the same filter context. [Card visual](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-card) |
| Page controls | Use page navigators, buttons or bookmarks. Set selected states and decide which filters carry across pages. | Test keyboard access, filter sync, clear/reset and return navigation. [Navigators](https://learn.microsoft.com/en-us/power-bi/create-reports/button-navigators) · [Slicers](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-slicers) · [Clear all slicers](https://learn.microsoft.com/en-us/power-bi/create-reports/buttons-apply-all-clear-all-slicers) |
| Custom analytical charts | Start with a native visual that answers the question. Use Deneb when a specific mark, layered chart or annotation justifies the custom specification. | Check selection, tooltip and accessibility behaviour in the intended viewing environment. [Deneb](https://deneb.guide/) |
| HTML or SVG components | Consider a compatible custom visual for a specific need such as a compact KPI comparison. Keep the source specification and data logic reviewable. | Check availability in the target tenant and verify selection, keyboard, export and publication behaviour for that visual. [Example build](https://www.linkedin.com/posts/borys-kuznietsov-712ab7312_powerbi-report-design-activity-7464933737638744064-_283) |

## 3. Validate the numbers and behaviour

- Recalculate a default total and at least one representative filtered state independently. For ratios, sum the numerators and denominators before dividing. Keep a real zero distinct from a missing or undefined value.
- Confirm cross-filtering and cross-highlighting are intentional. Check every control in its default, selected and cleared states. Label insights with their scope if they stay fixed when a filter changes.
- Inspect visual order, visible focus, alt text and chart legends. Check main values, matrix totals and text at Fit to Page. Check mobile, service or PDF only for the delivery surfaces in the brief.
- If interactions are slow, use Performance Analyzer to identify the specific visuals or queries involved. Record the build version, environment, test selection and visible result. [Accessibility](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports) · [Performance Analyzer](https://learn.microsoft.com/en-us/power-bi/desktop-performance-analyzer)

Use the [review checklist](../templates/review-checklist.md) to capture acceptance evidence. A browser prototype can demonstrate composition and intended behaviour. Desktop and published report checks establish what the Power BI implementation actually does.
