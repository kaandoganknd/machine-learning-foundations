# Data setup

The public portfolio package intentionally excludes raw CSV files. Copy the following files into this
directory before running the notebook:

```text
employees.csv
Placement_Data_Full_Class.csv
train.csv
```

## Source notes

- `employees.csv` is the teaching dataset used by the seminar's Pandas missing-data practical. A matching
  copy appears in the MIT-licensed `sivabalanb/Data-Analysis-with-Pandas-and-Python` repository, but confirm
  provenance and redistribution rights before committing the raw file.
- `Placement_Data_Full_Class.csv` is associated with the Kaggle *Factors Affecting Campus Placement*
  dataset. Public mirrors report unclear or unknown redistribution terms, so the raw file should not be
  committed without confirmation from the dataset owner.
- `train.csv` matches the 891-row Kaggle Titanic training dataset. Obtain it through the Kaggle competition
  or a clearly licensed mirror and comply with the applicable source terms.

The `.gitignore` file prevents CSV files in this directory from being committed accidentally.
