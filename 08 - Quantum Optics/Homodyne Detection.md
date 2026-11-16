---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

A detection scheme that measures a single [field quadrature](Quadrature%20Operators.md) of a light field. It works by mixing the (possibly weak, [vacuum-level](Vacuum%20Fluctuations.md), or [squeezed](Squeezed%20States.md)) signal with a strong, phase-controlled local oscillator on a [beamsplitter](Beam%20Splitter%20Transformation.md), then subtracting the two output photocurrents. This is the standard way to read out phase-dependent quantum-optical information that a simple photon counter cannot access.

## Prerequisite Concepts

- [Quadrature Operators](Quadrature%20Operators.md) — the quantity actually being measured
- [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md) — the mixing element that combines signal and local oscillator
- [Vacuum Fluctuations](Vacuum%20Fluctuations.md) — sets the detection noise floor when the signal port carries no classical field
- [Squeezed States](Squeezed%20States.md) — an input that can push the measured noise below the ordinary vacuum floor

## Regimes and Parameters

- Classical balanced-detection form (delayed copy of a field on a 50:50 splitter): subtracting the two output intensities isolates $\text{Re}\,G^{(1)}(\tau)$, the interference cross term, directly
- Quantum balanced homodyne: with local-oscillator field $E_{LO}=e^{i\theta}\sqrt{I_{LO}}$ and signal $E_{in}$, the photocurrent difference $\Delta I = I_2-I_1=\sqrt{2I_{LO}}\,X_{in}(\theta)$ is proportional to the input quadrature aligned with the LO phase $\theta$, amplified by the strong local oscillator field
- Sweeping the local-oscillator phase $\theta$ scans through every quadrature angle of the input state, allowing full phase-space tomography
- Full derivation of the photocurrent-difference operator, its dependence on the LO phase, and its variance in [Homodyne Detection Derivation](Homodyne%20Detection%20Derivation.md)

## Physical Intuition

A photon counter can only tell you how many photons arrived — it throws away all information about the field's phase. Homodyne detection is built specifically to recover that phase information by exploiting interference: mixing the signal with a strong, phase-stable reference beam on a beamsplitter, then looking only at the *difference* between the two output intensities, cancels out everything except the part of the signal that lines up with the reference's phase. Because the reference (local oscillator) is strong, even a microscopically weak fluctuation in the signal — down to the level of vacuum noise itself — gets amplified into an easily measurable macroscopic photocurrent difference. Rotating the local oscillator's phase is like rotating which "slice" of phase space you're looking at, letting the same device measure any quadrature you choose.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quadrature Operators](Quadrature%20Operators.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [First-Order Coherence Function](First-Order%20Coherence%20Function.md), [Standard Quantum Limit](Standard%20Quantum%20Limit.md), [Squeezed States](Squeezed%20States.md)
**Concepts Used:** [Quadrature Operators](Quadrature%20Operators.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Squeezed States](Squeezed%20States.md)
