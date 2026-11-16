---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

An elementary matrix is the identity with a single row operation applied; multiplying by it on the left performs that same row operation on any matrix.

## Key Equation

$$
E=\rho(I)\ \Longrightarrow\ EA=\rho(A)
$$

**Derived From:** definition — $\rho$ is one elementary row operation, $E$ is the result of applying it to $I$.

## Supporting Formulas

- **Theorem.** $E=\rho(I)$ is invertible and its inverse is also elementary: $$ E^{-1}=\rho^{-1}(I) $$
- **Theorem.** $A$ is invertible $\iff$ $A$ is a product of elementary matrices.
- Row-reducing $A$ is left-multiplication by a sequence of elementary matrices: $$ E_n\cdots E_3E_2E_1A=I\ \Longrightarrow\ A^{-1}=E_n\cdots E_3E_2E_1 $$

## Derivation Outline

1. Apply one [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md) to $I$ to get $E$.
2. Left-multiplying $A$ by $E$ repeats that operation on $A$.
3. Chaining operations that reduce $A$ to $I$ gives $A^{-1}$ as the product of the $E_k$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md), [Invertible Matrices](../11%20-%20Linear%20Algebra/Invertible%20Matrices.md), [Gauss-Jordan Elimination](../11%20-%20Linear%20Algebra/Gauss-Jordan%20Elimination.md), [Matrix Multiplication](../11%20-%20Linear%20Algebra/Matrix%20Multiplication.md)
**Full Derivation:** 
