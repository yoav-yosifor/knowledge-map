---
tags:
  - ordinary-differential-equations
  - concept
---
---
## Core Idea

A first-order linear ODE can always be normalized so that the coefficient of $y'$ is 1; it is homogeneous when the right-hand side is zero and non-homogeneous otherwise.

## Key Equation

$$
y'+a(x)\,y=b(x)
$$

**Derived From:** the general form $\alpha(x)y'+\beta(x)y=\gamma(x)$. As long as $\alpha(x)\neq 0$, divide through by $\alpha(x)$ and define $a(x)=\dfrac{\beta(x)}{\alpha(x)}$, $b(x)=\dfrac{\gamma(x)}{\alpha(x)}$.

## Supporting Formulas

- $a(x)$ is the coefficient of the function itself; $b(x)$ is some function of $x$.
- $$ b(x)=0 $$ — first-order linear, **homogeneous**; solved as a [separable ODE](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md).
- $$ b(x)\neq 0 $$ — first-order linear, **non-homogeneous**; can be solved by several methods, for example [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md).

## Derivation Outline

1. Write the ODE as $\alpha(x)y'+\beta(x)y=\gamma(x)$.
2. Divide by $\alpha(x)\neq0$.
3. Rename the coefficients $a(x)$ and $b(x)$ to reach $y'+a(x)y=b(x)$.
4. Check whether $b(x)=0$ to decide which method applies.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE.md), [Separation of Variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md), [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md), [Linear ODE Solution Formula](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE%20Solution%20Formula.md)
**Full Derivation:** 
