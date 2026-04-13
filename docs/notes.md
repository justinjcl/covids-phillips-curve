# Project Notes

## Research Question
Did the relationship between unemployment and inflation change after COVID? Specifically, does the traditional Phillips Curve — which predicts a negative relationship between unemployment and inflation — still hold in the post-COVID period?

## Data Decisions

**Why 2015 to 2025?**
Chosen to capture a reasonable pre-COVID baseline while including the full COVID shock and recovery period. Starting earlier would add data but the post-2008 recovery period has its own distortions that could complicate the analysis.

**Why monthly data?**
FRED provides monthly data for both series. Monthly gives more observations than quarterly or annual and captures short term movements better. Tradeoff is more noise in the relationship.

**Why this inflation measure (CPALTT01USM657N)?**
OECD Consumer Price Index, year over year percent change. Chosen because it is a standard comparable measure. Alternative would be PCE which the Fed actually targets but CPI is more widely cited and understood.

**Missing value in unemployment (Oct 2025)**
Row 129 had no unemployment rate for October 2025. Dropped because the data had not been published at time of download. Only one row affected at the end of the series so dropping was cleaner than imputing.

**Why split at March 2020 / June 2020?**
March 2020 is when COVID lockdowns began in the US. June 2020 chosen as the post-COVID start to skip the acute shock period where both variables behaved abnormally. Including the shock months in either regression would distort the coefficients.

## Analysis Decisions

**Why OLS regression?**
Simple linear regression is appropriate for testing the direction and significance of a bivariate relationship. The Phillips Curve is traditionally estimated with OLS so this is consistent with the literature.

**Why separate regressions for each period?**
Running one regression across the full period would give an average relationship that masks any structural change. Splitting allows direct comparison of the relationship before and after COVID.

## Key Findings

**Pre-COVID regression (Jan 2015 to Feb 2020, n=61)**
- Coefficient: +0.025 (positive, not negative as Phillips Curve predicts)
- P-value: 0.635 (not statistically significant)
- R-squared: 0.004 (unemployment explains almost none of inflation variance)

**Post-COVID regression (Jun 2020 to Sep 2025, n=45)**
- Coefficient: ~0.001 (essentially zero)
- P-value: 0.98 (completely insignificant)
- R-squared: ~0

**Interpretation**
The simple two-variable Phillips Curve showed no statistically significant relationship in either period. This does not necessarily mean the relationship does not exist — it likely means the model is too simple. Inflation is influenced by supply shocks, oil prices, fiscal policy, and monetary policy, none of which are captured here. A more complete model would include additional variables. The visual time series plot does show the COVID shock clearly — unemployment spiked while inflation dropped in early 2020, then unemployment recovered while inflation surged in 2021-2022, consistent with the narrative of stimulus-driven demand inflation.

## Limitations
- Only two variables — a multivariate model would give more complete results
- Monthly data is noisy — annual averages might show cleaner relationships
- The post-COVID period is still short (45 observations) — more data over time may change results
- No lag structure tested — unemployment today may affect inflation 6 to 12 months later

## Next Steps
- Add oil prices or a supply shock variable from FRED
- Test lagged relationships — does unemployment at time t predict inflation at t+6?
- Compare results using PCE instead of CPI
- Consider a rolling regression to show how the coefficient changes over time
