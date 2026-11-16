---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

A system of linear equations asks for the $n$-tuple $(x_1,\dots,x_n)$ satisfying all $m$ equations at once; it has either a unique solution, infinitely many, or none.

## Key Equation

$$
\begin{cases}
a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1\\
a_{21}x_1+a_{22}x_2+\cdots+a_{2n}x_n=b_2\\
\vdots\\
a_{m1}x_1+a_{m2}x_2+\cdots+a_{mn}x_n=b_m
\end{cases}
\iff A\mathbf{x}=\mathbf{b}
$$

**Derived From:** definition — the $a_{ij},b_i$ are constants from a field $\mathbb{F}$ ($\mathbb{C}$ or $\mathbb{R}$), the $x_j$ are the unknowns.

## Supporting Formulas

- $$ A=\begin{pmatrix}a_{11}&\cdots&a_{1n}\\ \vdots&\ddots&\vdots\\ a_{m1}&\cdots&a_{mn}\end{pmatrix},\quad \mathbf{x}=\begin{pmatrix}x_1\\ \vdots\\ x_n\end{pmatrix},\quad \mathbf{b}=\begin{pmatrix}b_1\\ \vdots\\ b_m\end{pmatrix} $$ — coefficient matrix, vector of unknowns, right-hand-side vector
- $$ \left(\begin{array}{ccc|c}a_{11}&\cdots&a_{1n}&b_1\\ \vdots&\ddots&\vdots&\vdots\\ a_{m1}&\cdots&a_{mn}&b_m\end{array}\right) $$ — augmented matrix (compact notation)
- $$ \begin{cases}5x+8y=0\\2x+y=1\end{cases}\ \longrightarrow\ \left(\begin{array}{cc|c}5&8&0\\2&1&1\end{array}\right),\quad \begin{pmatrix}5&8\\2&1\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix}=\begin{pmatrix}0\\1\end{pmatrix} $$ — worked example
- Homogeneous system: $b_j=0$ for all $j$.

## Derivation Outline

1. Rewrite the system as an augmented matrix.
2. Apply [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md) (they don't change the solution set) to simplify it.
3. Read off the solution(s) from the resulting [Echelon Form](../11%20-%20Linear%20Algebra/Echelon%20Form.md) / [Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Elementary Row Operations](../11%20-%20Linear%20Algebra/Elementary%20Row%20Operations.md), [Echelon Form](../11%20-%20Linear%20Algebra/Echelon%20Form.md), [Reduced Echelon Form](../11%20-%20Linear%20Algebra/Reduced%20Echelon%20Form.md)
**Full Derivation:** 
