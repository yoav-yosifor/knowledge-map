---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

A resonant laser can drive a two-level atom's excited-state population all the way from 0% to 100% and back, oscillating rather than settling toward a steady value. That's different from the older picture, which treats light as an [incoherent rate process](Einstein%20Coefficients.md) and predicts population creeping up toward at most 50%. The difference comes down to what's being tracked: quantum mechanics follows probability amplitudes, which can reinforce or cancel, not just probabilities, which can only ever add.

## Key Equation

$$
P_e(t) = \left(\frac{\Omega_0}{\Omega}\right)^2 \sin^2\!\left(\frac{\Omega\,t}{2}\right), \qquad \Omega = \sqrt{\Omega_0^2+\Delta^2}
$$

**Derived From:** solving the RWA equations of motion $i\,\dot b_g=\tfrac{\Omega_0}{2}b_e,\ i\,\dot b_e = \Delta\,b_e+\tfrac{\Omega_0}{2}b_g$ for an atom starting in the ground state ($b_g(0)=1,\ b_e(0)=0$) — see [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md).

## Supporting Formulas

- Peak Rabi frequency: $\Omega_0 = d E_0/\hbar$ — the maximum coupling rate, set by the transition dipole moment $d$ and field amplitude $E_0$; see [Transition Dipole Moment](Transition%20Dipole%20Moment.md)
- Resonant case ($\Delta=0$): $P_e(t)=\sin^2(\Omega_0 t/2)$ — complete population transfer, period $T_\text{Rabi}=2\pi/\Omega_0$
- $\pi$-pulse: duration $t_\pi=\pi/\Omega_0$ gives $P_e=1$ — complete transfer $|g\rangle\to|e\rangle$
- $\pi/2$-pulse: duration $t_{\pi/2}=\pi/(2\Omega_0)$ gives the equal superposition $\tfrac{1}{\sqrt2}(|g\rangle+i|e\rangle)$ — maximum coherence, the first step of every Ramsey sequence
- Off resonance ($\Delta\neq0$): amplitude is reduced, $(\Omega_0/\Omega)^2<1$, and the oscillation frequency $\Omega=\sqrt{\Omega_0^2+\Delta^2}$ is faster than $\Omega_0$
- Einstein rate-equation limit: for incoherent light, ensemble-averaged over many atoms and long times, the same physics reduces to $P_e(t)=P_e^\infty(1-e^{-\gamma t})$ with $P_e^\infty\leq0.5$ — see [Einstein Coefficients](Einstein%20Coefficients.md)

## Derivation Outline

1. Write the atomic state as a superposition $c_g|g\rangle+c_e|e\rangle$ and substitute into the Schrödinger equation with the full dipole-driven Hamiltonian.
2. Move to the frame rotating at the laser frequency and apply the rotating wave approximation to remove the rapidly oscillating counter-rotating terms, leaving a time-independent $2\times2$ Hamiltonian.
3. Diagonalize (or directly solve) this time-independent system for the amplitudes starting purely in the ground state; squaring the excited-state amplitude gives the Rabi formula above.

## Physical Intuition

The key difference from the older, classical rate-equation picture is that quantum mechanics tracks complex probability amplitudes, not just real, positive probabilities. Amplitudes can add constructively and then destructively, the way two waves can build up and then cancel — that reversal is exactly what a Rabi oscillation is: population climbs from the ground state toward the excited state, then the coherent coupling drives it back down, then up again, indefinitely, as long as nothing disturbs the phase. A rate equation has no way to produce this back-and-forth because it only ever tracks how fast population moves in one direction. Detuning the laser from resonance does two things at once: it speeds up the oscillation (there is now an extra "restoring force" pulling the state back, in addition to the drive) while simultaneously capping how far the population can climb, because the mismatch between laser and atom energy never lets the transfer go fully to completion.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [Dressed States](Dressed%20States.md), [Optical Bloch Equations](Optical%20Bloch%20Equations.md), [Einstein Coefficients](Einstein%20Coefficients.md)
**Full Derivation:**
