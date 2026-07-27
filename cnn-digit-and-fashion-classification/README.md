# Convolutional Neural Networks for Digit and Fashion Classification

This project consolidates two guided image-classification activities into a reproducible CNN
study: handwritten digit recognition from competition-style CSV files and independent
Fashion-MNIST classification.

## Highlights

- Validates the supplied digit CSV schema, pixel range, class coverage, and missing values.
- Uses stratified training/validation separation for the labelled digit data.
- Builds compact convolutional networks rather than flattening images immediately.
- Generates 28,000 digit predictions without claiming accuracy on an unlabelled file.
- Evaluates Fashion-MNIST on its untouched official test partition.
- Reports accuracy, log-loss, confusion matrices, per-class recall, and visible errors.

## Key Results

- Digit CNN: **97.67% validation accuracy** and **0.0764 log-loss** on a stratified
  6,300-image validation set.
- Unlabelled digit file: **28,000 predictions generated**; no accuracy is claimed because
  ground-truth labels were not supplied.
- Fashion-MNIST CNN: **86.81% test accuracy** and **0.3684 log-loss** on the official
  10,000-image test set.

## Repository Structure

```text
cnn-digit-and-fashion-classification/
├── README.md
├── data/
│   └── README.md
└── cnn_digit_and_fashion_classification.ipynb
```

## Run Locally

Install the repository requirements, place the digit `train.csv` and `test.csv` files in a
local folder, and set `DIGITS_DATA_DIR` to that folder before running the notebook.
Fashion-MNIST downloads automatically through TensorFlow/Keras.

## Scope

This is a compact educational deep-learning project, not a production model or an exhaustive
architecture benchmark. No Kaggle leaderboard score, cloud deployment, or independent
research claim is made.
