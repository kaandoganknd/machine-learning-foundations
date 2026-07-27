# Data

This project expects a local file named `Mastercard_stock_history.csv`.

Expected schema:

```text
Date, Open, High, Low, Close, Volume, Dividends, Stock Splits
```

The validated local file contains 3,872 daily observations from 25 May 2006 to
11 October 2021, with no missing values or duplicate dates.

The CSV is not redistributed because its original download provenance and reuse licence were
not supplied. To run the notebook, place the file in a local folder and set
`MASTERCARD_DATA_DIR` to that folder.
