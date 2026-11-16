---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

There is no physical process that can perfectly copy an arbitrary unknown quantum state. This is a direct consequence of the linearity of quantum evolution. A universal copier would have to copy non-orthogonal states, and doing so is incompatible with how linear evolution works.

## Key Equation

$$
\nexists\, U \ \text{such that} \ U(|\psi\rangle\otimes|e\rangle) = |\psi\rangle\otimes|\psi\rangle \ \ \forall\, |\psi\rangle
$$

**Derived From:** assume such a $U$ exists for two non-orthogonal states $|\psi\rangle,|\phi\rangle$; linearity of $U$ applied to a superposition of them produces cross terms inconsistent with the claimed output for the superposition itself — a standard proof by contradiction (not spelled out step-by-step in the source).

## Supporting Formulas

- Copying is only possible for a set of known, mutually orthogonal states
- Unknown quantum information cannot be duplicated — classical intuition about replication does not extend to the quantum regime

## Derivation Outline

1. Assume a universal cloning unitary $U$ exists: $U(|\psi\rangle\otimes|e\rangle)=|\psi\rangle\otimes|\psi\rangle$ for all $|\psi\rangle$.
2. Apply $U$ separately to two non-orthogonal states $|\psi\rangle,|\phi\rangle$ — each clones correctly by assumption.
3. Apply $U$ to a superposition of $|\psi\rangle$ and $|\phi\rangle$; linearity forces cross terms that don't match the claimed cloned output of that superposition.
4. Contradiction ⇒ no such $U$ exists for arbitrary states.
5. Only known, mutually orthogonal states can be copied — unknown states cannot.

## Physical Intuition

Photocopying a piece of paper works because the ink is sitting right there in the open — you can look at it and reproduce exactly what you see. An unknown quantum state doesn't offer that: you can't look at it without disturbing it, and even a machine built to copy it without looking would have to work for every possible input, including inputs that are themselves superpositions of two other states it also claims to copy correctly. But a copier is only allowed to relabel one system's information onto a second, blank system in a way that respects how quantum states combine — and a machine that copies two individual states correctly cannot also correctly copy their superposition, because the two requirements pull in mathematically incompatible directions. This isn't a technological limitation waiting for a cleverer engineer to fix; it's baked into the fact that quantum evolution never throws information away or invents it, which is exactly why quantum cryptography can promise that eavesdropping leaves a trace — an eavesdropper can't just quietly clone the qubit in transit and analyze the copy at their leisure.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [No-Deleting Theorem](No-Deleting%20Theorem.md), [Quantum Teleportation](Quantum%20Teleportation.md), [BB84 Protocol](BB84%20Protocol.md)
**Full Derivation:**
