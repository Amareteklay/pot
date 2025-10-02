# Foundations of Probability and Statistics

This chapter builds the probabilistic and statistical foundations that underpin every later section of POT. Treat these notes as both a learning guide and a reference while working through data analysis projects.

## Learning Objectives

- Understand probability axioms, conditional probability, and Bayes' rule.
- Distinguish between discrete and continuous random variables and their distributions.
- Master expectation, variance, covariance, and transformations of random variables.
- Develop intuition for sampling distributions, estimation, and hypothesis testing.

## 1. Probability Basics

### Sample Spaces and Events
- A *sample space* \(\Omega\) contains all possible outcomes of an experiment; events are subsets of \(\Omega\).
- The sigma-algebra \(\mathcal{F}\) is a collection of events closed under complements and countable unions. We typically assume \(\Omega, \mathcal{F}, P\) forms a probability space.
- Probability measure \(P\) satisfies Kolmogorov axioms: non-negativity, normalization \(P(\Omega)=1\), and countable additivity for disjoint events.

### Counting Rules
- Product rule: number of ordered sequences is the product of choices at each step.
- Permutations: \(n!\) arrangements; ordered k-permutations: \(n!/(n-k)!\).
- Combinations: \(\binom{n}{k}\) unordered subsets; with replacement, use stars-and-bars \(\binom{n+k-1}{k}\).
- Conditional counting: restrict to an event, then count outcomes within it.

### Conditional Probability and Independence
- Conditional probability: \(P(A \mid B) = P(A \cap B) / P(B)\) for \(P(B) > 0\).
- Law of total probability: if \(\{B_i\}\) partitions \(\Omega\), then \(P(A) = \sum_i P(A \mid B_i) P(B_i)\).
- Bayes' rule: \(P(B_j \mid A) = \frac{P(A \mid B_j)P(B_j)}{\sum_i P(A \mid B_i) P(B_i)}\).
- Independence: events A and B independent if \(P(A \cap B) = P(A)P(B)\); extend to collections when every finite subset multiplies.

### Common Pitfalls
- Conditioning on zero-probability events is undefined unless using limits (regular conditional probability).
- Independence is stronger than mutual exclusivity; disjoint events cannot be independent unless one has zero probability.
- In combinatorics, carefully distinguish between ordered and unordered selections and whether sampling is done with replacement.

## 2. Random Variables

### Definitions
- A random variable (RV) is a measurable function from \(\Omega\) to \(\mathbb{R}\). Discrete RVs take countable values; continuous RVs have densities with respect to Lebesgue measure.
- Distribution of X captured by cumulative distribution function (CDF) \(F_X(x) = P(X \le x)\).

### Discrete RVs
- Probability mass function (pmf): \(p_X(x) = P(X = x)\). Ensure \(\sum_x p_X(x) = 1\).
- Expectation: \(E[X] = \sum_x x p_X(x)\); variance: \(Var(X) = E[X^2] - (E[X])^2\).
- Typical distributions: Bernoulli, Binomial, Poisson, Geometric, Negative Binomial. Capture support, pmf, mean, variance in a quick table for review.

### Continuous RVs
- Probability density function (pdf) integrates to 1. For an interval, \(P(a \le X \le b) = \int_a^b f_X(x) dx\).
- Expectation: \(E[X] = \int x f_X(x) dx\); variance defined analogously.
- Common families: Uniform, Exponential, Gaussian, Gamma, Beta, Pareto. Recognize parameterizations (scale vs rate, shape vs concentration).

### Moment Generating and Characteristic Functions
- Moment generating function (mgf): \(M_X(t) = E[e^{tX}]\), exists near zero, encodes all moments via derivatives.
- Characteristic function (cf): \(\phi_X(t) = E[e^{itX}]\) always exists and uniquely determines distribution.
- Use mgfs to sum independent RVs: mgf of sum equals product of individual mgfs.

### Transformations
- For Y = g(X) with invertible monotone g, density transforms as \(f_Y(y) = f_X(g^{-1}(y)) |d g^{-1}(y)/dy|\).
- For non-invertible g, partition the domain and sum contributions.
- Expectation of transformations: \(E[g(X)] = \sum_x g(x) p_X(x)\) or \(\int g(x) f_X(x) dx\).

