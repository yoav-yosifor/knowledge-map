---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

The Laplace transform is an integral transform from the time domain ($t$) to the Laplace (frequency) domain ($s$) that turns derivatives into algebraic operations, so a differential equation becomes an algebraic equation.

## Key Equation

$$
X(s)=\mathcal{L}\{x(t)\}=\int_0^{\infty}x(t)\,e^{-st}\,dt
$$

**Derived From:** definition. It replaces a function of $t$ by a function of $s$ (time domain to frequency domain). The source writes the inverse transform as $x(t)=\mathcal{L}^{-1}\{X(s)\}=\int_0^{\infty}X(s)\,e^{st}\,ds$; this is transcribed as given, and the source says to use it by reading known pairs off the formula sheet rather than evaluating that integral.

## Supporting Formulas

Properties (from the formula sheet):

- **Uniqueness:** if $y_1,y_2$ are continuous and $\mathcal{L}(y_1)=\mathcal{L}(y_2)$, then $y_1=y_2$.
- **Linearity:** $\mathcal{L}(y_1+ay_2)=\mathcal{L}(y_1)+a\mathcal{L}(y_2)$.
- **First derivative:** $\mathcal{L}(y')=s\mathcal{L}(y)-y(0)$.
- **$n$-th derivative:** $\mathcal{L}\!\left(y^{(n)}\right)=s^n\mathcal{L}(y)-s^{n-1}y(0)-\cdots-sy^{(n-2)}(0)-y^{(n-1)}(0)$.
- **Derivative of the transform:** $\mathcal{L}(ty)=-F'(s)$, where $F(s)=\mathcal{L}(y)$.
- **Shift in $s$:** if $F(s)=\mathcal{L}(y)$, then $F(s-a)=\mathcal{L}\!\left(e^{at}y(t)\right)$.
- **Shift in $t$:** if $F(s)=\mathcal{L}(y)$, then $e^{-as}F(s)=\mathcal{L}\!\left(u(t-a)\,y(t-a)\right)$, with $u$ the [step function](../12%20-%20Ordinary%20Differential%20Equations/Step%20and%20Delta%20Functions.md).

Known transforms (from the formula sheet):

| $x(t)$ | $\mathcal{L}\{x(t)\}$ |
|---|---|
| $1$ | $\dfrac1s$ |
| $t^n$ | $\dfrac{n!}{s^{n+1}}$ |
| $\sin(at)$ | $\dfrac{a}{s^2+a^2}$ |
| $\cos(at)$ | $\dfrac{s}{s^2+a^2}$ |
| $e^{at}$ | $\dfrac{1}{s-a}$ |
| $\delta(t-a)$ | $e^{-sa}$ |

Inverse pairs used in the source's examples: $\mathcal{L}^{-1}\!\left\{\dfrac{1}{s^2+1}\right\}=\sin t$ and $\mathcal{L}^{-1}\!\left\{e^{-as}F(s)\right\}=f(t-a)\,u(t-a)$.

## Derivation Outline

1. Apply the transform to the function of $t$ to get a function of $s$.
2. Use linearity and the derivative rule to convert derivatives into powers of $s$ (initial conditions appear automatically).
3. Invert using the table and the shift rules.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Laplace Transform Method](../12%20-%20Ordinary%20Differential%20Equations/Laplace%20Transform%20Method.md), [Step and Delta Functions](../12%20-%20Ordinary%20Differential%20Equations/Step%20and%20Delta%20Functions.md), [Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE.md)
**Full Derivation:** 
