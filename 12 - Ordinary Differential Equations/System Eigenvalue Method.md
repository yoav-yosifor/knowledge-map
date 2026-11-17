---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

A homogeneous linear system with constant coefficients has solutions of the form (constant vector) times $e^{\lambda t}$, where $\lambda$ and the vector are an eigenvalue and eigenvector of the coefficient matrix.

## Key Equation

$$
\begin{pmatrix}x\\y\end{pmatrix}=c_1\vec v_1e^{\lambda_1t}+c_2\vec v_2e^{\lambda_2t},\qquad \det(P-\lambda I)=0
$$

**Derived From:** try $x=\alpha e^{\lambda t}$, $y=\beta e^{\lambda t}$, so $x'=\alpha\lambda e^{\lambda t}$, $y'=\beta\lambda e^{\lambda t}$. Substituting into the system and dividing by $e^{\lambda t}$ gives $\lambda\begin{pmatrix}\alpha\\ \beta\end{pmatrix}=P\begin{pmatrix}\alpha\\ \beta\end{pmatrix}$, where $P$ is the coefficient matrix. Nontrivial solutions exist when $\Delta=\det(P-\lambda I)=0$; each eigenvalue $\lambda_i$ gives an eigenvector $\vec v_i=(\alpha,\beta)^{T}$.

## Supporting Formulas

- Find the eigenvalues from the determinant $\Delta=0$, then for each eigenvalue solve $(P-\lambda I)\vec v=0$ for the eigenvector.
- The initial conditions fix $c_1,c_2$ (the source does this by row-reducing a matrix).
- Example: $x'=2x+y$, $y'=3x+4y$, $x(0)=2$, $y(0)=2$.
  - $P=\begin{pmatrix}2&1\\3&4\end{pmatrix}$, $\Delta=\begin{vmatrix}2-\lambda&1\\3&4-\lambda\end{vmatrix}=\lambda^2-6\lambda+5=0$, so $\lambda_1=1$, $\lambda_2=5$.
  - $\lambda_1=1$: $\alpha+\beta=0$, $\vec v_1=\begin{pmatrix}1\\-1\end{pmatrix}$. $\lambda_2=5$: $-3\alpha+\beta=0$, $\vec v_2=\begin{pmatrix}1\\3\end{pmatrix}$.
  - General solution: $\begin{pmatrix}x\\y\end{pmatrix}=c_1\begin{pmatrix}1\\-1\end{pmatrix}e^{t}+c_2\begin{pmatrix}1\\3\end{pmatrix}e^{5t}$; the initial conditions give $c_1=c_2=1$, so $x(t)=e^{t}+e^{5t}$, $y(t)=-e^{t}+3e^{5t}$.

## Derivation Outline

1. Write the system in matrix form with coefficient matrix $P$.
2. Substitute $x=\alpha e^{\lambda t}$, $y=\beta e^{\lambda t}$ and cancel $e^{\lambda t}$.
3. Solve $\det(P-\lambda I)=0$ for the eigenvalues.
4. For each eigenvalue, solve for the eigenvector.
5. Form the general solution as a linear combination and fit the initial conditions.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [ODE Systems](../12%20-%20Ordinary%20Differential%20Equations/ODE%20Systems.md), [System Elimination Method](../12%20-%20Ordinary%20Differential%20Equations/System%20Elimination%20Method.md), [Characteristic Equation Method](../12%20-%20Ordinary%20Differential%20Equations/Characteristic%20Equation%20Method.md), [Matrices](../11%20-%20Linear%20Algebra/Matrices.md), [Linear Systems](../11%20-%20Linear%20Algebra/Linear%20Systems.md)
**Full Derivation:** 
