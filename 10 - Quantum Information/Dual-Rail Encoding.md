---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

A photonic [qubit](Qubit.md) is often encoded using two optical modes that together hold a fixed total photon number. A single photon's location, which of the two modes it occupies, defines the logical state. That makes it equivalent to an ordinary two-level system, one that maps naturally onto waveguides and [beam-splitter](Beam%20Splitter%20Transformation.md) networks.

## Key Equation

$$
|0\rangle \equiv |01\rangle, \qquad |1\rangle \equiv |10\rangle
$$

**Derived From:** the two-mode, single-photon subspace of the quantized field (photon-number/Fock states — covered in a future Quantum Photonics course).

## Supporting Formulas

-

## Derivation Outline

1. Take two optical modes (e.g. two waveguides) and restrict to the single-photon subspace of the field.
2. Identify "photon in mode 1, vacuum in mode 2" as logical $|0\rangle\equiv|01\rangle$.
3. Identify "vacuum in mode 1, photon in mode 2" as logical $|1\rangle\equiv|10\rangle$.
4. Superpositions of these two Fock states give arbitrary qubit states, manipulable with beam-splitters and phase shifters.

## Physical Intuition

A photon doesn't come with a built-in "zero" or "one" label the way an electron's spin does, so photonic quantum computing needs some physical feature of the light to stand in for a qubit, and the simplest choice is just where the photon is. Take two parallel paths — two waveguides, two fiber arms, whatever the platform offers — and agree that exactly one photon will occupy one or the other of them at any time. Calling "photon in the top path" your logical zero and "photon in the bottom path" your logical one turns a single particle's location into a genuine two-level system, with superpositions of zero and one corresponding physically to the photon being in a coherent superposition of traveling down both paths at once. This is an attractive encoding precisely because the hardware you need to manipulate it — beamsplitters to mix the two paths together, phase shifters to adjust the relative phase between them — is exactly the same linear-optical toolkit used for classical interferometry, so single-qubit gates come essentially for free once you can route light through a network of waveguides and beamsplitters. The price paid for that simplicity shows up elsewhere: because information here is tied to which path a single indivisible photon takes, making two separate photons interact with each other to build a two-qubit gate is a much harder physical problem than manipulating one photon on its own.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Qubit](Qubit.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md)
**Full Derivation:**