## 3. Multivariate Distributions

### Joint, Marginal, and Conditional Distributions
- Joint pmf/pdf \(f_{X,Y}(x, y)\) integrates or sums to 1. Marginals retrieved via summing/integrating over the other variable.
- Conditional density: \(f_{X\mid Y}(x \mid y) = f_{X,Y}(x, y) / f_Y(y)\) provided denominator nonzero.
- Independence when joint factorizes: \(f_{X,Y}(x, y) = f_X(x) f_Y(y)\).

### Covariance Structure
- Covariance \(Cov(X, Y) = E[(X - E[X])(Y - E[Y])]\); correlation \(\rho_{XY} = Cov(X,Y)/(\sigma_X \sigma_Y)\).
- Covariance matrix \(\Sigma\) for vector \(\mathbf{X}\) captures pairwise covariances; symmetric and positive semi-definite.
- Law of total covariance: \(Cov(X, Y) = E[Cov(X, Y \mid Z)] + Cov(E[X \mid Z], E[Y \mid Z])\).

### Conditioning and Projection
- Conditional expectation \(E[X \mid Y]\) is the best mean-square predictor of X using Y.
- Law of iterated expectations: \(E[ E[X \mid Y] ] = E[X]\).
- Use conditional expectation for variance decomposition: \(Var(X) = E[Var(X \mid Y)] + Var(E[X \mid Y])\).

### Transformations of Vectors
- For \(\mathbf{Y} = A \mathbf{X} + \mathbf{b}\), means transform linearly and covariances transform as \(A \Sigma_X A^{\top}\).
- For nonlinear transforms, Jacobian determinant arises: if \(\mathbf{Y} = g(\mathbf{X})\) invertible, \(f_{\mathbf{Y}}(\mathbf{y}) = f_{\mathbf{X}}(g^{-1}(\mathbf{y})) |\det J_{g^{-1}}(\mathbf{y})|\).

## 4. Limit Theorems

### Convergence Concepts
- Almost sure convergence: \(P(\lim_{n\to\infty} X_n = X) = 1\).
- Convergence in probability: for all \(\epsilon > 0\), \(P(|X_n - X| > \epsilon) \to 0\).
- Convergence in distribution: CDFs converge at continuity points; implies convergence of expectations for bounded continuous functions.
- Relationships: almost sure implies in probability implies in distribution; converse statements do not hold generally.

### Laws of Large Numbers
- Weak law: sample mean of iid RVs with finite expectation converges in probability to the mean.
- Strong law (Kolmogorov): under mild conditions (finite first moment suffices for iid), sample mean converges almost surely.
- Chebyshev's inequality gives a simple proof of the weak law when variance finite.

### Central Limit Theorem (CLT)
- For iid RVs with finite variance \(\sigma^2\), the normalized sum converges in distribution to Normal(0,1).
- Lyapunov and Lindeberg conditions extend CLT to non-identically distributed sequences.
- Use CLT for approximate inference and constructing asymptotic confidence intervals.

