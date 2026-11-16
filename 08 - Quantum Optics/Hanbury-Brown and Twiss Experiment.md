---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

The Hanbury-Brown and Twiss (HBT) experiment measures [intensity correlations](Second-Order%20Coherence%20Function.md) between two separated detectors, instead of relying on direct field interference. It was originally used (1956) to infer the angular diameter of stars from starlight bunching statistics.

## Prerequisite Concepts

- [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md) — the quantity the experiment measures directly
- [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md) — splits the incoming light between the two detectors
- [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md) — the detection statistics that must be distinguished from genuine intensity bunching

## Regimes and Parameters

- For Gaussian-distributed (thermal/chaotic) starlight: $G^{(2)}(0)=2\langle I\rangle^2$, decaying to $G^{(2)}(\tau\gg\tau_c)=\langle I\rangle^2$ — a bunching signature at zero delay that disappears once the delay exceeds the coherence time
- Because the measurement uses intensity correlations rather than field interference, it requires no interferometric path-length stability — a major practical advantage over direct fringe measurements for astronomical baselines
- Historically controversial: since $g^{(1)}$ is normally associated with a single photon interfering with itself, it was initially unclear how incoherent starlight could show correlations at all; the Siegert relation resolves this by showing the bunching is a classical wave effect, not evidence of photon-photon interaction

## Physical Intuition

Instead of trying to make two beams of starlight interfere directly — which would require keeping the path lengths stable to a fraction of a wavelength over enormous distances — HBT instead asks a statistical question: when one detector registers an unusually bright moment, does the other detector (looking at the same source through a different path) tend to see a bright moment too, at very nearly the same time? For chaotic light like starlight, the answer is yes, because the source's intensity fluctuates as a whole, not independently in each path. Measuring how strongly the two detectors' fluctuations track each other, and how that correlation shrinks as detectors are moved apart, effectively reconstructs the same spatial coherence information an ordinary interferometer would give, but a much more forgiving experiment to actually build.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md)
**Concepts Used:** [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md)
