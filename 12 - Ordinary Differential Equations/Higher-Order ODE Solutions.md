---
tags:
  - ordinary-differential-equations
  - concept
---
---
## Core Idea

The general solution of an $n$-th order linear ODE has as many constants as the order, and it is built as the homogeneous solution (a linear combination of independent solutions) plus one particular solution.

## Key Equation

$$
y=y_h+y_p,\qquad y_h=\sum_iC_iy_i
$$

**Derived From:** the source's solution recipe. The number of constants in the solution equals the order of the ODE (unlike first-order ODEs, which always showed one constant). The set of solutions of the homogeneous ODE is a vector subspace, so a linear combination of solutions is again a solution, and the $y_i$ must be linearly independent. The same principle is behind the variation of parameters formula.

## Supporting Formulas

- Order $n$ $\Rightarrow$ $n$ constants in the general solution.
- Solutions of the homogeneous ODE form a [vector subspace](../11%20-%20Linear%20Algebra/Subspaces.md); the $y_i$ must be [linearly independent](../11%20-%20Linear%20Algebra/Linear%20Independence.md), and $y_h$ is a [linear combination](../11%20-%20Linear%20Algebra/Linear%20Combinations.md) of them.
- Always, in this order:
  - find the homogeneous solutions $y_h=\sum_iC_iy_i$;
  - find a particular solution $y_p$ of the non-homogeneous ODE;
  - the full solution is $y=y_h+y_p$;
  - if there are initial conditions, find the constants by substituting them.

## Derivation Outline

1. Solve the homogeneous ODE to get $y_h$ with $n$ independent solutions.
2. Find one particular solution $y_p$ of the full ODE.
3. Add them: $y=y_h+y_p$.
4. Use initial conditions to fix the $n$ constants.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE.md), [Variation of Parameters](../12%20-%20Ordinary%20Differential%20Equations/Variation%20of%20Parameters.md), [General and Particular Solutions](../12%20-%20Ordinary%20Differential%20Equations/General%20and%20Particular%20Solutions.md), [Characteristic Equation Method](../12%20-%20Ordinary%20Differential%20Equations/Characteristic%20Equation%20Method.md), [ODE Order Reduction](../12%20-%20Ordinary%20Differential%20Equations/ODE%20Order%20Reduction.md)
**Full Derivation:** 
