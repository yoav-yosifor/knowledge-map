---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

A π-pulse drives a two-level atom with a fixed-frequency pulse, timed exactly to flip the population. Adiabatic rapid passage does something different: it sweeps the laser's detuning slowly through resonance. As it sweeps, the Bloch vector continuously tracks the rotating effective field, dragging it from the ground state all the way to the excited state. Unlike a π-pulse, this transfer works no matter exactly how strong the coupling is.

## Key Equation

$$
\left|\frac{d\hat\Omega}{dt}\right| \ll \Omega(t) = \sqrt{\Omega_0^2+\Delta(t)^2}
$$

**Derived From:** the general adiabatic condition applied to the Rabi vector $\vec\Omega=(\Omega_0,0,-\Delta(t))$ — see [Adiabatic Approximation](Adiabatic%20Approximation.md); as $\Delta(t)$ is swept, the direction of $\vec\Omega$ must rotate slowly compared to its own magnitude (the instantaneous precession rate) for the Bloch vector to keep tracking it.

## Supporting Formulas

- Sweep geometry: as $\Delta$ sweeps from $\Delta\gg\Omega_0$ (Rabi vector near $-\hat z$) through $\Delta=0$ (Rabi vector along $+\hat x$) to $\Delta\ll-\Omega_0$ (Rabi vector near $+\hat z$), a Bloch vector starting at the south pole ends at the north pole
- Rapidity condition: the sweep must also be fast compared to spontaneous decay, $\tau_\text{sweep}\ll T_1$ — see [T1 and T2 Relaxation](T1%20and%20T2%20Relaxation.md)
- Robustness: unlike a π-pulse, which requires precise knowledge of $\Omega_0$ and precise timing, ARP only needs the adiabatic condition to hold, so it works even when $\Omega_0$ varies across an ensemble (e.g. due to spatially inhomogeneous laser intensity) — see [Inhomogeneous Broadening](Inhomogeneous%20Broadening.md)

## Derivation Outline

1. Instead of holding the laser frequency fixed, sweep the detuning $\Delta(t)$ continuously from far positive to far negative (or vice versa).
2. Track how the Rabi vector $\vec\Omega=(\Omega_0,0,-\Delta(t))$ rotates in direction as $\Delta(t)$ changes, from nearly $-\hat z$ through $+\hat x$ to nearly $+\hat z$.
3. Require the rotation of $\vec\Omega$'s direction to be slow compared to the instantaneous precession rate $|\vec\Omega|$ at every point in the sweep, so the Bloch vector — which always precesses around $\vec\Omega$ — has time to continuously realign with it rather than being left behind.

## Physical Intuition

A π-pulse is like giving the system one precisely-timed push: get the pulse area exactly right and the population lands exactly on the excited state, but get the timing or the field strength even slightly wrong and the transfer is incomplete. Adiabatic rapid passage instead works like slowly rotating a magnet next to a compass needle — as long as you turn the magnet slowly enough, the needle just follows along, ending up pointing wherever the magnet ends up, regardless of exactly how strong the magnet was or how fast you turned it (as long as "slow enough" was satisfied). Here the "magnet" is the effective Rabi vector, whose direction sweeps from pointing toward the ground state to pointing toward the excited state as the laser is tuned through resonance, and the atom's Bloch vector — the "compass needle" — just tags along, arriving at full excitation without needing to know the exact coupling strength in advance. This makes it forgiving of exactly the kind of atom-to-atom variation in coupling strength that would spoil a precisely-timed π-pulse.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Adiabatic Approximation](Adiabatic%20Approximation.md), [Optical Bloch Equations](Optical%20Bloch%20Equations.md), [Rabi Oscillations](Rabi%20Oscillations.md)
**Full Derivation:**
