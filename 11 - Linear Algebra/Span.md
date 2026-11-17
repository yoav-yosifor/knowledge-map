---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

The span of a set of vectors is the collection of all linear combinations of them, and it is the smallest subspace containing that set.

## Key Equation

$$
\mathrm{Span}(S)=\{\alpha_1v_1+\alpha_2v_2+\cdots+\alpha_nv_n\mid \alpha_i\in\mathbb{F},\ v_i\in S\},\qquad S=\{v_1,\dots,v_n\}\subseteq V
$$

**Derived From:** definition, for $V$ a vector space over $\mathbb{F}$ and $S\subseteq V$; the set of all [linear combinations](../11%20-%20Linear%20Algebra/Linear%20Combinations.md) of vectors from $S$. Also written $\mathrm{Sp}(S)$.

## Supporting Formulas

- $\mathrm{Span}(S)$ is a vector space (a [subspace](../11%20-%20Linear%20Algebra/Subspaces.md) of $V$).
- $$ S\subseteq W,\ W\ \text{a subspace of }V\ \Rightarrow\ \mathrm{Span}(S)\subseteq W $$ — $\mathrm{Span}(S)$ is the minimal subspace of $V$ containing $S$.
- $$ \mathrm{Span}(S)=W $$ — then $S$ *spans* $W$ ($S$ is a spanning set of $W$).

## Derivation Outline

1. Take all vectors from $S$ and all scalars from $\mathbb{F}$.
2. Collect every linear combination of them — that collection is $\mathrm{Span}(S)$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear Combinations](../11%20-%20Linear%20Algebra/Linear%20Combinations.md), [Linear Independence](../11%20-%20Linear%20Algebra/Linear%20Independence.md), [Subspaces](../11%20-%20Linear%20Algebra/Subspaces.md), [Vector Spaces](../11%20-%20Linear%20Algebra/Vector%20Spaces.md)
**Full Derivation:** 
