---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Once a driven atom has settled into steady state, how strongly it is excited depends on a single dimensionless number: the saturation parameter. It weighs how hard the laser is driving the transition against how fast the atom decays. Pushed to strong enough driving, the atom saturates at equal populations, but a two-level system can never be inverted, no matter how hard it is driven.

## Key Equation

$$
S = \frac{\Omega_0^2/2}{\Delta^2 + \gamma^2/4}
$$

**Derived From:** setting all time derivatives to zero in the optical Bloch equations (steady state, valid once the driving field has been on for $t\gg T_1,T_2$) and solving the resulting three algebraic equations for $u$, $v$, $w$ — see [Optical Bloch Equations](Optical%20Bloch%20Equations.md); $\gamma\equiv1/T_1$ is the spontaneous decay rate.

## Supporting Formulas

- Steady-state populations: $w_\text{st} = -\dfrac{1}{S+1}$ — approaches $-1$ (ground state) as $S\to0$, and $0$ (equal populations) as $S\to\infty$; never becomes positive, so a two-level atom can never be population-inverted purely by driving it harder
- Steady-state quadratures: $v_\text{st} = \dfrac{\Delta}{\Omega_0}\dfrac{S}{S+1}$ (dispersive, antisymmetric in $\Delta$), $u_\text{st} = \dfrac{\gamma}{2\Omega_0}\dfrac{S}{S+1}$ (absorptive, symmetric Lorentzian peak at resonance) — see [Optical Bloch Vector](Optical%20Bloch%20Vector.md)
- $S=1$ defines the saturation intensity on resonance: $\Delta=0,\ \Omega_0=\gamma/\sqrt2$
- Lineshape: $w_\text{st}$ vs. $\Delta$ is a power-broadened Lorentzian of width $\gamma\sqrt{1+S}$ — stronger driving broadens the observed linewidth

## Derivation Outline

1. Set $\dot u=\dot v=\dot w=0$ in the full optical Bloch equations (with $T_1,T_2$ decay included).
2. Solve the resulting linear system algebraically for the steady-state $u_\text{st}$, $v_\text{st}$, $w_\text{st}$ in terms of $\Delta$, $\Omega_0$, and $\gamma$.
3. Package the combination $\Omega_0^2/2$ over $(\Delta^2+\gamma^2/4)$ that appears repeatedly into the single dimensionless saturation parameter $S$.

## Physical Intuition

Think of the atom as constantly being pumped up by the laser and constantly leaking back down by spontaneous emission — steady state is simply the point where these two competing processes balance. $S$ is the ratio of how fast the laser is trying to push population up versus how fast the atom naturally decays; a weak laser gives $S\ll1$ and the atom sits almost entirely in the ground state, while a very strong laser gives $S\gg1$ and drives the populations toward a 50/50 split — but never past it, because spontaneous emission is always draining population out of the excited state and a two-level system has nowhere else for the "extra" population to hide. This is exactly why real lasers need at least three energy levels: with only two levels, there is a hard ceiling on how much of the atomic sample can ever be excited at once, no matter how much power is poured in.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Optical Bloch Equations](Optical%20Bloch%20Equations.md), [Optical Bloch Vector](Optical%20Bloch%20Vector.md)
**Full Derivation:**
