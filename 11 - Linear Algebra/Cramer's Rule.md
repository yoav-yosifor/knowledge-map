---
tags:
  - linear-algebra
  - concept
  - technique
---
---
## Core Idea

A square linear system $Ax=b$ has a unique solution exactly when $|A|\neq0$, and each component of that solution is a ratio of two determinants.

## Key Equation

$$
x_k=\frac{|A_k|}{|A|},\qquad A\in\mathbb{F}^{n\times n},\ b\in\mathbb{F}^{n\times1}
$$

**Derived From:** the statement as given in the source (it points to the Wikipedia entry "Cramer's rule" for details): $A_k$ is $A$ with its $k$-th column replaced by the vector $b$.

## Supporting Formulas

- Unique solution exists $\iff |A|\neq0$.
- $A_k$: replace column $k$ of $A$ by $b$.

## Derivation Outline

1. Check that $|A|\neq0$.
2. For each $k$, form $A_k$ by replacing column $k$ with $b$.
3. Compute $x_k=|A_k|/|A|$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md), [Invertible Matrices](../11%20-%20Linear%20Algebra/Invertible%20Matrices.md), [Matrices](../11%20-%20Linear%20Algebra/Matrices.md)
**Full Derivation:** 
