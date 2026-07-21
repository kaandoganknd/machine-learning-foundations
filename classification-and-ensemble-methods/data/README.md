# Data Notes

No raw data files are required or redistributed in this project.

## Modelling data

The notebook loads the documented Iris and Wine datasets distributed with scikit-learn.
This makes the analysis reproducible without relying on an unverified external file source.

## Supplied Iris CSV review

The teaching CSV supplied for the original activity was reviewed before the portfolio
refactor:

- 150 rows and 6 columns;
- 4 numeric measurement fields, 1 species target, and an index-like `Id` field;
- no encoded missing values;
- 50 rows for each of the three species; and
- SHA-256: `600ac44f23c2e6e0ae37daac8ceb2baba4df963efa580eb31b3b576b28e34c55`.

The `Id` field is not a biological measurement and must not be used as a predictor. The file
is excluded because its redistribution permission and provenance were not established. The
scikit-learn Iris copy differs from the supplied CSV in three measurement cells, so they
should not be described as byte- or value-identical sources.

## References

- [scikit-learn Iris loader](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html)
- [scikit-learn Wine loader](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html)
