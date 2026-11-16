---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

An echelon form pushed further — every pivot equals 1 and is the only nonzero entry in its column — so the solution can be read off directly; it is unique for each matrix.

## Key Equation

$$
\begin{pmatrix}
1&0&*&0&*&*&*&0&*\\
0&1&*&0&*&*&*&0&*\\
0&0&0&1&*&*&*&0&*\\
0&0&0&0&0&0&0&1&*\\
0&0&0&0&0&0&0&0&0
\end{pmatrix}
$$

**Derived From:** definition, reached by elementary row operations.

## Supporting Formulas

Definition (all must hold):
- The matrix is in [Echelon Form](../11%20-%20Linear%20Algebra/Echelon%20Form.md).
- There are zeros above every pivot as well as below (each pivot's column is zero except the pivot).
- Every pivot equals 1.

**Theorem.** Every matrix $A$ has a unique reduced echelon form (ordinary echelon form is not unique).

The number of pivot columns (and hence free variables) can be read at a glance.

## Derivation Outline

1. Reach echelon form.
2. Scale each pivot row so the pivot is 1.
3. Clear the entries above each pivot.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md), [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md), [Echelon Form](../11%20-%20Linear%20Algebra/Echelon%20Form.md)
**Full Derivation:** 
