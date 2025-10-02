# Discrete and Nonlinear Models

This chapter extends regression techniques to nonlinear settings, emphasizing discrete choice and count data models.

## Learning Objectives

- Understand likelihood-based estimation for binary, multinomial, and ordered outcomes.
- Interpret marginal effects and predicted probabilities from nonlinear models.
- Compare logit, probit, and complementary log-log link functions.
- Model count data using Poisson, negative binomial, and zero-inflated specifications.

## Outline

1. **Binary Choice Models**: logit, probit, link functions, marginal effects.
2. **Multinomial and Ordered Responses**: model structure, estimation, interpretation strategies.
3. **Limited Dependent Variables**: Tobit models, sample selection, corner solutions.
4. **Count Models**: Poisson, negative binomial, zero-inflated/hurdle models.
5. **Model Evaluation**: likelihood ratio tests, pseudo R², information criteria, ROC/PR curves.
6. **Computation**: optimization routines, numerical stability, gradient checks.

## Resources

- Notebook demonstrations comparing logit and probit predictions.
- Case studies using transportation mode choice and healthcare utilization datasets.
- Utility scripts for computing marginal effects and elasticities.

## Exercises

- Derive the score and Hessian for the logit model and implement Newton-Raphson updates.
- Fit count models to synthetic data with over-dispersion and interpret coefficients.
- Evaluate classification performance using ROC curves and confusion matrices.
