# Encoding Techniques

Five separate folders, one per encoding technique — all demonstrated on
the same dataset (`loan_data.csv`) so they're easy to compare.

## Structure
```
Encoding_Techniques/
├── Label_Encoding/       # target column / binary ordinal features
├── OneHot_Encoding/      # nominal, low cardinality
├── Ordinal_Encoding/     # features with a genuine rank order
├── Target_Encoding/      # nominal, high cardinality (risk: leakage)
└── Binary_Encoding/      # nominal, medium/high cardinality (fewer columns than one-hot)
```

## Which one to use?

| Situation | Encoder |
|---|---|
| Target column / binary ordinal | Label Encoding |
| Nominal, low cardinality | One-Hot Encoding |
| Ordinal (has a natural rank) | Ordinal Encoding |
| Nominal, high cardinality | Target Encoding |
| Nominal, medium/high cardinality, fewer columns needed | Binary Encoding |

Every notebook fits the encoder on **train** only and transforms **test**
separately, to avoid data leakage.

## Why the same dataset (`loan_data.csv`) for every technique?

1. **Fair comparison** — if each notebook used a different dataset, you
   couldn't tell whether a difference was due to the *encoder* or due to
   *different data*. Keeping the dataset fixed means the only thing that
   changes between notebooks is the encoding technique itself.

2. **`loan_data.csv` already has every column type needed:**

   | Column | Type | Encoder that fits |
   |---|---|---|
   | `loan_status` (target) | binary | Label Encoding |
   | `person_gender` | binary nominal | Label / One-Hot |
   | `person_home_ownership`, `previous_loan_defaults_on_file` | nominal, few categories | One-Hot Encoding |
   | `person_education` | has a natural rank (High School < ... < Doctorate) | Ordinal Encoding |
   | `loan_intent` | nominal, several categories | Target Encoding / Binary Encoding |

3. **It mirrors real projects** — in practice you don't pick "the
   encoding technique" for a whole dataset, you pick a *different*
   encoder for *each column* based on that column's nature. Demonstrating
   all 5 on one dataset shows that mixed reality, instead of implying
   "always use One-Hot" or "always use Label."
