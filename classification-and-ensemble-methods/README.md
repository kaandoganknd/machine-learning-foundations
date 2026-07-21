# Classification and Ensemble Methods

This project consolidates and extends guided classification activities into two reproducible
model-comparison studies. It compares support vector machines, K-nearest neighbours, tree
ensembles, boosting, voting, and stacking while keeping model selection separate from final
holdout evaluation.

## Highlights

- Compares 13 classifiers and ensembles on Iris using one repeated cross-validation design.
- Uses scaling inside model pipelines to prevent validation leakage.
- Benchmarks bagging, random forests, extra trees, boosting, voting, and stacking.
- Compares three boosting approaches and a voting ensemble on Wine.
- Includes dummy baselines, macro-F1, fold variation, confusion matrices, and permutation
  importance.
- Clearly separates explanatory two-feature decision boundaries from four-feature model
  evaluation.

## Key results

- Iris linear SVC: 0.966 mean macro-F1 across 25 training-only validation folds.
- Iris soft voting ensemble: 0.956 mean macro-F1.
- Wine histogram gradient boosting: 0.959 mean macro-F1.
- Both selected models score 1.000 macro-F1 on their small holdouts (30 Iris rows and 36 Wine
  rows), so the repeated-validation results are the more cautious performance summary.

## Repository structure

```text
classification-and-ensemble-methods/
├── README.md
├── data/
│   └── README.md
└── classification_and_ensemble_methods.ipynb
```

## Run locally

From the repository root, create a virtual environment, install `requirements.txt`, and run
the notebook from top to bottom. Both datasets load directly from scikit-learn, so no local
data files are required.

## Scope and limitations

The datasets are small educational benchmarks. The notebook demonstrates reproducible model
comparison rather than production readiness. The supplied SageMaker material contained
reading links but no completed cloud artefact, so this repository does not claim AWS model
training. See [`data/README.md`](data/README.md) for the input-data decision.
