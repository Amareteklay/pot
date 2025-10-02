# Data Catalog

The `data` directory stores the datasets used throughout POT. Each dataset should be lightweight, well-documented, and reproducible.

## Organization

```
 data/
 ├── raw/        # original files (if redistribution is permitted)
 ├── processed/  # cleaned versions used in the book
 └── metadata/   # data dictionaries, provenance notes
```

## Documentation Requirements

- Provide a README or metadata YAML/JSON file describing the source, variables, and cleaning steps.
- Note any licensing restrictions or citation requirements.
- Include scripts in `utils/data_generation/` or `notebooks/` that reproduce the processed datasets.

## Starter Datasets

- Synthetic distributions for demonstrating sampling and CLT concepts.
- Toy regression datasets (housing prices, wage equations).
- Panel data for DiD/event study walkthroughs.
- Survival/event datasets (customer churn, machine failure, clinical trials).

As the project grows, keep datasets small enough to track with Git LFS or provide download scripts when necessary.
