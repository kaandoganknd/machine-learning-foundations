# Neural Networks and Image Classification

This project consolidates and extends guided deep-learning activities into a reproducible
study of feed-forward regression, MNIST digit classification, and CIFAR-10 image
classification.

## Highlights

- Separates training, validation, and test data throughout the modelling workflow.
- Demonstrates the difference between interpolation and extrapolation on a sine function.
- Trains a regularised Dense classifier and performs class-level MNIST error analysis.
- Establishes a lightweight CIFAR-10 Dense baseline and documents why a CNN is the next step.
- Uses early stopping, fixed random seeds, confusion matrices, per-class recall, and
  high-confidence error examples.
- Documents why the supplied cloud setup materials are not evidence of AWS or Azure work.

## Key results

- Sine regression: **0.0377 interpolation RMSE** versus **1.7004 wide-range extrapolation
  RMSE**, demonstrating that good interpolation does not imply reliable extrapolation.
- MNIST Dense classifier: **97.39% test accuracy** on 10,000 images.
- CIFAR-10 Dense baseline: **22.90% test accuracy** on the full 10,000-image test set,
  compared with a 10% chance baseline. This intentionally lightweight result establishes a
  starting point for a future CNN rather than a competitive image classifier.

## Repository structure

```text
neural-networks-and-image-classification/
├── README.md
├── data/
│   └── README.md
└── neural_networks_and_image_classification.ipynb
```

## Run locally

From the repository root, create a virtual environment, install `requirements.txt`, and run
the notebook from top to bottom. The first execution downloads MNIST and CIFAR-10 through
TensorFlow/Keras, so internet access is required.

TensorFlow is CPU-compatible for this notebook. The CIFAR-10 baseline uses a stratified
6,000-image training subset, a 1,000-image validation subset, and the full 10,000-image test
set so the exercise remains practical on CPU-only hardware.

## Scope

This is a compact educational deep-learning project, not a production model or an exhaustive
architecture benchmark. AWS and Azure setup documents were reviewed, but no cloud experiment
or deployment artefact was supplied; no cloud implementation claim is made.