### Slutsky and Delta Methods
- Slutsky's theorem: if \(X_n \to_d X\) and \(Y_n \to_p c\), then \(X_n + Y_n \to_d X + c\), and similarly for products and ratios where defined.
- Delta method: if \(\sqrt{n}(\hat{\theta}_n - \theta) \to_d N(0, \sigma^2)\) and g is differentiable at \(\theta\), then \(\sqrt{n}(g(\hat{\theta}_n) - g(\theta)) \to_d N(0, (g'(\theta))^2 \sigma^2)\).

## 5. Estimation

### Point Estimators
- An estimator \(\hat{\theta}\) is a function of data intended to approximate parameter \(\theta\).
- Bias: \(Bias(\hat{\theta}) = E[\hat{\theta}] - \theta\); unbiased estimators satisfy zero bias.
- Mean squared error (MSE): \(MSE(\hat{\theta}) = Var(\hat{\theta}) + Bias^2\). Lower MSE is desirable.
- Consistency: \(\hat{\theta}_n \to_p \theta\). Asymptotic normality describes limiting distribution after scaling.

### Method of Moments (MoM)
- Equate sample moments \(m_k = \frac{1}{n} \sum X_i^k\) to theoretical moments and solve for parameters.
- Simple to implement, but may produce estimates outside parameter space or with larger variance than alternatives.

### Maximum Likelihood Estimation (MLE)
- Likelihood \(L(\theta) = f(X_1,\ldots,X_n; \theta)\); maximize log-likelihood for numerical stability.
- First-order condition: derivative equal zero; second derivative negative for maxima.
- Regularity yields asymptotic normality: \(\sqrt{n}(\hat{\theta} - \theta_0) \to_d N(0, I(\theta_0)^{-1})\) where \(I\) is Fisher information.
- Invariance: g of MLE is MLE of g(\theta).

### Efficiency and Information Bounds
- Cramer-Rao lower bound (CRLB): variance of unbiased estimator bounded below by inverse Fisher information.
- Efficient estimator achieves CRLB; asymptotically efficient if limit equals bound as n increases.
- Information additivity: for iid data, \(I_n(\theta) = n I_1(\theta)\).

## 6. Statistical Inference

### Confidence Intervals
- Confidence level \(1-\alpha\) indicates long-run coverage probability, not probability about a fixed parameter.
- Use pivotal quantities (e.g., \(\bar{X} \pm z_{\alpha/2} \sigma/\sqrt{n}\)) or asymptotic approximations (Wald interval).
- For small samples from Normal distributions with unknown variance, use t-distribution.
- When exact pivots unavailable, bootstrap intervals provide data-driven approximations.

### Hypothesis Testing
- Null hypothesis \(H_0\) versus alternative \(H_1\). Test statistic T with rejection region or p-value.
- Type I error: rejecting true \(H_0\) with probability \(\alpha\). Type II error: failing to reject false \(H_0\); power equals \(1-\beta\).
- Neyman-Pearson lemma gives most powerful tests for simple hypotheses using likelihood ratio statistic.
- Likelihood ratio, Wald, and score tests share asymptotic \(\chi^2\) distributions under \(H_0\).
- P-values measure extremeness under \(H_0\); adjust using Bonferroni or FDR methods when testing multiple hypotheses.

### Decision-Theoretic View
- Specify loss function L(\theta, a). Risk function is expected loss; minimax and Bayes rules minimize worst-case or posterior expected risk.
- Connects testing and estimation: estimators minimize risk under squared error; tests correspond to 0-1 loss decisions.

## Putting It Together

- Probability rules ensure coherent modeling; revisit counting and conditional probability whenever designing experiments.
- Distributions and moments provide the vocabulary for describing data; maintain a cheat sheet of common families.
- Multivariate tools (conditional expectation, covariance) underpin regression, time series, and modern ML methods.
- Limit theorems justify approximations; know when asymptotics apply and when exact finite-sample tools are needed.
- Estimation and inference build on these foundations; practice deriving estimators and evaluating their properties on simulated datasets.

## Suggested Exercises

1. Prove the law of total probability and Bayes' theorem using set algebra and axioms.
2. Compute expectations and variances for Binomial, Poisson, and Exponential distributions; verify with simulation.
3. Given a bivariate Normal distribution, derive conditional distributions and compute covariances explicitly.
4. Use the weak law and CLT to approximate probabilities for sample means; compare analytical approximations to Monte Carlo results.
5. Derive the MLE for the Exponential rate parameter and compute its Fisher information; compare to method of moments.
6. Design and analyze a hypothesis test for difference in proportions; report Type I error, power, and confidence interval for the effect size.

## Resources

- Worked examples using simulated data in notebooks (`foundations_probability.ipynb`, etc.).
- Quick reference sheets summarizing common distributions and test statistics.
- Links to classic texts (Casella & Berger, Wasserman) in the `references/` directory.

## Practice Tips

- Alternate between theory and computation: after deriving a formula, validate using a quick simulation in Python or R.
- Keep a running glossary of notation; consistent symbols reduce cognitive load in later chapters.
- Revisit these notes before tackling regression assumptions or advanced inference topics to ensure foundational clarity.
