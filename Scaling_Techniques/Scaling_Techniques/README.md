# Scaling Techniques

All three scaling techniques in one notebook, demonstrated on the same
dataset (`loan_data.csv`) so they're easy to compare directly.

## Structure
```
Scaling_Techniques/
├── scaling_techniques.ipynb
└── data/loan_data.csv
```

## What's inside
1. Load data, define X/y, split
2. Check outliers with a boxplot first — decides which scaler fits
3. **StandardScaler** — mean 0, std 1
4. **MinMaxScaler** — scales to [0, 1]
5. **RobustScaler** — uses median/IQR, resistant to outliers
6. Side-by-side comparison of all three on the same column

## Which one to use?

| Situation | Scaler |
|---|---|
| Roughly normal data, no/few outliers | StandardScaler |
| Need a bounded [0, 1] range, no/few outliers | MinMaxScaler |
| Data has outliers | RobustScaler |

Every scaler is fit on **train** only and applied to **test** with
`transform()`, to avoid data leakage.
