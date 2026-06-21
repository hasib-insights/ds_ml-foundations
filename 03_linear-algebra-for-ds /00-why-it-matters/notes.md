# 00 — Why Linear Algebra Matters for Data Science

## 1. Concept

Linear algebra is the math of organizing numbers into vectors and matrices, and combining them through a small set of operations (addition, scaling, multiplication). That's it — there's no deeper mystery at the foundation. What makes it powerful is that almost any dataset and almost any "transformation" of a dataset can be written this way, which means a handful of operations end up doing an enormous amount of work.

## 2. Why It Matters for Data Science

You already think in this structure without calling it linear algebra:

- A **spreadsheet** — rows of records, columns of fields — *is* a matrix.
- A **single row** (one customer, one transaction, one product) — *is* a vector.
- A **weighted sum**, like `Revenue = Σ(Quantity × Price)`, *is* a dot product.
- A **regression trendline** in Excel is solving a system of linear equations behind the scenes.

Four areas you'll hit constantly in data science are direct extensions of this:

| Area | What's really happening |
|---|---|
| Linear Regression | Solving `Ax = b` for the best-fit coefficients |
| PCA (dimensionality reduction) | Eigenvectors finding the directions where your data varies the most |
| Recommender Systems | Matrix factorization — splitting a big "users × products" matrix into smaller pieces |
| Neural Networks | Each layer is just matrix multiplication followed by a small nonlinear tweak |

So the order you're learning in (vectors → matrices → systems of equations → eigenvalues → decomposition → applications) isn't arbitrary — it's building toward being able to read those four rows of the table above and actually understand what's happening, not just call `.fit()`.

## 3. Worked Example

Say you're looking at a small product sales table:

| Product | Quantity Sold | Unit Price ($) |
|---|---|---|
| A | 10 | 5 |
| B | 4 | 12 |
| C | 7 | 8 |

Quantity is a vector: **q** = [10, 4, 7]
Price is a vector: **p** = [5, 12, 8]

Total revenue is the **dot product** of the two vectors:

```
q · p = (10×5) + (4×12) + (7×8)
      = 50 + 48 + 56
      = 154
```

That's the entire idea of a dot product — multiply matching positions, then sum. You've likely done this in Excel with `SUMPRODUCT()` without thinking of it as linear algebra.

## 4. Code

```python
import numpy as np

quantity = np.array([10, 4, 7])
price = np.array([5, 12, 8])

revenue = np.dot(quantity, price)
print(revenue)  # 154
```

Same calculation, same answer — but this is the form every later module builds on. Once you're comfortable with this, "Module 1: Vectors" is really just a deeper look at everything you can do with `q` and `p` beyond just multiplying them together.

## 5. Open Question

How far does this "spreadsheet = matrix" intuition actually stretch once you get to something like a neural network with millions of parameters — is it still the same operations just repeated at scale, or does something conceptually different start happening? (Answer this for yourself once you reach Module 10.)

