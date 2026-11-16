---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The DiVincenzo criteria are the fundamental requirements a [physical platform](Physical%20Qubit%20Platforms.md) must satisfy to be a viable quantum computer. They define the bridge between abstract quantum information theory and physical realization.

## Key Equation

$$

$$

**Derived From:** (a checklist of physical requirements, not a derived equation.)

## Supporting Formulas

- A scalable system of well-defined two-level systems (qubits)
- Ability to initialize qubits in a known state
- Long coherence times relative to gate operation times (T1/T2 relaxation — future Quantum Photonics course)
- A universal set of quantum gates — see [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md)
- Ability to perform measurement and extract classical information — see [Quantum Measurement](Quantum%20Measurement.md)

## Derivation Outline

1. Require a scalable register of well-defined two-level systems (qubits).
2. Require reliable initialization of qubits into a known reference state.
3. Require coherence times long compared to gate operation times.
4. Require a universal set of quantum gates to implement arbitrary computations.
5. Require a measurement scheme to extract classical readout.

## Physical Intuition

Quantum information theory on paper doesn't care what a qubit is made of — a qubit is just a two-level system, full stop. But if you actually want to build a machine, "just a two-level system" isn't nearly enough of a specification, and the DiVincenzo criteria are the checklist that closes that gap: they're the minimum list of hardware demands any physical platform has to meet before it's even a candidate for a working quantum computer, regardless of whether it's built from trapped ions, superconducting circuits, or photons. You need enough well-characterized two-level systems that you can scale the design up rather than being stuck at a handful of qubits; you need a reliable way to set every qubit to a known starting state before a computation begins; you need those qubits to hold onto their quantum information for much longer than it takes to actually perform an operation on them, since a superposition that decays before you're done manipulating it is useless; you need a way to build any quantum logic operation at all out of some finite, universal toolkit of gates; and at the end you need a way to actually read out classical answers. None of these are exotic mathematical requirements — they're exactly the practical obstacles every real qubit platform runs into, which is why the list functions as a report card for comparing very different technologies on equal footing.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Physical Qubit Platforms](Physical%20Qubit%20Platforms.md)
**Full Derivation:**
