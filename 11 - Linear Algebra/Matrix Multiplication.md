---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

The $(i,j)$ entry of a product is the row $i$ of the left matrix times the column $j$ of the right matrix; it is associative and distributive but not commutative.

## Key Equation

$$
A\in M_{m\times n}(\mathbb{F}),\ B\in M_{n\times p}(\mathbb{F}),\quad C=AB\in M_{m\times p}(\mathbb{F}),\qquad [C]_{ij}=[AB]_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}
$$

**Derived From:** definition — extends the row-times-column product below to every pair (row $i$ of $A$, column $j$ of $B$).

## Supporting Formulas

- $$ \begin{pmatrix}a_1&a_2&\cdots&a_n\end{pmatrix}\begin{pmatrix}b_1\\b_2\\ \vdots\\b_n\end{pmatrix}=\sum_{k=1}^{n}a_kb_k=a_1b_1+a_2b_2+\cdots+a_nb_n $$ — row vector ($1\times n$) times column vector ($n\times1$)
- The product is defined only when #columns of the left matrix = #rows of the right matrix.
- $$ AB\neq BA\ \text{in general} $$ — not commutative
- $$ (AB)C=A(BC) $$ — associativity
- $$ A(B+C)=AB+AC $$ — distributivity (the source prints $AB+BC$, which looks like a typo)
- $$ \alpha(AB)=(AB)\alpha $$ — scalars commute with products

## Derivation Outline

1. Check that the inner sizes match ($n$ columns of $A$ = $n$ rows of $B$).
2. For each $(i,j)$, multiply row $i$ of $A$ by column $j$ of $B$ and sum.
3. The result has the outer sizes, $m\times p$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Matrices](../11%20-%20Linear%20Algebra/Matrices.md), [Matrix Addition and Scaling](../11%20-%20Linear%20Algebra/Matrix%20Addition%20and%20Scaling.md), [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md)
**Full Derivation:** 
