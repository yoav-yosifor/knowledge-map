---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

Photon pairs produced by spontaneous parametric down-conversion are entangled in emission time and frequency. This happens because energy conservation ties the signal and idler frequencies to a fixed-frequency pump. In the idealized limit of a sharp pump and broadband phase matching, this becomes a perfect continuous-variable [EPR](../10%20-%20Quantum%20Information/EPR%20Argument.md) correlation between arrival time and frequency — the discrete photon-pair realization of Einstein's original position-momentum EPR state.

## Key Equation

$$
|\Psi\rangle = \int d\omega_s\,\tilde A(\omega_s)\,|\omega_s\rangle_s\otimes|\omega_p-\omega_s\rangle_i \;\xrightarrow[\ A(t-t')\to\delta(t-t')\ ]{\tilde A(\omega_s)\to\text{flat}}\; |\psi\rangle = |t\rangle_s\otimes|t\rangle_i
$$

**Derived From:** energy conservation in the down-conversion process, $\omega_s+\omega_i=\omega_p$, for a fixed pump frequency; selecting a narrow pinhole of phase-matched signal/idler directions leaves a joint two-photon amplitude $\tilde A(\omega_s)$ correlated purely through this constraint, whose Fourier transform is the equivalent time-domain amplitude $A(t-t')$.

## Supporting Formulas

- $\Delta(t_s-t_i)^2\to0$ and $\Delta(\omega_s+\omega_i-\omega_p)^2\to0$ simultaneously in the idealized limit — the photon-pair analogue of simultaneously well-defined relative-position and total-momentum EPR observables
- A real source has finite pump bandwidth and a non-flat joint spectral amplitude $A(t-t')$, which sets the actual timing/frequency correlation width — see the spontaneous limit of the [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md)

## Derivation Outline

1. Energy conservation in the down-conversion process fixes $\omega_s+\omega_i=\omega_p$ for a pump photon of definite frequency.
2. Selecting a narrow pinhole of phase-matched directions leaves the joint two-photon amplitude $\tilde A(\omega_s)$ correlated only through this constraint.
3. Fourier transform to the time domain: the same joint amplitude becomes a function $A(t-t')$ of the emission/detection time difference, so the photons are correlated in time as well as frequency.
4. Take the idealized limit of a flat spectral amplitude, $A(t-t')\to\delta(t-t')$, giving perfectly simultaneous detection times and perfectly anti-correlated frequencies about $\omega_p/2$.

## Physical Intuition

Inside a nonlinear crystal, a pump photon occasionally splits into two lower-energy photons, called signal and idler. Energy has to balance, so whatever frequency the signal photon ends up with, the idler's frequency is whatever is left over from the pump — the two are locked together the instant the pair is born, and since they're born together they also arrive at their detectors at essentially the same moment. Push this to the idealized extreme — an infinitely sharp pump frequency and infinitely broadband phase matching — and the two photons become perfectly correlated in both time and frequency simultaneously. That is exactly the strange situation Einstein, Podolsky, and Rosen worried about: two particles with no well-defined individual property, but whose difference in one variable (arrival time) and sum in the conjugate variable (frequency) are both pinned down exactly. Ordinary down-conversion hardware turns out to manufacture this thought experiment for real.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md), [Two-Mode Squeezed Vacuum](Two-Mode%20Squeezed%20Vacuum.md), [EPR Argument](../10%20-%20Quantum%20Information/EPR%20Argument.md)
**Full Derivation:**
