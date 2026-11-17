---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

A shortcut formula, taken from the formula sheet, gives the solution of a first-order linear ODE directly, instead of going through the homogeneous solution and variation of parameters step by step.

## Key Equation

$$
y'+a(x)\,y=b(x)\ \Longrightarrow\ y=e^{-A(x)}\left(C+\int b(x)\,e^{A(x)}\,dx\right),\qquad A(x)=\int a(x)\,dx
$$

**Derived From:** formula sheet (the source states it as a shortcut for the [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md) route; no derivation is given in the source).

## Supporting Formulas

- Worked example, $y'+\dfrac1xy=x$: $a(x)=\dfrac1x$ so $A(x)=\ln x$; $b(x)=x$; $e^{A(x)}=x$ and $e^{-A(x)}=x^{-1}$. Then $y=\dfrac1x\left[\int x\cdot x\,dx+C\right]=\dfrac1x\left[\dfrac{x^3}{3}+C\right]=\dfrac{x^2}{3}+\dfrac{C}{x}$, the same result as variation of parameters.

## Derivation Outline

1. Put the ODE in the form $y'+a(x)y=b(x)$.
2. Compute $A(x)=\int a(x)\,dx$.
3. Plug $a$, $b$ and $A$ into the formula and do the one remaining integral.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [First-Order Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/First-Order%20Linear%20ODE.md), [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md), [Bernoulli Equation](../12%20-%20Ordinary%20Differential%20Equations/Bernoulli%20Equation.md)
**Full Derivation:** 
