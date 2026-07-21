# Data

The raw Titanic CSV is intentionally not committed because its redistribution permission has
not been established. To reproduce the notebook, place the educational dataset supplied for
the exercise in this folder as `titanic.csv`.

## Expected file

- Filename: `titanic.csv`
- Rows: 891
- Columns: 12
- SHA-256 for the reviewed copy:
  `7d118fef8b6ccf7f81111877bc388536f7b1e498a655e3d649d19aaa010e9f6f`

Expected columns:

```text
PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch,
Ticket, Fare, Cabin, Embarked
```

The Wine dataset used in the first case study is loaded from
`sklearn.datasets.load_wine` and therefore requires no additional file.
