---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

A square matrix is invertible if some matrix undoes it from both sides, giving the identity.

## Key Equation

$$
A\ \text{invertible}\iff\exists B:\ AB=BA=I,\qquad B=A^{-1}
$$

**Derived From:** definition, for a square matrix $A$.

## Supporting Formulas

- $$ AB\ \text{invertible}\iff A\ \text{and}\ B\ \text{invertible},\quad (AB)^{-1}=B^{-1}A^{-1} $$
- $$ (\alpha A)^{-1}=\alpha^{-1}A^{-1} $$
- $$ (A^{-1})^{-1}=A $$
- $$ (A^{-1})^t=(A^t)^{-1} $$
- The sum of invertible matrices (or of non-invertible ones) is not necessarily invertible.

## Derivation Outline

1. Look for $B$ with $AB=BA=I$.
2. In practice find it with the [Gauss-Jordan Elimination](../11%20-%20Linear%20Algebra/Gauss-Jordan%20Elimination.md).
3. Equivalent conditions are collected in the [Invertible Matrix Theorem](../11%20-%20Linear%20Algebra/Invertible%20Matrix%20Theorem.md).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Matrices](../11%20-%20Linear%20Algebra/Matrices.md), [Matrix Multiplication](../11%20-%20Linear%20Algebra/Matrix%20Multiplication.md), [Transpose](../11%20-%20Linear%20Algebra/Transpose.md), [Gauss-Jordan Elimination](../11%20-%20Linear%20Algebra/Gauss-Jordan%20Elimination.md), [Elementary Matrices](../11%20-%20Linear%20Algebra/Elementary%20Matrices.md), [Invertible Matrix Theorem](../11%20-%20Linear%20Algebra/Invertible%20Matrix%20Theorem.md)
**Full Derivation:** 
