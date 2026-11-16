---
tags:
  - quantum-information
  - system
  - protocol
---
---
## Overview

BB84 is the first and most widely studied quantum key distribution protocol. It lets Alice and Bob establish a shared secret key over a public channel, with security guaranteed by physics rather than computational hardness — because any eavesdropping necessarily leaves a detectable trace.

## Prerequisite Concepts

- [Qubit](Qubit.md) — single qubits prepared in two non-commuting bases ($Z$: $|0\rangle,|1\rangle$; $X$: $|+\rangle,|-\rangle$)
- [No-Cloning Theorem](No-Cloning%20Theorem.md) — Eve cannot copy qubits and postpone measurement
- [Information-Disturbance Tradeoff](Information-Disturbance%20Tradeoff.md) — Eve cannot learn the key without introducing detectable errors
- [Uncertainty Relations](Uncertainty%20Relations.md) — measuring in the wrong basis irreversibly disturbs the state

## Regimes and Parameters

- Protocol: Alice sends qubits randomly prepared in $X$ or $Z$ basis → Bob measures each in a randomly chosen basis → Alice and Bob publicly compare *bases* (not outcomes) → matching-basis results form the raw key
- Eavesdropping detection: Eve doesn't know the preparation basis; measuring in the wrong basis (probability 1/2) introduces errors in Bob's outcomes; comparing a subset of results reveals Eve's presence, and the protocol aborts if the error rate is too high — detection probability grows exponentially with key length

## Physical Intuition

Any eavesdropping attempt leaves a physical trace: BB84's security follows directly from three no-go principles working together — Eve can't copy the qubits to measure later, can't learn the key without disturbing it, and measuring in the wrong basis irreversibly randomizes the outcome she was trying to steal.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [No-Cloning Theorem](No-Cloning%20Theorem.md), [Information-Disturbance Tradeoff](Information-Disturbance%20Tradeoff.md)
**Concepts Used:** [Qubit](Qubit.md), [Uncertainty Relations](Uncertainty%20Relations.md)
