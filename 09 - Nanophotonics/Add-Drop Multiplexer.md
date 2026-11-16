---
tags:
  - nanophotonics
  - system
  - device
---
---
## Overview

A ring coupled to **two** bus waveguides — an input/through bus and a drop/add bus — through two directional couplers ($\kappa_1$, $\kappa_2$). On resonance the ring routes the input from the through port to the drop port; off resonance the light stays in the through port. It is the four-port version of the ring resonator, used to pick one wavelength channel out of a stream (drop) or insert one (add), and as a Lorentzian bandpass filter.

## Prerequisite Concepts

- [Ring Resonator](Ring%20Resonator.md) — the underlying resonant loop, its resonance comb, FSR, $Q$ and round-trip loss $\alpha$.
- [Directional Coupler](Directional%20Coupler.md) — used twice; $\kappa_1$ couples the input bus to the ring, $\kappa_2$ couples the ring to the drop bus.
- [Critical Coupling](Critical%20Coupling.md) — generalized here to the balance $(1-\kappa_1)=(1-\kappa_2)(1-\alpha)$; with negligible loss this is just $\kappa_1=\kappa_2$.

## Regimes and Parameters

- Through and drop field transfer functions:
  $$T=\frac{E_{Through}}{E_{in}}=\frac{\sqrt{1-\kappa_1}-\sqrt{(1-\kappa_2)(1-\alpha)}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}}{1-\sqrt{(1-\kappa_1)(1-\kappa_2)(1-\alpha)}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}}$$
  $$D=\frac{E_{Drop}}{E_{in}}=\frac{-\sqrt{\kappa_1\kappa_2}\,(1-\alpha)^{1/4}\,e^{-i\frac{1}{2}\Delta\omega/\Delta\nu_{FSR}}}{1-\sqrt{(1-\kappa_1)(1-\kappa_2)(1-\alpha)}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}}$$
- Spectral response: the **drop** port is a passband (peaks at each resonance), the **through** port is the complementary stopband (notch at each resonance), both repeating every FSR.
- **Critical coupling:** $(1-\kappa_1)=(1-\kappa_2)(1-\alpha)$ makes the through port vanish on resonance; $\kappa_1$, $\kappa_2$ and $\alpha$ play interchangeable roles in the denominator. Loss-free limit: $\kappa_1=\kappa_2$.
- Increasing the coupling $\kappa$ broadens the drop peak (lower $Q$); increasing the loss $\alpha$ lowers the drop-peak height (power dissipated instead of dropped).
- **As an optical filter:** close to resonance with a large FSR the drop response is Lorentzian,
  $$|D|^2\propto\frac{1}{1+\left(\Delta\omega/\delta\Omega\right)^2},\qquad
  \delta\Omega^2=\frac{\left[1-\sqrt{(1-\kappa_1)(1-\kappa_2)(1-\alpha)}\right]^2}{\sqrt{(1-\kappa_1)(1-\kappa_2)(1-\alpha)}}\,\Delta\nu_{FSR}^2$$
  with the single controlling parameter $x=\sqrt{(1-\kappa_1)(1-\kappa_2)(1-\alpha)}$. Cascading several rings gives flat-top filters.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Ring Resonator](Ring%20Resonator.md), [Critical Coupling](Critical%20Coupling.md), [All-Pass Ring Transfer Function Derivation](All-Pass%20Ring%20Transfer%20Function%20Derivation.md)
**Concepts Used:** [Ring Resonator](Ring%20Resonator.md), [Directional Coupler](Directional%20Coupler.md), [Critical Coupling](Critical%20Coupling.md)
