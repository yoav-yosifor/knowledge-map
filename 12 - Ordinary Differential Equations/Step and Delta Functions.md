---
tags:
  - ordinary-differential-equations
  - concept
---
---
## Core Idea

The step function switches from 0 to 1 at a chosen time, and the Dirac delta is an ideal instantaneous pulse; both are used as forcing terms in ODEs and have simple Laplace transforms.

## Key Equation

$$
u(t)=\begin{cases}1&t\ge0\\0&t<0\end{cases},\qquad \int_{-\infty}^{\infty}\delta(t)\,dt=1,\qquad \mathcal{L}\{\delta(t-a)\}=e^{-as}
$$

**Derived From:** definitions as given in the source.

## Supporting Formulas

- **Step function** $u(t)$ can be shifted: $u_1=u(t-1)$, $u_2=u(t-2)$. The difference $u_1-u_2$ is a window function (1 between $t=1$ and $t=2$, 0 elsewhere).
- **Dirac delta** $\delta(t)$: an ideal, instantaneous, powerful pulse at exactly $t=0$; $\delta(t=0)=\infty$, but its integral (the area under it) equals 1.
- **Sampling property:** $\displaystyle\int_{-\infty}^{\infty}f(t)\,\delta(t-a)\,dt=f(a)$.
- **Laplace transform of delta:** $\mathcal{L}\{\delta(t)\}=1$, and of the shifted delta: $\mathcal{L}\{\delta(t-a)\}=e^{-as}$.
- **Use in ODEs:** represents a momentary excitation of a system, an immediate initial condition or an immediate response; allows a simple solution in the Laplace domain even when ordinary differentiation is not possible.
- The step function appears in the [shift-in-$t$ property](../12%20-%20Ordinary%20Differential%20Equations/Laplace%20Transform.md): $e^{-as}F(s)=\mathcal{L}\left(u(t-a)\,y(t-a)\right)$.

## Derivation Outline

1. Define $u(t)$ and shift it to $u(t-a)$ to start the step at time $a$.
2. Subtract two shifted steps to get a window.
3. For an instantaneous input at time $a$, use $\delta(t-a)$; its transform is $e^{-as}$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Laplace Transform](../12%20-%20Ordinary%20Differential%20Equations/Laplace%20Transform.md), [Laplace Transform Method](../12%20-%20Ordinary%20Differential%20Equations/Laplace%20Transform%20Method.md)
**Full Derivation:** 
