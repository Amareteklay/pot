# Personal Open Textbook (POT)

Personal Open Textbook (POT) is my living, breathing set of notes for learning and teaching statistics and econometrics with an applied, example-driven approach. The project is structured as a textbook, but it is intentionally open, iterative, and hands-on.

## Vision and Goals

- **Explain core ideas clearly.** Each chapter distills concepts into intuitive explanations backed by rigorous derivations.
- **Learn by doing.** Every concept is paired with code, data, and reproducible workflows.
- **Stay extensible.** The notebook-style layout, helper utilities, and data catalog are designed so new topics can be added over time.

## Repository Roadmap

| Phase | Focus | Highlights |
| --- | --- | --- |
| 0. Preface | Why POT exists, how to navigate the book, tooling overview | learning philosophy, contributing guidelines |
| 1. Foundations | Probability and statistics essentials | probability axioms, distributions, estimation, inference |
| 2. Regression | Linear models and diagnostics | OLS derivations, model assumptions, residual analysis |
| 3. Models | Nonlinear and discrete choice models | logit, probit, count models, limited dependent variables |
| 4. Panel | Longitudinal methods | fixed effects, random effects, DiD, event studies |
| 5. Survival & Event | Time-to-event analysis | survival functions, hazard models, event count analysis |
| 6. Advanced | Frontier techniques | instrumental variables, regression discontinuity, GMM, spatial models, machine learning |

Supporting directories:

- `utils/`: helper scripts for simulation, estimation, and visualization.
- `data/`: curated synthetic and cleaned real-world datasets used throughout the book.
- `references/`: annotated bibliographies, textbook notes, and PDFs of key papers.

## Syllabus Snapshot

1. **Preface** – project motivation, study plans, tooling checklist.
2. **Foundations of Probability and Statistics**
   - Describing uncertainty, random variables, distributions.
   - Estimation theory, sampling, hypothesis testing.
3. **Regression Analysis**
   - Simple and multiple linear regression.
   - Gauss–Markov theorem, inference, diagnostics, robustness checks.
4. **Discrete and Limited Dependent Variable Models**
   - Binary choice (logit/probit), ordered/discrete outcomes, count models.
   - Maximum likelihood estimation and interpretation.
5. **Panel Data Econometrics**
   - Fixed and random effects, difference-in-differences, event-study frameworks.
   - Dealing with serial correlation and clustering.
6. **Survival and Event Studies**
   - Duration analysis, hazard/survival functions, competing risks.
   - Event count analysis (ECA) and recurrent events.
7. **Advanced Topics**
   - Instrumental variables, regression discontinuity designs.
   - Generalized method of moments, spatial econometrics, ML augmentations.

Each chapter contains learning objectives, conceptual notes, worked examples, and code notebooks. Suggested readings and exercises are linked at the chapter level to keep the main text lightweight while remaining actionable.

## Contributing and Workflow

1. Clone the repository and set up a Python or R environment capable of running the examples.
2. Use the `utils/` module for shared helper functions and plotting themes.
3. Add new datasets in `data/` with documentation describing provenance and cleaning steps.
4. Reference canonical papers or textbooks via `references/`, citing them inline.
5. Open issues for new topics, corrections, or extension ideas.

## License

Content will be released under an open license (to be finalized) so that learners and educators can adapt and remix POT in their own courses.
