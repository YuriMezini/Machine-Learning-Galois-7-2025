# Machine-Learning-Galois-7-2025
# Non-\(S_7\) Galois Group Classifiers (50/50, 60/40, 80/20 splits)

This repository contains machine–learning models that classify the Galois
group of an irreducible septic polynomial among the six non-\(S_7\) groups
\[
  A_7,\ \mathrm{PSL}(3,2),\ C_7\rtimes C_3,\ D_7,\ C_7\rtimes C_6,\ C_7.
\]

All models use the same features (coefficients, discriminant, and
invariants) and the same classifier architecture; the only difference is
**how we split the data into train and test sets**:

- `ml_nonS7_50_50.py` – 50% train / 50% test  
- `ml_nonS7_60_40.py` – 60% train / 40% test  
- `ml_nonS7_80_20.py` – 80% train / 20% test  

This allows us to check how stable the results are when we vary the size of
the external hold–out test set.

---

## 1. Data and features

All scripts expect a CSV file containing the non-\(S_7\) part of the AIMS-7
database, e.g.

```python
CSV_PATH = "/path/to/AIMS-7inv.2025.csv"
