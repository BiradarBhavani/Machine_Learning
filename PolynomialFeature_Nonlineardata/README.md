# Non-Linear Data — Polynomial Regression

Handles data where `corr()` is close to 0 but a scatter plot shows a
curved pattern — plain Linear Regression underfits this, so Polynomial
Regression is used instead.

## Structure
```
Non_Linear_Data/
├── non_linear_data.ipynb
└── data/iceNL.csv
```

## What's inside
1. Load data
2. Check linearity — scatter plot + `corr()`
3. Baseline Linear Regression (shows the underfit)
4. `PolynomialFeatures` — expand the feature into x, x² terms
5. Fit Linear Regression on the expanded features
6. Evaluate — R², MAE, RMSE on train vs test
7. Visualize the fitted curve
8. Note on going tree-based if polynomial still underperforms

## Key takeaway
Low correlation ≠ no relationship — it can mean the relationship is
**non-linear**. Always check with a scatter plot before ruling a feature
out.
