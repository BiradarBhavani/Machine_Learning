# Classification Metrics

Trains a quick Logistic Regression model on `loan_data.csv`, then walks
through every major classification metric using its real predictions.

## Structure
```
Classification_Metrics/
├── classification_metrics.ipynb
└── data/loan_data.csv
```

## What's inside
1. Load data + train a quick model (to get real predictions to evaluate)
2. Confusion Matrix — TP/TN/FP/FN, the foundation of every other metric
3. Accuracy
4. Precision
5. Recall
6. F1-score
7. `classification_report` — all of the above at once
8. ROC-AUC
9. ROC curve visualization
10. Cheat sheet — which metric to use when

## Cheat sheet

| Metric | Question it answers | Use when |
|---|---|---|
| Accuracy | % correct overall | Classes are balanced |
| Precision | How many predicted positives were correct? | False positives are costly |
| Recall | How many actual positives were caught? | False negatives are costly |
| F1-score | Balance of precision and recall | Need one summary number |
| ROC-AUC | How well does the model rank positives vs negatives? | Comparing models, threshold-independent |
