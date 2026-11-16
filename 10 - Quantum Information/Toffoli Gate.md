---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The Toffoli (CCNOT) gate flips a target qubit only if both of two control qubits are $|1\rangle$. It is a universal reversible classical gate, and it's fundamental for fault-tolerant constructions.

## Key Equation

$$

$$

**Derived From:** a three-qubit generalization of [Controlled-U Gate](Controlled-U%20Gate.md) with two control qubits and $U=X$; (explicit $8\times8$ matrix not given in the source).

## Supporting Formulas

-

## Derivation Outline

1. Take the [Controlled-U Gate](Controlled-U%20Gate.md) construction and generalize it to two control qubits instead of one.
2. Set the applied unitary to $U=X$ (bit flip) on the target qubit.
3. Define the action: flip the target iff both controls are $|1\rangle$, otherwise leave it alone — a reversible quantum AND.
4. Note reversibility (Toffoli$^2=I$) is required since quantum evolution cannot discard information the way classical AND/OR gates do.

## Physical Intuition

Think of the Toffoli gate as a quantum stand-in for the classical logical AND, wired up so that it never destroys information. It looks at two control qubits, and only if both of them are in the "on" state does it flip a third, target qubit; if either control is "off," the target is left completely alone. What makes this more than just a curiosity is that it's reversible — running it twice undoes it, and knowing the output always lets you reconstruct the input — which is exactly the property an operation needs to be allowed as a genuine quantum gate, since quantum evolution can never throw information away the way an ordinary classical AND gate does. Because you can build every classical logic function, including irreversible ones like AND and OR, out of Toffoli gates wired together with some fixed extra "helper" qubits, having this one gate available is enough to reproduce the whole of classical computation inside a reversible, quantum-compatible circuit. That's also why it keeps showing up as scaffolding inside larger, fault-tolerant constructions: whenever an algorithm needs an ordinary classical decision made conditionally on two other qubits' values, without measuring anything or breaking the delicate coherence of the rest of the circuit, the Toffoli gate is the natural tool for making that decision reversibly.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [CNOT Gate](CNOT%20Gate.md), [Controlled-U Gate](Controlled-U%20Gate.md)
**Full Derivation:**
