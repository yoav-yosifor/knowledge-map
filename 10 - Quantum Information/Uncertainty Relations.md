---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Uncertainty relations are a structural consequence of non-commuting operators, not a technical limitation of [measurement](Quantum%20Measurement.md) devices. Certain pieces of information simply cannot be simultaneously encoded in a quantum state. The choice of measurement basis is what defines which information exists operationally.

## Key Equation

$$
[A, B] \neq 0
$$

**Derived From:** two observables $A$ and $B$ admit a common eigenbasis, and hence simultaneously sharp values, only if they commute; non-commutativity is what forces a tradeoff in the precision with which both can be known at once.

## Supporting Formulas

- Extracting information about one observable destroys information about its non-commuting conjugate —

## Derivation Outline

1. Take two observables $A$ and $B$ and ask whether they share a common eigenbasis.
2. A common eigenbasis — simultaneously sharp values for both — exists only if $[A,B]=0$.
3. If $[A,B]\neq0$, no such basis exists, so no state has definite values of both at once.
4. Hence extracting information about $A$ necessarily costs information about its non-commuting conjugate $B$ — a structural tradeoff, not a device limitation.

## Physical Intuition

Uncertainty reflects a limit on simultaneous knowledge, not an experimental flaw — the basis you choose to measure in defines what information exists at all, operationally, for the conjugate observable.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quantum Measurement](Quantum%20Measurement.md), [Information-Disturbance Tradeoff](Information-Disturbance%20Tradeoff.md)
**Full Derivation:**
