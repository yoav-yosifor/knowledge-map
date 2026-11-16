---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The Bell states are the four maximally [entangled](Entanglement.md) two-qubit states. Together they form an orthonormal basis for the two-qubit Hilbert space. They are also the canonical resource behind [teleportation](Quantum%20Teleportation.md), [superdense coding](Superdense%20Coding.md), and tests of nonlocality.

## Key Equation

$$
|\Phi^\pm\rangle = \frac{|00\rangle \pm |11\rangle}{\sqrt2}, \qquad |\Psi^\pm\rangle = \frac{|01\rangle \pm |10\rangle}{\sqrt2}
$$

**Derived From:** applying [Hadamard Gate](Hadamard%20Gate.md) then [CNOT Gate](CNOT%20Gate.md) to a computational basis state (standard circuit construction; not spelled out in the source).

## Supporting Formulas

- Each Bell state has exactly two nonzero, equal Schmidt coefficients $1/\sqrt2$ — see [Schmidt Decomposition](Schmidt%20Decomposition.md)
- Reduced state of either qubit of any Bell state: $\rho_A=\rho_B=I/2$ (maximally mixed) — see [Partial Trace](Partial%20Trace.md)
- The singlet $|\Psi^-\rangle$ is the EPR state used in [EPR Argument](EPR%20Argument.md)

## Derivation Outline

1. Start from a computational basis state, e.g. $|00\rangle$.
2. Apply a Hadamard to the first qubit: $|00\rangle \to \tfrac{1}{\sqrt2}(|00\rangle+|10\rangle)$.
3. Apply CNOT with that qubit as control: entangles into $\tfrac{1}{\sqrt2}(|00\rangle+|11\rangle)$.
4. Varying the input basis state and its signs generates all four combinations $|\Phi^\pm\rangle,|\Psi^\pm\rangle$.
5. Each has two equal Schmidt coefficients $1/\sqrt2$, so tracing out either qubit gives $\rho=I/2$.

## Physical Intuition

Take two qubits and ask: is there a way to prepare them so that measuring one instantly tells you, with certainty, what you'll get from the other — no matter which basis you choose to measure in — even though neither qubit on its own has a definite state at all? That's what a Bell state is. It isn't that the two qubits secretly agreed on an outcome in advance and are each just carrying their own copy of the answer — look at either qubit by itself and it behaves like a perfect coin flip, carrying no information whatsoever. All of the information lives in the correlation between the two, not in either one individually. There are exactly four independent ways to build this kind of correlation (matching outcomes with a plus or a minus sign, or opposite outcomes with a plus or a minus sign), which is why the four Bell states form a complete alternative way of describing any state of two qubits — asking "which Bell state is this" is just as valid a question as asking "what is qubit one doing and what is qubit two doing," except that second question has no good answer once the pair is entangled.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement](Entanglement.md), [EPR Argument](EPR%20Argument.md), [Superdense Coding](Superdense%20Coding.md), [Quantum Teleportation](Quantum%20Teleportation.md)
**Full Derivation:**
