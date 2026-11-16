---
tags:
  - linear-algebra
  - concept
  - technique
---
---
## Core Idea

Three allowed moves on the rows of a system that never change its solution set, used to simplify the system until the solution is visible.

## Key Equation

$$
R_i\leftrightarrow R_j,\qquad \alpha R_i\to R_i\ (\alpha\neq0),\qquad R_i+\alpha R_j\to R_i\ (j\neq i)
$$

**Derived From:** each operation is reversible, so the new system has exactly the same solutions as the old one.

## Supporting Formulas

- $$ \begin{cases}2x+y=1\\5x+8y=0\end{cases}\xrightarrow{R_1\leftrightarrow R_2}\begin{cases}5x+8y=0\\2x+y=1\end{cases} $$ — row swap
- $$ \begin{cases}5x+8y=0\\2x+y=1\end{cases}\xrightarrow{\frac12R_1\to R_1}\begin{cases}2.5x+4y=0\\2x+y=1\end{cases} $$ — scale a row by a nonzero scalar
- $$ \begin{cases}5x+8y=0\\2x+y=1\end{cases}\xrightarrow{R_2+\frac12R_1\to R_2}\begin{cases}5x+8y=0\\4.5x+5y=1\end{cases} $$ — add a multiple of another row
- Matrices $A,B$ are **row-equivalent** if $B$ is reachable from $A$ by finitely many elementary row operations.

## Derivation Outline

1. Choose an operation that creates a zero below a leading coefficient.
2. Apply it; the solution set is unchanged because the operation is invertible.
3. Repeat until the matrix reaches [Echelon Form](../11%20-%20Linear%20Algebra/Echelon%20Form.md).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md), [Echelon Form](../11%20-%20Linear%20Algebra/Echelon%20Form.md), [Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md)
**Full Derivation:** 
