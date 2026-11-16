---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

A subset $W\subseteq V$ of a vector space over $\mathbb{F}$ that is itself a vector space under the operations of $V$.

## Key Equation

*Shortcut criterion — $W\subseteq V$ is a subspace if and only if:*

$$
\forall u,w\in W:\ u+w\in W,\qquad \forall\alpha\in\mathbb{F},\,w\in W:\ \alpha w\in W,\qquad 0_V\in W
$$

**Derived From:** definition of a subspace; the source gives this as the "shortcut criterion" (closure under addition, closure under scalars, existence of the neutral element).

## Supporting Formulas

- Trivial subspaces of any $V$: $V$ itself, and $\{0\}$ (the smallest subspace of $V$).
- For subspaces $U,W\subseteq V$: $U\cap W$ is a subspace of $V$.
- $$ U+W=\{u+w\mid u\in U,\ w\in W\} $$ — sum of subspaces
- $$ U,W\subseteq U+W $$
- $$ U+W\neq U\cup W $$ — in general
- $U\cup W$ is a subspace of $V$ $\iff$ $U\subseteq W$ or $W\subseteq U$

## Derivation Outline

1. Check closure under addition.
2. Check closure under scalar multiplication.
3. Check that $0_V\in W$; the remaining axioms are inherited from $V$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Vector Spaces](../11%20-%20Linear%20Algebra/Vector%20Spaces.md), [Linear Combinations](../11%20-%20Linear%20Algebra/Linear%20Combinations.md)
**Full Derivation:** 
