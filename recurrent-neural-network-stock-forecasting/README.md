# Recurrent Neural Networks for One-Step Stock-Price Forecasting

This project develops and evaluates LSTM and GRU models for retrospective one-step-ahead
forecasting of Mastercard's daily High price from the previous 60 trading days.

## Highlights

- Validates 3,872 chronological observations from May 2006 to October 2021.
- Fits the scaler only on the training period to prevent future information leakage.
- Uses data through 2019 for training, 2020 for validation and early stopping, and 2021 as
  the final holdout period.
- Compares LSTM and GRU models with a persistence baseline that repeats the previous price.
- Reports RMSE, MAE, MAPE, learning curves, and aligned holdout-period forecasts.
- Separates predictive error from investment or trading claims.

## Key Results

On the 195-session 2021 holdout period:

- Persistence baseline: **5.28 RMSE**, **3.84 MAE**, and **1.06% MAPE**.
- GRU: **7.47 RMSE**, **5.87 MAE**, and **1.62% MAPE**.
- LSTM: **11.47 RMSE**, **9.49 MAE**, and **2.59% MAPE**.

The baseline outperformed both recurrent models. This negative result is retained because it
demonstrates rigorous benchmark comparison and prevents an unsupported claim that a more
complex model is automatically better.

## Repository Structure

```text
recurrent-neural-network-stock-forecasting/
├── README.md
├── data/
│   └── README.md
└── recurrent_neural_network_stock_forecasting.ipynb
```

## Run Locally

Install the repository requirements, place `Mastercard_stock_history.csv` in a local folder,
and set `MASTERCARD_DATA_DIR` to that folder before running the notebook from top to bottom.

The raw CSV is not redistributed because its original download provenance and reuse licence
were not supplied.

## Scope

This is a compact educational forecasting experiment, not a production model, trading
strategy, or investment recommendation. The dataset ends in October 2021, and the results
should not be interpreted as current market forecasts.
