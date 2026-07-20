# Data files

The raw CSV files are intentionally excluded because redistribution permissions have not been
established. To reproduce the notebook, add these files locally:

| Local filename | Expected shape | Required columns | SHA-256 of reviewed file |
|---|---:|---|---|
| `diabetes.csv` | 768 × 9 | `Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`, `Outcome` | `698c203a14aa31941d2251175330c9199f3ccdb31597abbba2a3e35416257a72` |
| `employees.csv` | 1000 × 8 | `First Name`, `Gender`, `Start Date`, `Last Login Time`, `Salary`, `Bonus %`, `Senior Management`, `Team` | `222246292f5090a6051ab5085a70ea1f317fbe5ca1313350f64097535173ac5c` |

The hashes identify the exact files used to generate the saved outputs. If your files differ,
the validation counts may also differ.
