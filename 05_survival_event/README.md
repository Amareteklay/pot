# Survival and Event Analysis

This chapter introduces tools for modeling time-to-event data and recurrent events.

## Learning Objectives

- Understand survival and hazard functions and their relationship.
- Estimate parametric, semi-parametric, and non-parametric survival models.
- Analyze competing risks and recurrent event processes.
- Apply event count analysis (ECA) techniques for high-frequency data.

## Outline

1. **Foundations**: survival/hazard functions, censoring, truncation, Kaplan–Meier estimation.
2. **Cox Proportional Hazards Model**: partial likelihood, proportionality diagnostics, time-varying covariates.
3. **Parametric Models**: exponential, Weibull, log-logistic, accelerated failure time models.
4. **Competing Risks**: cumulative incidence functions, cause-specific hazards.
5. **Recurrent Events and ECA**: gap-time vs. calendar-time models, counting processes, Poisson regression links.
6. **Visualization and Communication**: survival curves, hazard plots, reporting standards.

## Resources

- Notebook examples using clinical trial and customer churn datasets.
- Utility functions for survival curve plotting and baseline hazard extraction.
- Suggested readings from Klein & Moeschberger, Jenkins, and related papers.

## Exercises

- Compare Kaplan–Meier and Nelson–Aalen estimates on censored data.
- Fit Cox and parametric models, checking proportional hazard assumptions.
- Model recurrent events and discuss the interpretation of intensity functions.
