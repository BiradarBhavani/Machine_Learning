# Target Encoding

Replaces each category with the mean of the target for that category.
Best for high-cardinality nominal features. Risk: target leakage —
always fit on train only.

## Structure
```
Target_Encoding/
├── target_encoding.ipynb
└── data/loan_data.csv
```
