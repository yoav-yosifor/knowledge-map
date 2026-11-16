---
tags:
  - quantum-information
  - system
  - framework
---
---
## Overview

A survey of the major physical platforms used to realize a [qubit](Qubit.md) and build a quantum computer. Each platform encodes quantum information in a different physical degree of freedom, and each makes a different tradeoff against the [DiVincenzo Criteria](DiVincenzo%20Criteria.md).

## Prerequisite Concepts

- [DiVincenzo Criteria](DiVincenzo%20Criteria.md) — the requirements every platform is judged against
- [Qubit](Qubit.md) — the abstract information unit each platform physically realizes
- [Decoherence](Decoherence.md) — what limits every platform (T1/T2 relaxation detail belongs to a future Quantum Photonics course)

## Regimes and Parameters

- **Photons:** polarization ($|H\rangle,|V\rangle$), path (dual-rail), time-bin — see [Dual-Rail Encoding](Dual-Rail%20Encoding.md)
- **Trapped ions:** internal electronic states — very high fidelity, long coherence, slower gates
- **Neutral atoms:** hyperfine energy levels — strong interactions, flexible geometry, complex control
- **Superconducting circuits:** Josephson-junction states — fast gates, scalable fabrication, requires cryogenics
- **Quantum dots:** electron spin or charge
- **Photonic systems specifically:** low decoherence, room-temperature operation, but weak photon-photon interaction makes two-qubit gates hard; dominant noise is photon loss, not phase decoherence (unlike matter qubits, where $T_1/T_2$ dominate)

## Physical Intuition

Every platform trades off the same handful of properties differently: how well-isolated the qubit is from its environment (coherence) versus how strongly qubits can be made to interact with each other (gate speed and fidelity). Photonic systems sit at one extreme — nearly perfect isolation, but qubits that barely talk to each other.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [DiVincenzo Criteria](DiVincenzo%20Criteria.md), [Qubit](Qubit.md)
**Concepts Used:** [Qubit](Qubit.md), [Decoherence](Decoherence.md)
