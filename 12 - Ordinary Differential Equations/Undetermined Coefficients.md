---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

For a non-homogeneous linear ODE with constant coefficients whose right-hand side is a polynomial, an exponential, a sine or cosine (or a product or sum of these), guess a particular solution of the same type with unknown coefficients, then find the coefficients by substituting into the ODE. (The source calls this the guessing method.)

## Key Equation

$$
y=y_h+y_p,\qquad a_ny^{(n)}+\cdots+a_0y=g(x)
$$

**Derived From:** as for first-order ODEs, the solution is the homogeneous part plus a particular part. $y_h$ is found with the [characteristic equation](../12%20-%20Ordinary%20Differential%20Equations/Characteristic%20Equation%20Method.md); $y_p$ is guessed from a table according to the form of $g(x)$.

## Supporting Formulas

Basic table:

| $g(x)$ | guess $y_p$ |
|---|---|
| $P_n(x)$ (polynomial of degree $n$; a constant is degree 0) | polynomial of degree $n$, $Q_n(x)$ |
| $C\cdot e^{\lambda x}$ | $A\cdot e^{\lambda x}$ |
| $C\cos(\omega x)$ or $C\sin(\omega x)$ | $A\sin(\omega x)+B\cos(\omega x)$ |

Extended table (handles products and the overlap with $y_h$); $s$ is the multiplicity of the relevant root in the characteristic polynomial:

| $g(x)$ | guess $y_p$ |
|---|---|
| $P_n(x)$ | $x^{s}Q_n(x)$, $s$ = multiplicity of the root $\lambda=0$ |
| $C\cdot P_n(x)\cdot e^{\alpha x}$ | $x^{s}Q_n(x)\,e^{\alpha x}$, $s$ = multiplicity of the root $\lambda=\alpha$ (the source's table writes "$\lambda=\alpha,0$") |
| $C\,P_n(x)\,e^{\alpha x}\sin(\omega x)$ or $\cos(\omega x)$ | $x^{s}Q_{n,1}(x)e^{\alpha x}\sin(\omega x)+x^{s}Q_{n,2}(x)e^{\alpha x}\cos(\omega x)$, $s$ = total multiplicity of the roots $\lambda=\alpha\pm\omega i$ (the source's table also lists $\lambda=0$) |

- If a term of the guess already appears in $y_h$ (it is linearly dependent on the homogeneous solutions), multiply by $x$ until it is independent — this is the factor $x^{s}$.
- If $g(x)$ matches none of these forms, use [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md) (the source says this comes in the next tutorial).
- Example: $y''-y=\cos(2x)$. $y_h=C_1e^{x}+C_2e^{-x}$; guess $y_p=A\sin(2x)+B\cos(2x)$; substituting gives $-5A\sin(2x)-5B\cos(2x)=\cos(2x)$, so $A=0$, $B=-\tfrac15$, and $y=C_1e^{x}+C_2e^{-x}-\tfrac15\cos(2x)$.
- Example: $y''-2y'+2y=e^{x}$ with $y(0)=y'(0)=0$. Roots $\lambda=1\pm i$, $y_h=C_1e^{x}\cos x+C_2e^{x}\sin x$; guess $y_p=Ae^{x}$ gives $A=1$. The initial conditions give $C_1=-1$ and $C_2=0$, so $y=-e^{x}\cos x+e^{x}$.
- Example: $y''-4y'+4y=3+e^{2x}$. $y_h=C_1e^{2x}+C_2xe^{2x}$ (double root $\lambda=2$). The guess $A+Be^{2x}$ overlaps with $y_h$, and $A+Bxe^{2x}$ still does, so $y_p=A+Bx^2e^{2x}$. Substituting gives $2Be^{2x}+4A=e^{2x}+3$, so $B=\tfrac12$, $A=\tfrac34$, and $y=C_1e^{2x}+C_2xe^{2x}+\tfrac12x^2e^{2x}+\tfrac34$.

## Derivation Outline

1. Solve the homogeneous ODE (characteristic polynomial) to get $y_h$.
2. Choose the form of $y_p$ from the table, using the form of $g(x)$ and the roots of the characteristic polynomial.
3. Substitute $y_p$ into the ODE and compare with $g(x)$.
4. Find the constants and substitute them back into $y_p$.
5. Write $y=y_h+y_p$ (and use initial conditions if given).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Characteristic Equation Method](../12%20-%20Ordinary%20Differential%20Equations/Characteristic%20Equation%20Method.md), [Higher-Order ODE Solutions](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20ODE%20Solutions.md), [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md), [ODE Operator and Kernel](../12%20-%20Ordinary%20Differential%20Equations/ODE%20Operator%20and%20Kernel.md), [Initial Value Problem](../12%20-%20Ordinary%20Differential%20Equations/Initial%20Value%20Problem.md)
**Full Derivation:** 
