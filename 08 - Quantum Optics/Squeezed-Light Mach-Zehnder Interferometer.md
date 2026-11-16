---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

This is an ordinary Mach-Zehnder interferometer — [two beamsplitters](Beam%20Splitter%20Transformation.md) conserving total photon number. A [coherent state](Coherent%20States.md) drives the bright input port, while [squeezed vacuum](Squeezed%20States.md) is injected into the otherwise-unused dark port. This combination pushes the phase sensitivity beyond the [standard quantum limit](Standard%20Quantum%20Limit.md).

## Prerequisite Concepts

- [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md) — the two mixing elements of the interferometer
- [Coherent States](Coherent%20States.md) and [Displacement Operator](Displacement%20Operator.md) — the bright input in one arm
- [Squeezed States](Squeezed%20States.md) — the non-classical input injected into the unused port
- [Standard Quantum Limit](Standard%20Quantum%20Limit.md) — the ordinary vacuum-limited sensitivity this device beats
- [Measurement Sensitivity](Measurement%20Sensitivity.md) — the figure of merit used to quantify the improvement

## Regimes and Parameters

- Balanced interferometer, $t_1=r_1=t_2=r_2=1/\sqrt2$; input state $|\alpha_a,g_b\rangle$, a coherent state of amplitude $\alpha$ in one arm and squeezed vacuum of squeezing parameter $g$ in the other
- Operated at the dark fringe, $\phi=\pi/2$, where the mean photon-number difference between the outputs vanishes and only the cross-correlation between the two input modes survives
- Ordinary shot-noise-limited sensitivity with no squeezing ($g=0$): $\Delta\phi_{min}=1/\alpha$
- With squeezing ($g<0$, i.e. squeezing the quadrature aligned with the measurement) and a strong coherent field ($\sinh^2g\ll\alpha^2$): $\Delta\phi_{min}\approx e^{g}/\alpha$ — an improvement by the factor $e^{g}$ over the unsqueezed case
- Full derivation of the mean and variance of the output photon-number difference in [Squeezed-Light Mach-Zehnder Sensitivity Derivation](Squeezed-Light%20Mach-Zehnder%20Sensitivity%20Derivation.md)
- Real-world realization: LIGO's use of injected squeezed vacuum to improve gravitational-wave-detector sensitivity (Aasi et al., *Nature Photonics* **7**, 613–619, 2013)

## Physical Intuition

An ordinary Mach-Zehnder interferometer measures a phase shift by looking at how light redistributes between its two output ports as the relative phase between the arms changes. Even with a perfect light source, the port you don't deliberately inject light into isn't silent — vacuum fluctuations leak in there and add noise to the measurement, capping the achievable sensitivity at the standard quantum limit. The fix used here is simple in spirit: instead of leaving that port empty, deliberately fill it with squeezed vacuum, engineered to be quieter than ordinary vacuum in exactly the direction that matters for this measurement. Because squeezing doesn't touch the mean signal — only the noise — this lets the interferometer keep its full sensitivity to the phase while suppressing the noise that used to leak in through the unused port, buying a clean improvement in how small a phase shift can be resolved. This is the working principle behind quantum-enhanced interferometers such as the squeezed-light upgrade used at LIGO.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [SU(1,1) Interferometer](SU(1,1)%20Interferometer.md), [Standard Quantum Limit](Standard%20Quantum%20Limit.md), [Homodyne Detection](Homodyne%20Detection.md), [Beamsplitter Loss Model](Beamsplitter%20Loss%20Model.md)
**Concepts Used:** [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Coherent States](Coherent%20States.md), [Squeezed States](Squeezed%20States.md), [Measurement Sensitivity](Measurement%20Sensitivity.md)
