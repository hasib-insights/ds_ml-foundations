# 01 — Vectors

## 1. Concept

A vector is just an ordered list of numbers, where each position represents a feature or dimension. If a customer is described by `[Groceries spend, Electronics spend, Clothing spend]`, that customer is a 3-dimensional vector — same idea scales to hundreds of features, you just can't draw it anymore.

The core operations:

- **Addition/Subtraction** — element-wise, position by position
- **Scalar multiplication** — multiply every entry by the same number (scales the vector up/down without changing direction)
- **Dot product** — multiply matching positions and sum (covered in Module 00) — this is the basis for measuring how *aligned* two vectors are
- **Norm (length/magnitude)** — how "big" a vector is. The two you'll see constantly:
  - **L2 norm** (Euclidean): `√(x₁² + x₂² + ... + xₙ²)` — straight-line distance
  - **L1 norm** (Manhattan): `|x₁| + |x₂| + ... + |xₙ|` — sum of absolute values

## 2. Why It Matters for Data Science

- Every row in your dataset is a vector — clustering, KNN, and recommendation engines all run on **distance between vectors**.
- **Cosine similarity** (dot product scaled by the norms) is the standard way to compare things like customer behavior, document similarity in NLP, or product embeddings — it cares about *pattern*, not *scale*.
- **L1 and L2 norms** show up directly as the "penalty" terms in Lasso and Ridge regression (regularization) — they're literally just vector norms applied to the model's coefficients.

## 3. Worked Example

Two customers' spending across three categories:

| Customer | Groceries | Electronics | Clothing |
|---|---|---|---|
| A | 50 | 20 | 10 |
| B | 45 | 25 | 8 |

**A** = [50, 20, 10], **B** = [45, 25, 8]

**Difference (A − B):**
```
[50-45, 20-25, 10-8] = [5, -5, 2]
```

**Euclidean distance** (L2 norm of the difference):
```
√(5² + (-5)² + 2²) = √(25 + 25 + 4) = √54 ≈ 7.35
```

**Dot product:**
```
A · B = (50×45) + (20×25) + (10×8) = 2250 + 500 + 80 = 2830
```

**Cosine similarity** (dot product ÷ product of norms):
```
‖A‖ = √(50² + 20² + 10²) = √3000 ≈ 54.77
‖B‖ = √(45² + 25² + 8²)  = √2714 ≈ 52.10

cos(θ) = 2830 / (54.77 × 52.10) ≈ 0.99
```

A ~0.99 cosine similarity says these two customers have an almost identical *spending pattern*, even though the raw Euclidean distance (7.35) isn't zero — that gap between the two metrics is the whole point of the open question below.

## 4. Code

```python
import numpy as np

A = np.array([50, 20, 10])
B = np.array([45, 25, 8])

diff = A - B
print("Difference:", diff)

distance = np.linalg.norm(diff)              # Euclidean (L2) distance
print("Euclidean distance:", distance)

dot = np.dot(A, B)
print("Dot product:", dot)

cosine_sim = dot / (np.linalg.norm(A) * np.linalg.norm(B))
print("Cosine similarity:", cosine_sim)
```

## 5. Open Question

When would Euclidean distance and cosine similarity actually *disagree* about which two customers are "most similar"? (Hint: picture a customer who buys in the exact same proportions as A, but spends one-tenth as much overall — what happens to each metric?)

