---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

This is an interferometer built from two nonlinear-crystal [parametric amplifiers](Optical%20Parametric%20Amplifier.md) instead of two beamsplitters. Instead of conserving total photon number ([SU(2)](SU(2)%20and%20SU(1,1)%20Dynamics.md)), it conserves the signal-idler photon-number *difference* ([SU(1,1)](SU(2)%20and%20SU(1,1)%20Dynamics.md)). Its [phase sensitivity](Measurement%20Sensitivity.md) improves exponentially with [squeezing strength](Squeezing%20Operator%20Derivation.md), and no coherent seed light is required at all.

## Prerequisite Concepts

- [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md) — each nonlinear crystal implements a squeezing transformation of the field
- [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md) — the relative phase imposed between the two parametric-amplifier stages
- [Measurement Sensitivity](Measurement%20Sensitivity.md) — the figure of merit used to quantify performance
- [Vacuum Fluctuations](Vacuum%20Fluctuations.md) — the only input required; the entire signal is vacuum fluctuations amplified by the non-linear stages
- [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md) — the symmetry classification this device is named after

## Regimes and Parameters

- Two optical parametric amplifiers (OPAs) of squeezing parameter $g$ in place of the two beamsplitters of a Mach-Zehnder interferometer, with a relative phase $\phi$ between them; undepleted-pump and degenerate down-conversion assumed
- At $\phi=0$: the two squeezing stages add, equivalent to a single crystal of twice the length, $\hat a_{out}=\hat a\cosh(2g)+\hat a^\dagger\sinh(2g)$
- At $\phi=\pi/2$: the two stages exactly cancel, $\hat a_{out}=i\hat a$ — the squeezing "undoes itself," the signature of interference in this system (period $\pi/2$ rather than $\pi$, a consequence of the degenerate case where signal and idler share the same phase)
- With vacuum input, mean output photon number $\langle\hat a_{out}^\dagger\hat a_{out}\rangle=\sinh^2(2g)\cos^2\phi$ — vacuum fluctuations amplified into a detectable signal, modulated by $\cos^2\phi$
- Sensitivity at the dark fringe, strong-squeezing limit: $\Delta\phi_{min}\approx\sqrt2\,e^{-2g}$ — improves exponentially faster with $g$ than the beamsplitter-based (SU(2)) case, and requires no bright coherent input at all
- Full derivation of the output operator, mean, variance, and sensitivity in [SU(1,1) Interferometer Sensitivity Derivation](SU(1,1)%20Interferometer%20Sensitivity%20Derivation.md)

## Physical Intuition

An ordinary interferometer needs a bright beam of light to measure a phase shift against — more photons, better sensitivity, but only as the square root of the photon number. An SU(1,1) interferometer works completely differently: it doesn't conserve the number of photons flowing through it at all, because each of its two stages is a nonlinear crystal that creates photons in correlated pairs rather than just redirecting existing ones. Run vacuum — literally no input light — through two of these crystals with a controlled phase between them, and the vacuum's own irreducible fluctuations get amplified into a real, measurable signal, whose size depends sensitively on that phase. Because the amplification is exponential in the crystal's squeezing strength rather than merely additive in photon number, the achievable sensitivity improves exponentially with squeezing too — a fundamentally different, and ultimately faster, way to buy precision than simply pouring in more photons.

## Isomorphisms

- SU(1,1) is represented mathematically by Lorentz boosts on a hyperbola, the same non-compact structure underlying special-relativistic velocity addition — in contrast to the beamsplitter's SU(2), which is represented by ordinary rotations on a sphere; this compact-vs-non-compact distinction is why beamsplitting is always bounded while parametric squeezing gives unbounded exponential gain. See [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md).

## Open Questions

- [ ]

---

## Links

**Related:** [Squeezed-Light Mach-Zehnder Interferometer](Squeezed-Light%20Mach-Zehnder%20Interferometer.md), [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md), [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md), [Measurement Sensitivity](Measurement%20Sensitivity.md)
**Concepts Used:** [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md)
