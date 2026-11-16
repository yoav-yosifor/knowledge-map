---
tags:
  - nanophotonics
  - system
  - device
---
---
## Overview

A closed loop of waveguide (a ring or racetrack) evanescently coupled to a straight bus waveguide through a directional coupler. Light in the bus at a frequency that fits an integer number of wavelengths into the loop builds up resonantly inside the ring; off resonance it passes by almost untouched. In this single-bus **all-pass filter** configuration the device is a frequency-selective phase element and notch filter, and the workhorse building block for integrated modulators, filters, delay lines and sensors.

## Prerequisite Concepts

- [Directional Coupler](Directional%20Coupler.md) — the bus–ring junction; its power coupling coefficient $\kappa$ and the $2\times2$ matrix set how much light enters and leaves the loop each pass.
- [Structural Dispersion and Group Index](Structural%20Dispersion%20and%20Group%20Index.md) — the wavelength dependence of $n_{eff}$ in the (usually HIC) ring waveguide; the group index $n_g$ governs the resonance spacing.
- [Free Spectral Range](Free%20Spectral%20Range.md) — the frequency spacing of the resonance comb, $\Delta\omega_{FSR}=2\pi c/(L\,n_g)$.
- [Cavity Q Factor and Finesse](Cavity%20Q%20Factor%20and%20Finesse.md) — how sharp each resonance is / how long light lives in the loop.
- [Critical Coupling](Critical%20Coupling.md) — the $\kappa=\alpha$ operating point where the through port goes dark and the stored energy peaks.
- [Waveguide Bending Loss](Waveguide%20Bending%20Loss.md) — the intrinsic radiation loss of the curved sections, part of the per-round-trip loss $\alpha$; reduced by HIC and larger radius.
- [Ring Resonator Rate Equations](Ring%20Resonator%20Rate%20Equations.md) — the time-domain (coupled-mode) description of the circulating envelope, valid at high $Q$ near resonance.

## Regimes and Parameters

- The device is fully specified by **three** parameters: the free spectral range $\Delta\nu_{FSR}$, the power coupling coefficient $\kappa$, and the loss per round trip $\alpha$.
- Resonance condition: $\dfrac{\omega_m}{c}n_{eff}(\omega)L=2\pi m$ — a comb of resonances spaced by the FSR.
- All-pass spectral response: unity transmission with **notches** at each resonance; the width and depth of a notch depend on $\kappa$, $\alpha$ and the FSR. With $\alpha=0$ the magnitude response is flat ("all-pass") and only the phase varies.
- **Under-coupled** ($\kappa<\alpha$), **critically coupled** ($\kappa=\alpha$, notch $\to$ zero, stored energy maximal, build-up $1/\kappa$), **over-coupled** ($\kappa>\alpha$).
- On-resonance field build-up can exceed the input, $|E_1/E_{in}|^2>1$, when $\alpha<2\sqrt{\kappa}/(1+\sqrt{\kappa})$.
- Characterized in practice by the loaded $Q$ (linewidth measurement); fabricated micro-rings in the source reach $Q\sim10^4$.
- Typical applications built on this block: high-speed modulators, add/drop filters, cascaded rings for flat-top filters, optical delay/storage, and refractive-index sensors.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Add-Drop Multiplexer](Add-Drop%20Multiplexer.md), [Mach-Zehnder Interferometer](Mach-Zehnder%20Interferometer.md), [All-Pass Ring Transfer Function Derivation](All-Pass%20Ring%20Transfer%20Function%20Derivation.md)
**Concepts Used:** [Directional Coupler](Directional%20Coupler.md), [Structural Dispersion and Group Index](Structural%20Dispersion%20and%20Group%20Index.md), [Free Spectral Range](Free%20Spectral%20Range.md), [Cavity Q Factor and Finesse](Cavity%20Q%20Factor%20and%20Finesse.md), [Critical Coupling](Critical%20Coupling.md), [Waveguide Bending Loss](Waveguide%20Bending%20Loss.md), [Ring Resonator Rate Equations](Ring%20Resonator%20Rate%20Equations.md)
