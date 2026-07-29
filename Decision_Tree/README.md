# Decision Tree Classifier

Binary classification on `loan_data.csv` (predicting `loan_status`).

## Structure
```
Decision_Tree/
├── decision_tree.ipynb
└── data/loan_data.csv
```

## What's inside
1. Load data, define X/y, split
2. Preprocessing — **encoding only, no scaling** (tree splits don't care
   about feature magnitude)
3. Fit with `max_depth` limit (prevents overfitting)
4. Predict
5. Evaluate — train vs test accuracy, classification report, confusion matrix
6. Feature importance
7. Visualize the top levels of the tree

## Key takeaway
Decision Trees need encoding but **not** scaling. Unlike Logistic
Regression, they can overfit badly if left unconstrained — always check
train vs test accuracy, and tune `max_depth` / `min_samples_leaf` if the
gap is large.
