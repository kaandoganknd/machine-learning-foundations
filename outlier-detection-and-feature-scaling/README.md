# Outlier Detection and Feature Scaling

This project is a refined and extended version of a guided data preprocessing exercise. It
applies IQR-based outlier detection, Min–Max scaling, and standardisation to Diabetes and
Employees datasets while documenting the effect of each preprocessing decision.

## Highlights

- Uses fixed 1.5×IQR bounds and excludes the target from outlier detection.
- Compares Diabetes distributions before and after filtering.
- Quantifies the change in target balance caused by removing 129 rows.
- Avoids deleting employee records because of missing fields unrelated to the analysis.
- Validates `MinMaxScaler` and `StandardScaler` outputs with explicit assertions.
- Documents possible zero-coded missing measurements in the Diabetes data.

## Repository structure

```text
outlier-detection-and-feature-scaling/
├── README.md
├── data/
│   └── README.md
└── outlier_detection_and_feature_scaling.ipynb
```

## Run locally

From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Add the two required CSV files to `outlier-detection-and-feature-scaling/data/`, rename the
Diabetes file to `diabetes.csv`, and run the notebook from top to bottom.

## Data note

The raw teaching datasets are not included because their redistribution permissions have not
been established. See [`data/README.md`](data/README.md) for filenames, schemas, and file hashes.

## Scope

This is a preprocessing demonstration rather than a predictive modelling study. The notebook
does not claim that every statistically extreme observation is erroneous.
