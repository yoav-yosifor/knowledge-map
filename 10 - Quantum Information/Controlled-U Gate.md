---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

A controlled-$U$ gate applies a [unitary](Unitary%20Quantum%20Gate.md) $U$ to a target qubit only when a control qubit is $|1\rangle$; otherwise it leaves the target untouched. The [CNOT Gate](CNOT%20Gate.md) is the special case $U=X$.

## Key Equation

$$
\text{controlled-}U = |0\rangle\langle0| \otimes I + |1\rangle\langle1| \otimes U
$$

**Derived From:** conditioning the identity/target-unitary choice on the control qubit's basis-state projector.

## Supporting Formulas

-

## Derivation Outline

1. Take the control qubit's two basis projectors, $|0\rangle\langle0|$ and $|1\rangle\langle1|$.
2. Pair $|0\rangle\langle0|$ with the identity $I$ on the target — do nothing.
3. Pair $|1\rangle\langle1|$ with the chosen unitary $U$ on the target — apply $U$.
4. Sum the two terms: $|0\rangle\langle0|\otimes I+|1\rangle\langle1|\otimes U$.
5. Choosing $U=X$ gives CNOT, $U=Z$ gives the controlled-phase gate, and so on.

## Physical Intuition

This is the general template CNOT is one specific example of: pick any single-qubit operation you like — a bit flip, a phase flip, a rotation, anything reversible — and build a two-qubit gate that applies it to the target exactly when the control is 1, and does nothing to the target when the control is 0. Wire in a bit-flip and you get CNOT; wire in a phase-flip and you get a controlled-phase gate; the construction itself doesn't care which operation was chosen. What makes this pattern so central is that it's the standard recipe for turning any single-qubit gate already available into an entangling, two-qubit resource — there's no need for a fundamentally new physical mechanism for every different controlled operation, just a way to condition whatever gate already exists on a control qubit's state.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [CNOT Gate](CNOT%20Gate.md), [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md)
**Full Derivation:**
