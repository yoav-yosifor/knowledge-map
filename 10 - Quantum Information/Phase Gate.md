---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

A photonic phase gate adds a controlled phase to a single optical mode. Physically, it's implemented by a phase shifter. It's the photonic realization of a single-qubit phase rotation.

## Key Equation

$$
|1\rangle \rightarrow e^{i\phi}|1\rangle
$$

**Derived From:** a linear phase shift applied to one mode by a physical phase shifter — a special case of a [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) diagonal in the Fock basis.

## Supporting Formulas

-

## Derivation Outline

1. Start from a general single-mode unitary that is diagonal in the Fock (photon-number) basis.
2. A physical phase shifter delays the mode by a fixed path/medium length, leaving $|0\rangle$ untouched and multiplying $|1\rangle$ by $e^{i\phi}$.
3. Being diagonal, this changes no detection probability — only the phase relationships between photon-number possibilities.
4. Recognize this as the special, single-mode case of a [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) — the photonic realization of a single-qubit phase rotation.

## Physical Intuition

A phase gate does something that sounds almost like nothing at all: it leaves the zero-photon state completely alone and only tags the one-photon state with an extra twist of phase, a kind of bookkeeping angle that doesn't change how likely you are to detect a photon there but does change how that mode interferes with any other mode it later gets combined with. Physically this is about as simple an operation as quantum optics offers — a phase shifter is just a piece of material or path-length delay that a photon in that mode passes through, picking up an extra phase purely because it took slightly longer, or traveled through a slightly different medium, than it would have otherwise. Nothing about which mode the photon is in changes, and nothing about the probability of finding it there changes either — the operation is diagonal in the natural photon-counting basis, touching only the invisible phase relationships between different photon-number possibilities. That's exactly why this gate matters so much for photonic quantum computing even though it looks so unassuming: interference is the entire mechanism by which photonic circuits compute anything, and interference is controlled entirely by relative phase, so a device that does nothing but adjust phase is, in this architecture, doing all of the real work.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md)
**Full Derivation:**
