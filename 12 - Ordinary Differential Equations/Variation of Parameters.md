---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

To solve a non-homogeneous first-order linear ODE, solve the homogeneous equation first, then let the constant in that solution become an unknown function of $x$ and find what that function must be.

## Key Equation

$$
y=y_h+y_p
$$

**Derived From:** the source's method — the solution is the sum of the homogeneous solution $y_h$ and a particular non-homogeneous part $y_p$, where $y_p$ is found by replacing the constant $C$ in $y_h$ with a differentiable function $C(x)$, substituting into the full ODE, and solving for $C(x)$.

## Supporting Formulas

- Worked example, $y'+\dfrac{1}{x}y=x$:
  - Homogeneous part: $y'+\dfrac1xy=0$ is separable and gives $y_h=\dfrac{C}{x}$.
  - Substituting $y=\dfrac{C(x)}{x}$ into the full ODE (using the quotient rule) gives $\dfrac{C'(x)}{x}=x$, so $C'(x)=x^2$ and $C(x)=\dfrac{x^3}{3}$.
  - So $y_p=\dfrac{x^2}{3}$ and $y=y_h+y_p=\dfrac{C}{x}+\dfrac{x^2}{3}$.

## Derivation Outline

1. Identify a [first-order linear ODE](../12%20-%20Ordinary%20Differential%20Equations/First-Order%20Linear%20ODE.md) with $b(x)\neq0$.
2. Solve the homogeneous equation (by [separation of variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md)) to get $y_h$ with a constant $C$.
3. Replace $C$ by a function $C(x)$ and substitute into the non-homogeneous ODE.
4. Solve for $C(x)$ and form $y_p$.
5. Write $y=y_h+y_p$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [First-Order Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/First-Order%20Linear%20ODE.md), [Separation of Variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md), [General and Particular Solutions](../12%20-%20Ordinary%20Differential%20Equations/General%20and%20Particular%20Solutions.md), [Linear ODE Solution Formula](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE%20Solution%20Formula.md)
**Full Derivation:** 
