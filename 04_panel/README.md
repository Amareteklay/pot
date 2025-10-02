# Panel Data Econometrics

This chapter tackles longitudinal data methods for analyzing repeated observations on units over time.

## Learning Objectives

- Distinguish between fixed-effects and random-effects estimators.
- Implement difference-in-differences (DiD) and event-study designs.
- Diagnose issues like serial correlation, clustering, and heterogeneous treatment effects.
- Understand identification strategies in panel settings.

## Outline

1. **Panel Data Structure**: notation, within/between variation, data organization.
2. **Fixed Effects Models**: entity, time, and two-way effects; demeaning transformations; incidental parameters.
3. **Random Effects Models**: GLS estimators, Hausman test, variance components.
4. **Difference-in-Differences**: two-way fixed effects, staggered adoption, robustness checks.
5. **Event Studies**: dynamic treatment effects, visualization, pre-trend testing.
6. **Advanced Topics**: clustered standard errors, heterogeneous treatment models, synthetic control introductions.

## Resources

- Templates for panel regressions in R (`fixest`) and Python (`linearmodels`).
- Example datasets: wage panels, policy interventions, and firm-level studies.
- Utility scripts for assembling balanced/unbalanced panels and plotting treatment effects.

## Exercises

- Estimate fixed and random effects models on provided datasets and interpret coefficients.
- Implement a DiD design and assess robustness using placebo and leads/lags tests.
- Visualize event-study coefficients with confidence bands and discuss identification.
