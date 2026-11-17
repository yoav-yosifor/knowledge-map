---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

A Bernoulli equation is a first-order ODE that is linear except for a power of $y$ on the right-hand side; the substitution $z=y^{1-n}$ turns it into a first-order linear ODE.

## Key Equation

$$
y'+a(x)\,y=b(x)\,y^{n},\quad n\neq0,1\ \xrightarrow{\ z=y^{1-n}\ }\ z'+(1-n)\,a(x)\,z=(1-n)\,b(x)
$$

**Derived From:** assume $y\neq0$ and divide by $y^{n}$ to get $\dfrac{y'}{y^{n}}+a(x)\,y^{1-n}=b(x)$. With $z=y^{1-n}$, $z'=(1-n)\dfrac{y'}{y^{n}}$, which gives $\dfrac{z'}{1-n}+a(x)\,z=b(x)$, equivalent to the key equation.

## Supporting Formulas

- Solve the linear ODE for $z$ (e.g. with the [linear ODE solution formula](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE%20Solution%20Formula.md)), then recover $y=z^{\frac{1}{1-n}}$.
- Example: $y'+2y=y^{2}e^{x}$ has $a=2$, $b=e^{x}$, $n=2$. With $z=\dfrac1y$ the equation becomes $z'-2z=-e^{x}$, which gives $z=Ce^{2x}+e^{x}$, so $y=\dfrac{1}{Ce^{2x}+e^{x}}$.

## Derivation Outline

1. Check that the ODE has the form $y'+a(x)y=b(x)y^{n}$ with $n\neq0,1$.
2. Substitute $z=y^{1-n}$ and differentiate.
3. Get the linear ODE $z'+(1-n)a(x)z=(1-n)b(x)$.
4. Solve for $z$, then substitute back to get $y$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [First-Order Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/First-Order%20Linear%20ODE.md), [Linear ODE Solution Formula](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE%20Solution%20Formula.md), [Linear Argument Substitution](../12%20-%20Ordinary%20Differential%20Equations/Linear%20Argument%20Substitution.md)
**Full Derivation:** 
