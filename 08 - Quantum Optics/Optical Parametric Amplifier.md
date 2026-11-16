---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

A nonlinear crystal that transfers energy from a strong classical pump beam into a weaker signal beam via [three-wave mixing](Three-Wave%20Mixing%20Phase-Matching.md), generating a new "idler" field in the process. Classically, this makes it an amplifier. Quantum mechanically, in its degenerate form, it's the physical device that implements the [squeezing operator](Squeezing%20Operator%20Derivation.md) and generates squeezed light.

## Prerequisite Concepts

- [Three-Wave Mixing Phase-Matching](Three-Wave%20Mixing%20Phase-Matching.md) — the underlying coupled-mode framework this device operates in
- [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md) — the quantum operator this device implements in its degenerate, undepleted-pump regime
- [Squeezed States](Squeezed%20States.md) — the non-classical light this device produces
- [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md) — the symmetry classification of the interaction this device implements

## Regimes and Parameters

- **Undepleted pump:** the pump field at $\omega_3$ is strong enough to be treated as a fixed classical amplitude, uncoupled to the signal ($\omega_1$) and idler ($\omega_2=\omega_3-\omega_1$); classical coupled equations $dA_1/dz=\kappa_1A_2^*$, $dA_2/dz=\kappa_2A_1^*$ give exponential (hyperbolic) gain, $A_1(z)=\cosh(|\kappa|z)A_1(0)$, $A_2(z)=e^{-2i\theta}\sinh(|\kappa|z)A_1^*(0)$ for a signal seeded at $z=0$ and no injected idler
- **Degenerate case** ($\omega_1=\omega_2$, single mode $\hat a$): the quantum interaction Hamiltonian reduces exactly to the squeezing generator, $\hat H=\kappa\hat a^2+\kappa^*\hat a^{\dagger2}$, with squeezing parameter $r=\kappa L$ accumulated over the crystal length $L$ — applying this to the vacuum produces squeezed vacuum, turning the noise circle in phase space into an ellipse
- **Non-degenerate case** (signal and idler distinct): $\hat H=\kappa\hat a_s\hat a_i+\kappa^*\hat a_i^\dagger\hat a_s^\dagger$ — parametric down-conversion, a pump photon annihilated to create a correlated signal-idler photon pair; this is the source used to generate the indistinguishable photon pairs behind the [Hong-Ou-Mandel Effect](Hong-Ou-Mandel%20Effect.md)
- **Weak-signal (spontaneous) limit:** with no signal seed at all, spontaneous parametric down-conversion generates photon pairs from vacuum fluctuations alone — the same physics as squeezed-vacuum generation, viewed in the discrete photon-pair picture rather than the continuous-quadrature picture

## Physical Intuition

Think of the OPA as a one-way energy funnel: a strong pump beam pumps energy into whatever weaker signal field is present, amplifying it, and — because energy and momentum must both balance in the underlying three-photon process — a third field, the idler, is unavoidably created alongside the amplified signal. In the special case where the signal and idler collapse into the very same mode, this amplification process is exactly the physical mechanism that generates squeezed light: it isn't a separate, exotic process from ordinary optical parametric amplification, it's the very same nonlinear-crystal physics, just viewed at the level of individual quadratures rather than mean intensities. Even with no signal seeded at all, the crystal still creates correlated photon pairs directly out of the vacuum — this is where squeezed vacuum, and independently, the correlated photon pairs used in two-photon interference experiments, both come from.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Squeezed States](Squeezed%20States.md), [SU(1,1) Interferometer](SU(1,1)%20Interferometer.md), [Hong-Ou-Mandel Effect](Hong-Ou-Mandel%20Effect.md), [Three-Wave Mixing Phase-Matching](Three-Wave%20Mixing%20Phase-Matching.md)
**Concepts Used:** [Three-Wave Mixing Phase-Matching](Three-Wave%20Mixing%20Phase-Matching.md), [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md)
