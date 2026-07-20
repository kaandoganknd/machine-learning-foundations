# Categorical Encoding and Imbalanced Classification

This project consolidates and extends six guided preprocessing activities into one
reproducible analysis. It demonstrates mixed-type feature encoding, classification
evaluation, and leakage-safe resampling across Adult, Employees, and Diabetes datasets.

## Highlights

- Separates ordinal education encoding from nominal one-hot encoding.
- Uses `ColumnTransformer` and pipelines to fit preprocessing only on training data.
- Treats `?` sentinels as missing and removes exact Adult duplicates before splitting.
- Encodes employee categories without using employee names or discarding incomplete rows.
- Compares baseline, random oversampling, random undersampling, and SMOTE using stratified CV.
- Selects a strategy using training-fold PR-AUC and evaluates once on an untouched test set.
- Uses confusion matrices and multiple metrics instead of relying on accuracy alone.

## Key results

- Adult holdout: 85.1% accuracy, 0.900 ROC-AUC, and 0.762 PR-AUC.
- Diabetes random oversampling: recall increases from 50.7% to 67.2% and F1 from 56.2% to
  64.3% on the same untouched test set.
- Employees: 1,000 rows are retained and three categorical fields become 14 one-hot features.

## Repository structure

```text
categorical-encoding-and-imbalanced-classification/
├── README.md
├── data/
│   └── README.md
└── categorical_encoding_and_imbalanced_classification.ipynb
```

## Run locally

From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Add the three required CSV files to this project's `data/` folder, rename the Diabetes file
to `diabetes.csv`, and run the notebook from top to bottom.

## Data and ethical scope

Raw teaching datasets are excluded because redistribution permissions have not been
established. The Adult dataset includes sensitive demographic fields; this exercise is not a
fairness assessment or a production decision system. See [`data/README.md`](data/README.md).
