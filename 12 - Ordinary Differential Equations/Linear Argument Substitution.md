---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

An ODE of the form $y'=f(ax+by+c)$ is not separable as written, but the substitution $z=ax+by+c$ turns it into a separable ODE in $z$, which is solved and then substituted back to recover $y$.

## Key Equation

$$
y'=f(ax+by+c)\ \xrightarrow{\ z=ax+by+c\ }\ z'=b\,f(z)+a
$$

**Derived From:** defining $z=ax+by+c$ and differentiating with respect to $x$ gives $z'=a+by'$; substituting $y'=f(z)$ gives $z'=b\,f(z)+a$, which is separable in $z$.

## Supporting Formulas

- $$ \int\frac{dz}{b\,f(z)+a}=\int dx + C $$ — general solution in terms of $z$; then substitute back $z=ax+by+c$ to find $y$.
- Example: $y'=(x+y+1)^2$ with $z=x+y+1$ gives $z'=z^2+1$, then $\arctan(z)=x+C$, so $y=\tan(x+c)-x-1$.

## Derivation Outline

1. Define $z=ax+by+c$.
2. Differentiate with respect to $x$: $z'=a+by'$.
3. Substitute $y'=f(z)$ to get $z'=b\,f(z)+a$, a [separable ODE](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md).
4. Separate and integrate, then substitute back to find $y$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Separation of Variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md), [Homogeneous First-Order ODE](../12%20-%20Ordinary%20Differential%20Equations/Homogeneous%20First-Order%20ODE.md)
**Full Derivation:** 
