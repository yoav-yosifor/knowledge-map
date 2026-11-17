---
tags:
  - ordinary-differential-equations
  - concept
---
---
## Core Idea

A system of ODEs is a set of coupled differential equations for several unknown functions at once, and in the linear first-order case each derivative is a linear combination of all the unknowns plus a function of $t$.

## Key Equation

$$
\begin{cases}x'=a_{11}x+a_{12}y+f_1(t)\\ y'=a_{21}x+a_{22}y+f_2(t)\end{cases}
$$

**Derived From:** definition (the source writes the general linear first-order system for two unknowns $x$ and $y$).

## Supporting Formulas

- General system of $n$ first-order ODEs: $x_i'=f(t,x_1,\dots,x_n)$, $i=1,\dots,n$.
- Linear first-order system: $x_i'=a_1x_1+\dots+a_nx_n+f_i(t)$, $i=1,\dots,n$.
- Two methods for solving a linear system appear in the source: [System Elimination Method](../12%20-%20Ordinary%20Differential%20Equations/System%20Elimination%20Method.md) (reduce to one higher-order ODE) and the [System Eigenvalue Method](../12%20-%20Ordinary%20Differential%20Equations/System%20Eigenvalue%20Method.md) (eigenvalues and eigenvectors of the coefficient matrix).

## Derivation Outline

1. Identify the unknown functions $x_1(t),\dots,x_n(t)$.
2. Write each derivative as a function (or linear combination) of the unknowns.
3. Choose a solution method and use the initial conditions to fix the constants.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE.md), [System Elimination Method](../12%20-%20Ordinary%20Differential%20Equations/System%20Elimination%20Method.md), [System Eigenvalue Method](../12%20-%20Ordinary%20Differential%20Equations/System%20Eigenvalue%20Method.md), [Initial Value Problem](../12%20-%20Ordinary%20Differential%20Equations/Initial%20Value%20Problem.md)
**Full Derivation:** 
