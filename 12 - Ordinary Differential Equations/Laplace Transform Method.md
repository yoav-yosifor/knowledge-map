---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

To solve a linear ODE with initial conditions, transform it to the Laplace domain, solve the resulting algebraic equation for $Y(s)$, and transform back; the initial conditions are built in from the start.

## Key Equation

$$
\mathcal{L}\{\text{ODE}\}\ \Longrightarrow\ \text{algebraic equation for }Y(s)\ \Longrightarrow\ y(t)=\mathcal{L}^{-1}\{Y(s)\}
$$

**Derived From:** the source's three-step method:

1. Apply the [Laplace transform](../12%20-%20Ordinary%20Differential%20Equations/Laplace%20Transform.md) to both sides of the ODE (functions of $t$ become functions of $s$).
2. Solve the algebraic equation in the frequency domain (derivatives became algebraic operations).
3. Apply the inverse transform to get the solution in the time domain.

## Supporting Formulas

- The difficulty moves from calculus to algebra: partial fractions, common denominators, and so on.
- Advantage: no need to split into homogeneous and non-homogeneous parts, or to find the general solution and then fit the constants to the initial conditions — everything is accounted for from the first step, so the result is exactly the function that solves the ODE.
- Works even for forcing terms that are not differentiable in the time domain (for example a delta function).
- Example 1: $y''+y=\delta(t-\pi)$, $y(0)=0$, $y'(0)=0$. Transforming: $\left(s^2Y-sy(0)-y'(0)\right)+Y=e^{-\pi s}$, so $Y(s)=\dfrac{e^{-\pi s}}{s^2+1}$ and $y(t)=\sin(t-\pi)\,u(t-\pi)$.
- Example 2: $y''-5y'+4y=e^{3t}$, $y(0)=2$, $y'(0)=-3$.
  - Transform: $s^2Y-2s+3-5(sY-2)+4Y=\dfrac{1}{s-3}$, so $Y(s)\left(s^2-5s+4\right)=\dfrac{1}{s-3}+2s-13$.
  - Common denominator: $Y(s)=\dfrac{1+(2s-13)(s-3)}{(s-3)(s-4)(s-1)}=\dfrac{2s^2-19s+40}{(s-3)(s-4)(s-1)}$.
  - Partial fractions $\dfrac{A}{s-3}+\dfrac{B}{s-4}+\dfrac{C}{s-1}$, matching coefficients: $A+B+C=2$, $-5A-4B-7C=-19$, $4A+3B+12C=40$, giving $A=-\tfrac12$, $B=-\tfrac43$, $C=\tfrac{23}{6}$.
  - Inverse: $y(t)=-\tfrac12e^{3t}-\tfrac43e^{4t}+\tfrac{23}{6}e^{t}$ (the source writes the middle coefficient as $-1\tfrac13$).

## Derivation Outline

1. Transform the ODE, using linearity and $\mathcal{L}(y^{(n)})$ with the given initial conditions.
2. Isolate $Y(s)$.
3. Rewrite $Y(s)$ with a common denominator and decompose it into partial fractions (solve for the coefficients by multiplying out and matching powers of $s$).
4. Invert term by term using the table.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Laplace Transform](../12%20-%20Ordinary%20Differential%20Equations/Laplace%20Transform.md), [Step and Delta Functions](../12%20-%20Ordinary%20Differential%20Equations/Step%20and%20Delta%20Functions.md), [Initial Value Problem](../12%20-%20Ordinary%20Differential%20Equations/Initial%20Value%20Problem.md), [Undetermined Coefficients](../12%20-%20Ordinary%20Differential%20Equations/Undetermined%20Coefficients.md)
**Full Derivation:** 
