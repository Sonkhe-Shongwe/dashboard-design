# Credit Portfolio design study

**Open `index.html` in a browser from a local checkout.** Try **2023 → Q4**, open **Cohort coverage**, then clear the filters. The selected cohort carries between pages while the labelled full-sample comparison stays fixed.

## Design decisions

- The light finance layout puts the eligible population beneath the headline rate. This keeps the figure and its denominator together when the selection changes.
- Blue and teal consistently identify 2022 and 2023. Both arrears charts use the same scale. Coverage charts use independent labelled scales to accommodate their different measures.
- The annual matrix provides exact values and totals. The browser prototype groups other coverage exclusions for compact display. The proposed Power BI matrix describes the full exclusion breakdown.

## Data and verification

The demo embeds eight published quarterly aggregates from the Credit Portfolio project, derived from Freddie Mac’s 2022 and 2023 U.S. mortgage samples. The research plan explains eligibility, scope and publication boundaries. [Published aggregate CSV](https://github.com/Sonkhe-Shongwe/credit-portfolio-risk-analysis/blob/main/power-bi/month_12_cohorts.csv) · [Research plan](https://github.com/Sonkhe-Shongwe/credit-portfolio-risk-analysis/blob/main/docs/RESEARCH_PLAN.md)

With **2023 Q4** selected, the account arrears rate is 0.5856% (63 of 10,759 eligible loans). On the coverage page, eligibility is 86.07% and the voluntary payoff rate is 13.58%. Clearing filters restores the full-sample view. These selections and values were checked in a JavaScript harness.

[Full report design specification](https://github.com/Sonkhe-Shongwe/credit-portfolio-risk-analysis/blob/e2a1dbf299ad0a7ca582d05a2ba84cc38e43a4b9/docs/DASHBOARD_DESIGN.md) · [Portfolio Light theme starter](../../themes/portfolio-light.json)
