---
tags:
  - linear-algebra
  - concept
  - technique
---
---
## Core Idea

Gauss–Jordan elimination used to find an inverse: place $A$ next to the identity and row-reduce; if $A$ reaches the identity, what appears on the other side is $A^{-1}$.

## Key Equation

$$
\left(\,A\mid I\,\right)\ \xrightarrow{\text{elementary row operations}}\ \left(\,I\mid A^{-1}\,\right)
$$

**Derived From:** the same row operations that turn $A$ into $I$, applied to $I$, build $A^{-1}$ (see [Elementary Matrices](../11%20-%20Linear%20Algebra/Elementary%20Matrices.md)).

## Supporting Formulas

For $A\in M_{n\times n}(\mathbb{F})$:
- If the canonical form of $A$ is $I$, the right-hand block is $A^{-1}$.
- If the canonical form of $A$ is not $I$, $A$ is **not invertible**.

## Derivation Outline

1. Write the augmented matrix $(A\mid I)$ with $I$ of the matching size.
2. Row-reduce until the left block is in [Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md) (the canonical form).
3. Check whether the left block is $I$; if so, read $A^{-1}$ from the right block.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Invertible Matrices](../11%20-%20Linear%20Algebra/Invertible%20Matrices.md), [Elementary Matrices](../11%20-%20Linear%20Algebra/Elementary%20Matrices.md), [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md), [Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md)
**Full Derivation:** 
