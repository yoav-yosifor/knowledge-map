---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

A matrix is a rectangular array of field elements; the set of all $m\times n$ matrices over $\mathbb{F}$ is where matrix algebra lives (it is not itself a field).

## Key Equation

$$
A\in M_{m\times n}(\mathbb{F}),\qquad (A)_{ij}=[A]_{ij}=a_{ij}
$$

**Derived From:** notation — $a_{ij}$ is the entry in row $i$, column $j$.

## Supporting Formulas

- $\mathbb{F}^{m\times n}=M_{m\times n}(\mathbb{F})=M^{m\times n}(\mathbb{F})$ — all $m\times n$ matrices with entries in the field $\mathbb{F}$.
- $$ A=B\iff A,B\in M_{m\times n}(\mathbb{F})\ \text{and}\ [A]_{ij}=[B]_{ij}\ \ \forall\, i,j $$ — equality: same size and same entries.
- Square matrix: #rows = #columns, $A\in M_n(\mathbb{F})=M_{n\times n}(\mathbb{F})$.
- $$ I_n=\begin{pmatrix}1&&0\\&\ddots&\\0&&1\end{pmatrix} $$ — identity matrix, the neutral element for multiplication.
- $$ 0_n=\begin{pmatrix}0&&0\\&\ddots&\\0&&0\end{pmatrix} $$ — zero matrix, the neutral element for addition.

## Derivation Outline

1. Index entries by row $i$ and column $j$.
2. Two matrices are equal only if their sizes match and every entry matches.
3. Define operations on them: [Matrix Addition and Scaling](../11%20-%20Linear%20Algebra/Matrix%20Addition%20and%20Scaling.md), [Matrix Multiplication](../11%20-%20Linear%20Algebra/Matrix%20Multiplication.md).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Matrix Addition and Scaling](../11%20-%20Linear%20Algebra/Matrix%20Addition%20and%20Scaling.md), [Matrix Multiplication](../11%20-%20Linear%20Algebra/Matrix%20Multiplication.md), [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md)
**Full Derivation:** 
