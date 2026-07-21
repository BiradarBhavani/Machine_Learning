# Binary Encoding

Converts categories to integers, then to binary digits split across
several columns — far fewer columns than One-Hot for medium/high
cardinality nominal features, without Target Encoding's leakage risk.

## Structure
```
Binary_Encoding/
├── binary_encoding.ipynb
└── data/loan_data.csv
```
