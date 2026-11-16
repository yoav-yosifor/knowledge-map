---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

Two indistinguishable photons entering the two ports of a balanced [beamsplitter](Quantum%20Beamsplitter.md) always leave together, out of the same port. This is a purely quantum two-photon interference effect with no classical analogue. Its signature is a coincidence-rate "dip" as a function of the photons' relative delay — a direct, practical measure of how indistinguishable the two photons are.

## Prerequisite Concepts

- [Quantum Beamsplitter](Quantum%20Beamsplitter.md) — the unitary scattering element the two photons interfere at
- [Quantum Second-Order Coherence](Quantum%20Second-Order%20Coherence.md) — the coincidence-rate observable, $G^{(2)}$, used to detect and quantify the effect
- [Single-Photon Wave Packet](Single-Photon%20Wave%20Packet.md) — the finite-duration wavepacket description needed to give the two photons a well-defined relative delay
- [Photon Number States](Photon%20Number%20States.md) — the input Fock states at each port

## Regimes and Parameters

- Distinguishable photons (e.g. orthogonal polarizations, $|1;H\rangle_a\otimes|1;V\rangle_b$): all four output combinations appear with the classically expected coincidence probability, $G^{(2)}(0)=1/2$ — no two-photon interference, since the polarization tags "which path" each photon took
- Indistinguishable photons at zero delay, $|1\rangle_a\otimes|1\rangle_b$: the "one photon in each output" outcome cancels by destructive interference between the two indistinguishable histories (both transmitted / both reflected); the output collapses to $\tfrac{i}{\sqrt2}(|2,0\rangle+|0,2\rangle)$, always bunched together in one output — the two detectors never click together, $G^{(2)}(0)=0$
- Finite relative delay $\tau$ between wavepacket photons interpolates between these two limits, the **Hong-Ou-Mandel (HOM) dip**: $G^{(2)}(0;\tau)=\tfrac12(1-|(\phi_a^*\ast\phi_b)(\tau)|^2)$, a function of the overlap between the two photon wavepackets — full derivation in [Hong-Ou-Mandel Dip Derivation](Hong-Ou-Mandel%20Dip%20Derivation.md)
- For identical Gaussian wavepackets: $G^{(2)}(0;\tau)=\tfrac12(1-e^{-\sigma^2\tau^2/2})$ — a dip from the classical value $1/2$ down to exactly $0$ at $\tau=0$, with width set by the inverse spectral bandwidth $1/\sigma$
- Spectrally correlated photon pairs (as from spontaneous parametric down-conversion, with a non-factorizable joint spectral amplitude) can produce an anomalously narrow HOM dip even when each individual photon is narrowband and long in time

## Physical Intuition

If two indistinguishable photons arrive at a beamsplitter from opposite sides at exactly the same moment, there are, in principle, two ways for one photon to end up in each output: both photons could be transmitted straight through, or both could be reflected. Because the photons are genuinely indistinguishable, nature cannot "know" which of these two histories actually happened, and the two possibilities interfere — destructively, as it turns out, so that the "split" outcome never occurs at all. The photons always leave bunched together, both from the same output port, chosen randomly between the two ports shot to shot, but never separated. This has nothing to do with either detector alone — look at one output on its own and you see nothing unusual — the entire effect lives in the correlation between the two detectors, which simply never fire together. Giving the two photons a time delay smooths this perfect coalescence into a graceful dip: as the delay grows, the photons become more distinguishable (their wavepackets no longer perfectly overlap), the destructive interference weakens, and the coincidence rate climbs back up toward the ordinary classical 50% expectation. Because the dip's shape is set entirely by how well the two photon wavepackets overlap, measuring it is one of the most direct and sensitive ways to certify that two photons — potentially from entirely different sources — are truly identical in every degree of freedom.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quantum Beamsplitter](Quantum%20Beamsplitter.md), [Quantum Second-Order Coherence](Quantum%20Second-Order%20Coherence.md), [Hanbury-Brown and Twiss Experiment](Hanbury-Brown%20and%20Twiss%20Experiment.md)
**Concepts Used:** [Quantum Beamsplitter](Quantum%20Beamsplitter.md), [Single-Photon Wave Packet](Single-Photon%20Wave%20Packet.md), [Photon Number States](Photon%20Number%20States.md)
