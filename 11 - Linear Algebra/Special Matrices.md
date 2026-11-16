---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

Square matrices with a prescribed pattern of zeros or symmetry: triangular, diagonal, scalar, symmetric and anti-symmetric.

## Key Equation

$$
\underbrace{\begin{pmatrix}*&*&*\\0&*&*\\0&0&*\end{pmatrix}}_{\text{upper triangular}}\qquad
\underbrace{\begin{pmatrix}*&0&0\\ *&*&0\\ *&*&*\end{pmatrix}}_{\text{lower triangular}}\qquad
\underbrace{\begin{pmatrix}*&0&0\\0&*&0\\0&0&*\end{pmatrix}}_{\text{diagonal}}\qquad
\underbrace{\begin{pmatrix}\alpha&0&0\\0&\alpha&0\\0&0&\alpha\end{pmatrix}}_{\text{scalar}}
$$

**Derived From:** definitions, for $A\in M_{n\times n}(\mathbb{F})$ (shown for $3\times3$).

## Supporting Formulas

- Upper triangular: all entries **below** the main diagonal are zero.
- Lower triangular: all entries **above** the main diagonal are zero.
- Diagonal: all entries above and below the main diagonal are zero.
- $$ A=\alpha I,\ \alpha\in\mathbb{F} $$ — scalar matrix
- $$ A^t=A $$ — symmetric
- $$ A=-A^t $$ — anti-symmetric (the source defines both for real matrices)

## Derivation Outline

1. Look at the position of the entries relative to the main diagonal.
2. Name the matrix by which regions are forced to zero.
3. Symmetric and anti-symmetric use the [Transpose](../11%20-%20Linear%20Algebra/Transpose.md).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Matrices](../11%20-%20Linear%20Algebra/Matrices.md), [Transpose](../11%20-%20Linear%20Algebra/Transpose.md), [Trace](../11%20-%20Linear%20Algebra/Trace.md)
**Full Derivation:** 
