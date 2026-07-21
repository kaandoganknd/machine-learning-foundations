# Supervised Classification and Model Evaluation

This project consolidates and extends guided classification activities into one
reproducible comparison of binary and multiclass machine-learning workflows. It uses the
scikit-learn Wine dataset and a Titanic passenger dataset to demonstrate model selection,
leakage-safe preprocessing, and transparent evaluation.

## Highlights

- Compares logistic regression, RBF SVM, and a constrained decision tree.
- Uses stratified train/test splits and five-fold cross-validation on training data only.
- Fits imputation, encoding, and scaling inside scikit-learn pipelines.
- Explains macro versus weighted metrics for multiclass classification.
- Evaluates binary predictions with a confusion matrix, ROC-AUC, and precision-recall curve.
- Adds deterministic Titanic features while excluding direct identifiers and high-cardinality
  text fields from the model.

## Key results

- Wine: RBF SVM reaches a mean cross-validated macro F1 of 0.992 and correctly classifies 44
  of 45 holdout observations, with 97.8% accuracy and 0.976 macro F1. The notebook explicitly
  cautions against overgeneralising this result from a small teaching dataset.
- Titanic: logistic regression is selected by cross-validated ROC-AUC and achieves 84.9%
  accuracy, 83.4% balanced accuracy, 79.7% F1, and 0.878 ROC-AUC on 179 untouched holdout
  observations.

## Repository structure

```text
supervised-classification-and-model-evaluation/
├── README.md
├── data/
│   └── README.md
└── supervised_classification_and_model_evaluation.ipynb
```

## Run locally

From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Add `titanic.csv` to this project's `data/` folder and run the notebook from top to bottom.
The Wine dataset loads directly from scikit-learn.

## Data and ethical scope

The raw Titanic file is excluded because redistribution permission has not been established.
The analysis uses historical demographic attributes for education only, makes no causal
claims, and is not intended for decisions about individuals. See
[`data/README.md`](data/README.md).
