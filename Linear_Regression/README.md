# Linear Regression

Step-by-step notebook covering **Simple Linear Regression** (1 feature)
and **Multiple Linear Regression** (multiple features).

## 📁 Structure

```
Linear_Regression/
├── linear_regression.ipynb
├── data/
│   ├── Salary_Data.csv      # Simple Linear Regression (YearsExperience -> Salary)
│   └── Advertising.csv      # Multiple Linear Regression (TV, Radio, Newspaper -> Sales)
└── README.md
```

## 📖 What's inside the notebook

1. **Imports**
2. **Load data**
3. **EDA — check linearity** (`.corr()` + scatter plot) *before* choosing
   Linear Regression as the algorithm
4. **Define X and y**
5. **Train/test split**
6. **Scaling** — why it's optional here (only needed for regularized
   models like Ridge/Lasso, or to compare coefficients fairly)
7. **Fit the model**
8. **Inspect coefficients** (`coef_`, `intercept_`)
9. **Predict**
10. **Evaluate** — R², MAE, RMSE on train vs test (checks over/underfitting)
    + actual-vs-predicted plot
11. **Multiple Linear Regression** — same steps repeated on `Advertising.csv`
12. **Checklist** — quick recap of what to verify in any Linear Regression
    notebook

## 🚀 Getting started

```bash
git clone <your-repo-url>
cd Linear_Regression
pip install pandas matplotlib scikit-learn jupyter
jupyter notebook linear_regression.ipynb
```

## 🧠 Key takeaways

- Always check linearity (`corr()` / scatter plot) before fitting —
  Linear Regression assumes a straight-line relationship.
- Split data into train/test **before** fitting the model.
- Scaling is optional for plain Linear Regression but required for
  regularized variants (Ridge, Lasso) and distance-based models.
- Evaluate on the **test** set, not just train, using R², MAE, and RMSE.
- A large gap between train and test scores signals overfitting.
