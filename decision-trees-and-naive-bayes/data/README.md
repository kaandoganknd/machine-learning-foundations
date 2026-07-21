# Data

Raw teaching datasets are not committed because redistribution permissions have not been
established. Add the reviewed files below to this folder.

| Filename | Rows × columns | Reviewed SHA-256 |
|---|---:|---|
| `diabetes.csv` | 768 × 9 | `698c203a14aa31941d2251175330c9199f3ccdb31597abbba2a3e35416257a72` |
| `breast_cancer.csv` | 569 × 33 | `1425d9affa78ba8e53afc81d0ef8a19069ee10c4b21fe89b3cf514071b12ee33` |
| `auto_mpg.csv` | 398 × 9 | `09a282cf12c7ab4ffb517b496b0dd1a8bac6e95977178cc7832c32044c32c3f6` |
| `adult.csv` | 32,561 × 15 | `5b00264637dbfec36bdeaab5676b0b309ff9eb788d63554ca0a249491c86603d` |

`adult.csv` is headerless and is loaded with an explicit 15-column schema. In `auto_mpg.csv`,
non-numeric horsepower markers are treated as missing. The fully empty breast-cancer export
column and record identifier are excluded from modelling.
