---
tags:
  - quantum-information
  - system
  - protocol
---
---
## Overview

A protocol that uses one shared entangled pair to transmit two classical bits by exchanging just a single qubit. It shows entanglement acting as a genuine communication resource, without violating the [Holevo Bound](Holevo%20Bound.md) or causality.

## Prerequisite Concepts

- [Bell States](Bell%20States.md) — the shared entangled pair
- [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) — Alice's local encoding unitary
- [Quantum Measurement](Quantum%20Measurement.md) — Bob's Bell measurement

## Regimes and Parameters

- Protocol: Alice and Bob pre-share a Bell pair → Alice applies one of four local unitaries ($I, X, Z, XZ$) → Alice sends her one qubit to Bob → Bob performs a joint Bell measurement on both qubits
- Result: two classical bits transmitted using one transmitted qubit

## Physical Intuition

Entanglement acts as a pre-shared resource that lets a single transmitted qubit carry the information of two classical bits — it does not violate the Holevo bound because the resource model has changed: the entanglement was not free, it had to be distributed beforehand.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quantum Teleportation](Quantum%20Teleportation.md), [Holevo Bound](Holevo%20Bound.md)
**Concepts Used:** [Bell States](Bell%20States.md), [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md), [Quantum Measurement](Quantum%20Measurement.md)
