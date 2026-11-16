---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

Several different-looking conditions on a square matrix all say the same thing: it is invertible (the source states this as a partial version of the theorem).

## Key Equation

$$
A\in M_{n}(\mathbb{F}):\quad A\ \text{invertible}\iff A\ \text{is a product of elementary matrices}\iff A\ \text{has canonical form}\ I_n\iff A\mathbf{x}=\mathbf{0}\ \text{has only}\ \mathbf{x}=\mathbf{0}\iff A\mathbf{x}=\mathbf{b}\ \text{has a unique solution for every}\ \mathbf{b}\in\mathbb{F}^n
$$

**Derived From:** theorem as stated in the source, without proof.

## Supporting Formulas

Equivalent conditions for a square $A\in M_n(\mathbb{F})$:
- $A$ is invertible.
- $A$ is a product of [Elementary Matrices](../11%20-%20Linear%20Algebra/Elementary%20Matrices.md).
- The canonical form ([Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md)) of $A$ is $I_n$.
- The homogeneous system $A\mathbf{x}=\mathbf{0}$ has only the solution $\mathbf{x}=\mathbf{0}$.
- $A\mathbf{x}=\mathbf{b}$ has a unique solution for every $\mathbf{b}\in\mathbb{F}^n$.

## Derivation Outline

1. The proof is not given in the source; fill it in by hand later.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Invertible Matrices](../11%20-%20Linear%20Algebra/Invertible%20Matrices.md), [Elementary Matrices](../11%20-%20Linear%20Algebra/Elementary%20Matrices.md), [Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md), [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md)
**Full Derivation:** 
