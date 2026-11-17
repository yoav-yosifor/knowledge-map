---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

When an ODE $P\,dx+Q\,dy=0$ is not exact, one can look for a function $\mu$ that, when multiplied through the whole equation, makes it exact.

## Key Equation

$$
\mu(x)=e^{\int\frac{P_y-Q_x}{Q}\,dx}\qquad\Big|\qquad \mu(y)=e^{\int\frac{Q_x-P_y}{P}\,dy}
$$

**Derived From:** requiring that $\mu P\,dx+\mu Q\,dy=0$ be exact, i.e. $(\mu P)_y=(\mu Q)_x$, and assuming $\mu$ depends on only one variable; the steps are in [Integrating Factor Derivation](../12%20-%20Ordinary%20Differential%20Equations/Integrating%20Factor%20Derivation.md).

## Supporting Formulas

- Use when $P_y\neq Q_x$ (the ODE is not exact, i.e. $F_{xy}\neq F_{yx}$).
- The expression $\dfrac{P_y-Q_x}{Q}$ (or $\dfrac{Q_x-P_y}{P}$) must depend on **only one** of the variables, otherwise the corresponding $\mu$ cannot be found this way.
- After multiplying: $\mu P\,dx+\mu Q\,dy=0$ with $(\mu P)_y=(\mu Q)_x$, then continue as for an [exact ODE](../12%20-%20Ordinary%20Differential%20Equations/Exact%20ODE.md).

## Derivation Outline

1. Check whether $P_y=Q_x$. If it does not, look for an integrating factor.
2. Compute $\dfrac{P_y-Q_x}{Q}$; if it depends only on $x$, use $\mu(x)$. Otherwise compute $\dfrac{Q_x-P_y}{P}$ and check that it depends only on $y$.
3. Compute $\mu$ from the formula and multiply the ODE by it.
4. Verify that $(\mu P)_y=(\mu Q)_x$, and solve the resulting exact ODE.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Exact ODE](../12%20-%20Ordinary%20Differential%20Equations/Exact%20ODE.md), [Linear ODE Solution Formula](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE%20Solution%20Formula.md)
**Full Derivation:** [Integrating Factor Derivation](../12%20-%20Ordinary%20Differential%20Equations/Integrating%20Factor%20Derivation.md)
