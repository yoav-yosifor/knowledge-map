---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

For a non-homogeneous linear ODE of any order whose right-hand side is not in the guessing table, take the homogeneous solution, let each constant become a function $c_k(x)$, and find those functions by solving a linear system with the Wronskian matrix.

## Key Equation

$$
y_p=c_1(x)y_1+c_2(x)y_2,\qquad
\begin{bmatrix}y_1&y_2\\y_1'&y_2'\end{bmatrix}\begin{bmatrix}c_1'(x)\\c_2'(x)\end{bmatrix}=\begin{bmatrix}0\\ \dfrac{g(x)}{\alpha_2(x)}\end{bmatrix}
$$

**Derived From:** the source's setup for $\sum_{i=0}^{n}\alpha_i(x)y^{(i)}=g(x)$, written for order 2 for simplicity (it holds for higher orders too). If $y_h=c_1y_1+c_2y_2$, we look for $y_p$ with the constants replaced by functions. The number of constants equals the order $n$ (the number of independent homogeneous solutions), and with many unknowns a matrix is natural. Since $y_1,\dots,y_n$ are a basis of the solution space, the [Wronskian](../12%20-%20Ordinary%20Differential%20Equations/Wronskian.md) matrix $W$ is invertible, so the system has a unique solution.

## Supporting Formulas

- By [Cramer's rule](../11%20-%20Linear%20Algebra/Cramer%27s%20Rule.md): $c_k'(x)=\dfrac{|W_k|}{|W|}$, where $W_k$ is $W$ with column $k$ replaced by the vector $\left(0,\dots,0,\dfrac{g(x)}{\alpha_n(x)}\right)^{T}$.
- For order 2:

  $$
  c_1'(x)=\frac{W_1}{W}=\begin{vmatrix}0&y_2\\ \frac{g(x)}{\alpha_n(x)}&y_2'\end{vmatrix}\cdot\frac{1}{|W|},\qquad
  c_2'(x)=\frac{W_2}{W}=\begin{vmatrix}y_1&0\\ y_1'&\frac{g(x)}{\alpha_n(x)}\end{vmatrix}\cdot\frac{1}{|W|}
  $$

- Then integrate $c_1',c_2'$ to get $c_1(x),c_2(x)$, form $y_p=c_1(x)y_1+c_2(x)y_2$, and $y=y_h+y_p$.
- Example: $y''-2y'+y=e^{x}\ln x$.
  - Homogeneous: $\lambda^2-2\lambda+1=0$, $\lambda_{1,2}=1$, so $y_h=c_1e^{x}+c_2xe^{x}$.
  - $W=\begin{vmatrix}e^{x}&xe^{x}\\e^{x}&(1+x)e^{x}\end{vmatrix}=e^{2x}$, $w_1=-xe^{2x}\ln x$, $w_2=e^{2x}\ln x$.
  - $c_1'=-x\ln x$, $c_2'=\ln x$, so $c_1=\dfrac{x^2}{4}-\dfrac{x^2\ln x}{2}$, $c_2=x\ln x-x$.
  - $y_p=x^2e^{x}\left(\dfrac{\ln x}{2}-\dfrac34\right)$ and $y=C_1e^{x}+C_2xe^{x}+\dfrac{x^2e^{x}}{2}\left(\ln x-\dfrac32\right)$.

## Derivation Outline

1. Solve the homogeneous ODE and get independent $y_1,\dots,y_n$.
2. Write $y_p=\sum_kc_k(x)y_k$.
3. Compute $W$ and each $W_k$ (replace column $k$ by $\left(0,\dots,0,g/\alpha_n\right)^T$).
4. Compute $c_k'=W_k/W$ and integrate to get $c_k(x)$.
5. Form $y_p$ and write $y=y_h+y_p$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md), [Wronskian](../12%20-%20Ordinary%20Differential%20Equations/Wronskian.md), [Undetermined Coefficients](../12%20-%20Ordinary%20Differential%20Equations/Undetermined%20Coefficients.md), [Higher-Order ODE Solutions](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20ODE%20Solutions.md), [Cramer's Rule](../11%20-%20Linear%20Algebra/Cramer%27s%20Rule.md)
**Full Derivation:** 
