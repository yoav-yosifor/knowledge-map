---
tags:
  - quantum-information
  - system
  - protocol
---
---
## Overview

A protocol that transfers an unknown quantum state from Alice to Bob, using one shared entangled pair and two classical bits. The original state is destroyed in the process, which is consistent with [no-cloning](No-Cloning%20Theorem.md). No matter or energy is transferred — only quantum information.

## Prerequisite Concepts

- [Bell States](Bell%20States.md) — the shared entangled resource
- [Quantum Measurement](Quantum%20Measurement.md) — Alice's Bell measurement
- [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) — Bob's correction unitary
- [No-Cloning Theorem](No-Cloning%20Theorem.md) — why the original must be destroyed

## Regimes and Parameters

- Protocol: Alice performs a Bell measurement on her qubit + the unknown state → she sends 2 classical bits to Bob → Bob applies the corresponding correction unitary → Bob's qubit becomes the exact original state

## Physical Intuition

Teleportation moves quantum information, not matter or energy — the entangled pair supplies the nonlocal correlation, and the two classical bits tell Bob exactly which local correction turns his half of the pair into the state Alice wanted to send. The entanglement is consumed and the original is destroyed.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Superdense Coding](Superdense%20Coding.md), [No-Cloning Theorem](No-Cloning%20Theorem.md), [No-Teleportation of Classical Description](No-Teleportation%20of%20Classical%20Description.md)
**Concepts Used:** [Bell States](Bell%20States.md), [Quantum Measurement](Quantum%20Measurement.md), [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md)
