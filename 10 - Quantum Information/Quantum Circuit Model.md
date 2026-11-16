---
tags:
  - quantum-information
  - system
  - framework
---
---
## Overview

The standard model of quantum computation runs in three steps: prepare an initial state, apply a sequence of [unitary gates](Unitary%20Quantum%20Gate.md), then [measure](Quantum%20Measurement.md). The output is a classical bit string, obtained probabilistically.

## Prerequisite Concepts

- [Qubit](Qubit.md) — the information unit
- [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) — the operations applied
- [Quantum Measurement](Quantum%20Measurement.md) — the final read-out step
- [Quantum Parallelism](Quantum%20Parallelism.md) — why superposition through the circuit is useful

## Regimes and Parameters

- Measurement is always postponed to the end — premature measurement collapses the state and destroys interference
- Classical bit vs qubit: classical state update is stochastic on real matrices; quantum state update is unitary on complex matrices

## Physical Intuition

Picture a quantum circuit as a strict three-act play with no exceptions to the ordering: first you set the stage by preparing a known starting state, then you let it evolve through a sequence of reversible operations that never destroy information, and only at the very last moment do you look at the result. The reason for this rigid ordering is that looking — measuring — is fundamentally different from every other step in the circuit. Every gate before measurement is unitary, meaning it can always be undone and it lets different computational paths keep interfering with each other, building up amplitude in the answers you want and canceling it in the answers you don't. The instant you measure, that interference machinery is gone: the state collapses to one definite outcome, and any chance to keep combining paths is lost for good. So if you measured partway through, you'd freeze the computation prematurely and throw away exactly the interference effects that make quantum computing worth doing at all. This is also what separates a quantum circuit from a classical one: classical bits are pushed around by processes that just shuffle probabilities, while qubits are pushed around by operations that preserve and exploit the richer, complex-valued structure of superposition — and it's only by holding off measurement until the answer is fully formed that a circuit gets to use that extra structure.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quantum Parallelism](Quantum%20Parallelism.md), [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md), [Quantum Measurement](Quantum%20Measurement.md)
**Concepts Used:** [Qubit](Qubit.md), [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md), [Quantum Measurement](Quantum%20Measurement.md)
