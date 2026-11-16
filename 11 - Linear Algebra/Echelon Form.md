---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

A staircase shape for a matrix, reached by elementary row operations, from which you can tell whether the system has no, one, or infinitely many solutions.

## Key Equation

$$
\begin{pmatrix}
*&\bullet&\bullet&\bullet&\bullet\\
0&*&\bullet&\bullet&\bullet\\
0&0&0&*&\bullet\\
0&0&0&0&0
\end{pmatrix}
$$

**Derived From:** definition — $*$ marks a leading coefficient (nonzero), $\bullet$ an arbitrary entry.

## Supporting Formulas

Definition (all three must hold):
- Zero rows appear at the bottom.
- Below each leading coefficient there is a column of zeros.
- Each leading coefficient lies to the right of the one in the row above.

Terms: the first nonzero entry of a row is its **pivot / leading coefficient**; its column holds a **dependent variable**; every other column holds a **free variable**. Dependent + free variables = number of columns.

Reading the solution from the augmented matrix:
- $$ \left(\begin{array}{ccc|c}*&*&*&*\\0&*&*&*\\0&0&0&a\end{array}\right),\ a\neq0 $$ — contradiction row → **no solution**.
- No contradiction row and free variables exist (#columns of coefficient matrix > #pivots) → **infinitely many solutions**.
- No contradiction row and every column has a pivot → **unique solution**.

## Derivation Outline

1. Bring the augmented matrix to echelon form with [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md).
2. Check for a contradiction row.
3. Count pivots versus unknowns.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md), [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md), [Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md)
**Full Derivation:** 
