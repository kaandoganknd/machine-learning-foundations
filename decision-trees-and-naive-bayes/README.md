# Decision Trees and Naive Bayes: Classification and Regression

This project consolidates and extends guided decision-tree and Naive Bayes activities into
one reproducible comparison across four datasets and five modelling tasks. It emphasises
training-only model selection, appropriate baselines, algorithm assumptions, and error
analysis rather than reporting accuracy alone.

## Highlights

- Tunes decision-tree complexity with cross-validation before holdout evaluation.
- Visualises a two-feature classification boundary and an interpretable tree excerpt.
- Compares Auto MPG tree regression with a linear-regression baseline.
- Uses Gaussian Naive Bayes for continuous Iris measurements.
- Uses Bernoulli Naive Bayes for binned and one-hot Adult features.
- Documents medical and demographic limitations prominently.

## Key results

- Diabetes tree: 0.802 holdout ROC-AUC and 47.8% recall.
- Two-feature breast-tumour tree: 87.7% accuracy and 0.947 ROC-AUC.
- Auto MPG: the 3.54 MPG linear-baseline RMSE beats the tree's 3.91 MPG RMSE.
- Iris Gaussian NB: 92.1% holdout accuracy.
- Adult Bernoulli NB: 0.891 ROC-AUC, 81.4% recall, and 55.6% precision.

## Repository structure

```text
decision-trees-and-naive-bayes/
├── README.md
├── data/
│   └── README.md
└── decision_trees_and_naive_bayes.ipynb
```

## Run locally

From the repository root, create a virtual environment, install `requirements.txt`, add the
four required CSV files to this project's `data/` folder, and run the notebook from top to
bottom. The Iris dataset loads directly from scikit-learn.

## Data and ethical scope

Raw teaching datasets are excluded because redistribution permissions have not been
established. The medical examples are not diagnostic systems, and the Adult example is not
a fairness assessment or a production decision model. See [`data/README.md`](data/README.md).
