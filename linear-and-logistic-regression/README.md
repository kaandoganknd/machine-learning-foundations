# Linear and Logistic Regression: Model Choice and Diagnostics

This project consolidates and extends three guided regression exercises into a reproducible
study of how target type determines model choice. It combines Iris classification, Iris
continuous-outcome regression, and a diagnostic comparison of linear and logistic models on
a binary Diabetes outcome.

## Highlights

- Applies multinomial logistic regression to three-class Iris species prediction.
- Compares linear-regression feature sets with training-only cross-validation.
- Evaluates continuous predictions with MAE, RMSE, R², and residual diagnostics.
- Demonstrates why ordinary linear regression is unsuitable for binary probabilities.
- Uses median imputation and scaling inside leakage-safe pipelines.
- Preserves all Diabetes rows and documents the treatment of zero placeholders.

## Key results

- Iris classification: 0.958 mean cross-validated macro F1 and 93.3% holdout accuracy.
- Iris sepal-length regression: 0.324 cm holdout RMSE and 0.828 R², versus 0.816 cm RMSE for
  the training-mean baseline.
- Diabetes: the linear probability model creates 27 invalid holdout predictions outside
  [0, 1], while logistic regression remains bounded and reaches 0.824 ROC-AUC.

## Repository structure

```text
linear-and-logistic-regression/
├── README.md
├── data/
│   └── README.md
└── linear_and_logistic_regression.ipynb
```

## Run locally

From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Add `iris.csv` and `diabetes.csv` to this project's `data/` folder and run the notebook from
top to bottom.

## Data and ethical scope

Raw teaching datasets are excluded because redistribution permissions have not been
established. The Diabetes analysis is educational only and is not a clinical model. See
[`data/README.md`](data/README.md).
