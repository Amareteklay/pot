# Regression Analysis

This chapter formalizes linear regression, explores diagnostics, and demonstrates robust estimation strategies.

## Learning Objectives

- Derive the ordinary least squares (OLS) estimator and understand its assumptions.
- Conduct inference on regression coefficients and predictions.
- Diagnose model misspecification using residual analysis and specification tests.
- Apply remedial measures such as robust standard errors and transformations.

## Outline

1. **Simple Linear Regression**: OLS derivation, interpretation, goodness-of-fit.
2. **Multiple Regression**: matrix formulation, partial effects, multicollinearity.
3. **Assumption Checks**: Gauss–Markov conditions, heteroskedasticity, autocorrelation.
4. **Diagnostics and Remedies**: residual plots, RESET test, robust/clustered standard errors.
5. **Model Selection**: information criteria, cross-validation, shrinkage introductions.
6. **Prediction and Forecasting**: interval estimates, out-of-sample evaluation.

## Resources

- Annotated derivations in LaTeX/Markdown.
- Example notebooks (`ols_basics.ipynb`, `diagnostics.ipynb`) with simulated and real data.
- Utility functions for regression summaries in `utils/regression_tools.py` (planned).

## Exercises

- Compute OLS estimates manually and with software, comparing results.
- Design diagnostic checks for given datasets and propose fixes.
- Evaluate predictive performance using train/test splits or cross-validation.
