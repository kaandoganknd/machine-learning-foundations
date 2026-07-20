# Missing Data Detection and Imputation

This notebook is a refined and extended version of a guided data preprocessing exercise. It demonstrates
missing-value detection, simple imputation, structural-missingness analysis, and reproducible validation
across three teaching datasets.

## What this exercise demonstrates

- Missing-value counts and percentages with pandas
- Categorical treatment choices that avoid inferring personal attributes
- Median and most-frequent imputation with `SimpleImputer`
- Why structural missingness should not be replaced mechanically
- Missingness indicators for high-missingness fields
- Assertions that verify the transformations

## Key methodological improvement

The original seminar asked for mean, median, and mode replacement in the placement dataset. Review of the
actual data shows that all 67 missing salaries belong to students who were not placed. Filling these values
with a typical placed salary would invent outcomes. The portfolio version leaves salary as not applicable
and records the decision explicitly.

## Repository structure

```text
missing-data-imputation/
├── README.md
├── missing_data_imputation.ipynb
└── data/
    └── README.md
```

## Run locally

From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Place the three required CSV files in `missing-data-imputation/data/`, then open
`missing-data-imputation/missing_data_imputation.ipynb` and run all cells.

## Verified results

- Employees: 1,000 rows, 8 columns, and 322 missing cells across four categorical fields
- Placement: 215 rows, 15 columns, and 67 structurally missing salary values
- Titanic: 891 rows, 12 columns; median age 28 and embarkation mode S

The cleaned notebook was executed from top to bottom against the user-provided source files, and all saved
assertions passed.

## Scope and limitations

This is a preprocessing exercise, not a predictive modelling project. It does not make causal claims or
report model performance. Raw datasets are excluded from version control until their redistribution terms
are confirmed.
