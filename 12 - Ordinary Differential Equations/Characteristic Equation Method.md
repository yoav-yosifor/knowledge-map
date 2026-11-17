---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

A homogeneous linear ODE with constant coefficients is solved by trying $y=e^{\lambda x}$, which turns the ODE into a polynomial equation in $\lambda$ whose roots give the solutions.

## Key Equation

$$
\sum_{k=0}^{n}a_ky^{(k)}=y^{(n)}+a_{n-1}y^{(n-1)}+\cdots+a_1y'+a_0y=0\ \Longrightarrow\ \lambda^n+a_{n-1}\lambda^{n-1}+\cdots+a_1\lambda+a_0=0
$$

**Derived From:** assume $y=e^{\lambda x}$. Then $y'=\lambda e^{\lambda x}$, $y''=\lambda^2e^{\lambda x}$, …, $y^{(n)}=\lambda^ne^{\lambda x}$. Substituting and factoring out the common $e^{\lambda x}$ gives $e^{\lambda x}\left(\lambda^n+a_{n-1}\lambda^{n-1}+\cdots+a_1\lambda+a_0\right)=0$. The bracket is the characteristic polynomial; its roots $\lambda_i$ give the solutions $y_i(x)=e^{\lambda_ix}$. The source says that after seeing this once, the method is automatic.

## Supporting Formulas

- **Distinct real roots:** $y_i=e^{\lambda_ix}$.
- **Repeated root** ($\lambda_1=\lambda_2$): the solutions must be linearly independent, so the source takes $y_1=C_1e^{\lambda_1x}$, $y_2=C_2\,x\,e^{\lambda_2x}$ (stated without proof in the source).
- **Complex roots** $\lambda_{1,2}=a\pm ib$ (a root and its conjugate): $y=C_1e^{ax}\cos(bx)+C_2e^{ax}\sin(bx)$ (stated without proof; it follows from trigonometric identities).
- Example: $2y''-y'-y=0$ gives $2\lambda^2-\lambda-1=0$, $\lambda_1=1$, $\lambda_2=-\tfrac12$, so $y=C_1e^{x}+C_2e^{-x/2}$.
- Example: $y'''-y''-y'+y=0$ gives $\lambda^3-\lambda^2-\lambda+1=(\lambda^2-1)(\lambda-1)=0$, roots $\lambda_{1,2}=1$, $\lambda_3=-1$, so $y=C_1e^{x}+C_2xe^{x}+C_3e^{-x}$.
- Example: $y^{(4)}+5y'''-7y''-5y'+6y=0$ gives $\lambda^4+5\lambda^3-7\lambda^2-5\lambda+6=0$. $\lambda=1$ is a root, so divide by $(\lambda-1)$ to get $\lambda^3+6\lambda^2-\lambda-6=(\lambda+1)(\lambda-1)(\lambda+6)$. Roots: $\lambda_{1,2}=1$, $\lambda_3=-1$, $\lambda_4=-6$, so $y=C_1e^{x}+C_2xe^{x}+C_3e^{-x}+C_4e^{-6x}$.

## Derivation Outline

1. Classify the ODE as linear, homogeneous, constant coefficients, of order $n$.
2. Write the characteristic polynomial by replacing $y^{(k)}$ with $\lambda^k$.
3. Find its $n$ roots (guess one root, then divide the polynomial and factor the rest).
4. For each root, write the solution (distinct real, repeated, or complex pair) and take a linear combination.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE.md), [Higher-Order ODE Solutions](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20ODE%20Solutions.md), [Linear Independence](../11%20-%20Linear%20Algebra/Linear%20Independence.md)
**Full Derivation:** 
