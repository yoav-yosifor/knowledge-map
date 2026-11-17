---
tags:
  - ordinary-differential-equations
  - concept
---
---
## Core Idea

The Wronskian of $n$ functions is the determinant of the matrix of the functions and their derivatives; it is used to test whether solutions of a homogeneous linear ODE are linearly independent.

## Key Equation

$$
W=\begin{vmatrix}
y_1 & y_2 & \cdots & y_n\\
y_1' & y_2' & \cdots & y_n'\\
\vdots & \vdots & \ddots & \vdots\\
y_1^{(n-1)} & y_2^{(n-1)} & \cdots & y_n^{(n-1)}
\end{vmatrix},\qquad W\neq0\ \Rightarrow\ y_1,\dots,y_n \text{ linearly independent}
$$

**Derived From:** definition. The columns are the solutions and their derivatives (the first row has no derivatives, the second row first derivatives, …, the last row derivatives of order $n-1$). As in linear algebra, vectors are independent when the determinant is nonzero. An independent set of solutions is a basis of the solution space, so $y_h=c_1y_1+c_2y_2+\cdots+c_ny_n$.

## Supporting Formulas

- Example: show $y_1=x$, $y_2=\sqrt{x}$ are linearly independent on $(0,\infty)$:

  $$
  W=\begin{vmatrix}x&\sqrt{x}\\1&\tfrac{1}{2\sqrt{x}}\end{vmatrix}=x\cdot\frac{1}{2\sqrt{x}}-\sqrt{x}=-\frac{\sqrt{x}}{2}\neq0
  $$

- Because $y_1,\dots,y_n$ form a basis of the solution space, $W$ is invertible, so the system used in [higher-order variation of parameters](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20Variation%20of%20Parameters.md) has a unique solution.

## Derivation Outline

1. Take the $n$ solutions of the homogeneous ODE.
2. Build the matrix with the solutions in the top row and their derivatives (up to order $n-1$) below.
3. Compute the determinant; $W\neq0$ means the solutions are linearly independent.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Higher-Order ODE Solutions](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20ODE%20Solutions.md), [Higher-Order Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20Variation%20of%20Parameters.md), [Linear Independence](../11%20-%20Linear%20Algebra/Linear%20Independence.md), [Cramer's Rule](../11%20-%20Linear%20Algebra/Cramer%27s%20Rule.md)
**Full Derivation:** 
