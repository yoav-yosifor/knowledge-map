---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The CNOT gate flips a target qubit if and only if a control qubit is $|1\rangle$. It is the canonical two-qubit entangling gate, and it's the special case $U=X$ of a general [Controlled-U Gate](Controlled-U%20Gate.md).

## Key Equation

$$
\mathrm{CNOT} = \begin{pmatrix} 1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0 \end{pmatrix}
\qquad \text{in the basis } \{|00\rangle,|01\rangle,|10\rangle,|11\rangle\}
$$

**Derived From:** a [Controlled-U Gate](Controlled-U%20Gate.md) with $U=X$ (the Pauli bit-flip).

## Supporting Formulas

- Action on basis states: $|00\rangle\to|00\rangle$, $|01\rangle\to|01\rangle$, $|10\rangle\to|11\rangle$, $|11\rangle\to|10\rangle$
- Photonic realization: constructed from a [Controlled-Phase Gate](Controlled-Phase%20Gate.md) (CZ) plus single-qubit gates

## Derivation Outline

1. Start from the general controlled-$U$ template $|0\rangle\langle0|\otimes I + |1\rangle\langle1|\otimes U$.
2. Set $U=X$, the Pauli bit-flip.
3. Read off the basis-state action: control $=0$ leaves target unchanged; control $=1$ flips it ($|10\rangle\leftrightarrow|11\rangle$).
4. Assemble the matrix in the $\{|00\rangle,|01\rangle,|10\rangle,|11\rangle\}$ basis to get the standard CNOT matrix.
5. Photonically, build the same gate from a controlled-phase gate (CZ) plus single-qubit gates.

## Physical Intuition

CNOT is the quantum version of an if-statement: if the control qubit is 1, flip the target; if it's 0, leave the target alone. Run it on two definite, classical-looking inputs and it does exactly that — nothing more interesting than an ordinary conditional. What makes it matter so much more than a classical if-statement is what happens when the control qubit isn't in a definite state at all, but a superposition of 0 and 1 — then the gate has to "flip the target" and "leave it alone" at the same time, in the two branches of that superposition, and those two branches stay linked together afterward. That linking is entanglement: the target's fate becomes correlated with the control's in a way that can't be undone by looking at either qubit alone. This is why CNOT paired with single-qubit gates is enough to build any quantum computation at all — single-qubit gates alone can never create these cross-qubit correlations, so at least one genuinely two-qubit, condition-on-superposition gate like this one has to be in the mix.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Controlled-U Gate](Controlled-U%20Gate.md), [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md), [Controlled-Phase Gate](Controlled-Phase%20Gate.md)
**Full Derivation:**
