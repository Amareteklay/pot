# Utilities

The `utils` directory houses shared helper code that keeps the textbook examples concise and consistent.

## Planned Structure

- `data_generation/`: simulation scripts for synthetic datasets.
- `estimation/`: wrappers for common estimators (e.g., OLS summaries, MLE routines).
- `visualization/`: plotting themes, ggplot/matplotlib helpers, and diagnostic charts.
- `formatting/`: functions for styling tables and exporting results.

## Usage Guidelines

- Keep functions modular and well-documented with docstrings and examples.
- Avoid hard-coding file paths; rely on configuration files or environment variables.
- Include lightweight unit tests or notebooks demonstrating usage when possible.

## Roadmap

1. Establish a base Python package structure with `__init__.py` files.
2. Provide cross-language parity where feasible (e.g., R scripts mirroring Python utilities).
3. Build a gallery of reusable figures (residual plots, survival curves, treatment effect charts).
