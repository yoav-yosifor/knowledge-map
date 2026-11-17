---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

A first-order ODE whose right-hand side depends only on the ratio $y/x$ becomes separable under the substitution $z=y/x$. (This is a different use of "homogeneous" than a linear ODE with zero right-hand side.)

## Key Equation

$$
y'=g\!\left(\frac{y}{x}\right)\ \xrightarrow{\ z=y/x\ }\ \int\frac{1}{g(z)-z}\,dz=\ln|x|+C
$$

**Derived From:** with $z=y/x$ we have $zx=y$, so $y'=z'x+z$. Then $g(z)=z'x+z$, i.e. $xz'=g(z)-z$, which separates to $\dfrac{dz}{g(z)-z}=\dfrac{dx}{x}$. Integrating gives the key equation (the source says it can be used directly as a formula).

## Supporting Formulas

- After finding $z$, do not stop: the solution is $y=x\cdot z$.
- Example 1: $y'=\dfrac{y}{x}+1$ has $g(z)=z+1$, so $\int\dfrac{dz}{z+1-z}=z=\ln|x|+c$ and $y=x\ln|x|+c\,x$.
- Example 2: $xy'=x\sqrt[x]{e^{y}}+y$ with $y(1)=3$ becomes $y'=e^{y/x}+\dfrac{y}{x}$, so $g(z)=e^{z}+z$ and $-e^{-z}=\ln|x|+C$. This gives $y=-x\ln(C-\ln|x|)$, and the initial condition gives $C=e^{-3}$, so $y=-x\ln\!\left(e^{-3}-\ln|x|\right)$.

## Derivation Outline

1. Check that the ODE has the form $y'=g(y/x)$ (divide by $x$ if needed).
2. Substitute $z=y/x$, so $y'=z'x+z$.
3. Rearrange to $xz'=g(z)-z$ and separate variables.
4. Integrate, then substitute back $y=x\cdot z$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Separation of Variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md), [Linear Argument Substitution](../12%20-%20Ordinary%20Differential%20Equations/Linear%20Argument%20Substitution.md), [Initial Value Problem](../12%20-%20Ordinary%20Differential%20Equations/Initial%20Value%20Problem.md)
**Full Derivation:** 
