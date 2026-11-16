---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The SWAP gate exchanges the states of two qubits.

## Key Equation

$$
\mathrm{SWAP} = \begin{pmatrix} 1&0&0&0\\0&0&1&0\\0&1&0&0\\0&0&0&1 \end{pmatrix}, \qquad |ij\rangle \rightarrow |ji\rangle
$$

**Derived From:** a [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) defined by its action of exchanging the two qubit registers.

## Supporting Formulas

-

## Derivation Outline

1. Define the gate's action directly on the two-qubit computational basis: $|ij\rangle\to|ji\rangle$.
2. Write the corresponding matrix — a permutation matrix, unitary by construction.
3. Since it's a basis permutation, applying it twice returns $|ij\rangle\to|ji\rangle\to|ij\rangle$, so $\mathrm{SWAP}^2=I$.
4. Recognize this as a [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) whose only effect is exchanging the two registers' information.

## Physical Intuition

The SWAP gate does exactly what its name promises and nothing more: whatever information one qubit was carrying, that information ends up on the other qubit instead, and vice versa, with nothing lost, added, or scrambled together in the process. If the first qubit was pointing in some particular direction on the Bloch sphere and the second was pointing in a completely different one, after the swap those two directions have simply traded places between the physical qubits — the total quantum information in the pair is completely unchanged, only its location has moved. This is useful any time the physical layout of a quantum computer doesn't match the logical layout you need for a given algorithm: qubits are often only able to interact directly with their nearest physical neighbors, so if two qubits that need to talk to each other for some later operation are sitting far apart on the chip, a chain of SWAP gates can relocate quantum information across the chip step by step until the two states you actually need to interact are sitting next to each other. Because it's built out of reversible, unitary logic just like every other gate in the circuit model, applying SWAP twice in a row undoes it completely and returns both qubits to exactly where they started, which is exactly what you'd expect from a gate that's just relabeling which physical qubit holds which piece of information.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [CNOT Gate](CNOT%20Gate.md), [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md)
**Full Derivation:**
