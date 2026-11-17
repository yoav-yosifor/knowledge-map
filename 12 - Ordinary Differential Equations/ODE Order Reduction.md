---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

When the zeroth-order term $y$ does not appear in a higher-order ODE, the substitution $p=y'$ lowers its order by one, so it can be solved with first-order methods and then integrated back to find $y$.

## Key Equation

$$
y'=p,\qquad y''=p'
$$

**Derived From:** the source's method — substitute into the original ODE to get a first-order ODE in $p(x)$, solve it, then return to the definition $y'=p$ and integrate to find $y$.

## Supporting Formulas

- Works for both homogeneous and non-homogeneous ODEs, as long as $y$ itself does not appear.
- Example (homogeneous): $xy''=y'$ becomes $xp'=p$, which is separable: $\dfrac1p\,dp=\dfrac1x\,dx$, so $\ln p=\ln x+C$ and $p=Cx$. Then $y'=Cx$ gives $y=C_1x^2+C_2$.
- Example (non-homogeneous): $xy''+y'=4x$ becomes $x\,p'+p=4x$, i.e. $p'+\dfrac1xp=4$. With the [linear ODE solution formula](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE%20Solution%20Formula.md): $a(x)=\dfrac1x$, $b(x)=4$, $A(x)=\ln|x|$, so $p=\dfrac1x\left(C+2x^2\right)=2x+\dfrac{C}{x}$. Then $y'=p$ gives $y=x^2+C_1\ln|x|+C_2$.
- Finding $p$ is not enough — the last step is always to integrate $y'=p$.

## Derivation Outline

1. Check that $y$ itself does not appear in the ODE.
2. Substitute $y'=p$, $y''=p'$ to get a first-order ODE in $p$.
3. Solve for $p$ (e.g. [separation of variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md) or the linear ODE formula).
4. Return to $y'=p$ and integrate to get $y$ (a second constant appears).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Separation of Variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md), [Linear ODE Solution Formula](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE%20Solution%20Formula.md), [ODE Order and Degree](../12%20-%20Ordinary%20Differential%20Equations/ODE%20Order%20and%20Degree.md), [Higher-Order ODE Solutions](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20ODE%20Solutions.md)
**Full Derivation:** 
