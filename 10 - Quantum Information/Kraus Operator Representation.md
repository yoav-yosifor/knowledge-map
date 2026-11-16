---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

Any physically allowed quantum noise process is a completely positive trace-preserving (CPTP) map. Every such map can be written as a sum of Kraus operators acting on the density matrix. Together, this is the general framework for describing open-system, noisy, quantum evolution.

## Key Equation

$$
\mathcal{E}(\rho) = \sum_k E_k\,\rho\,E_k^\dagger, \qquad \sum_k E_k^\dagger E_k = I
$$

**Derived From:** modeling the system's coupling to an environment via a joint unitary evolution, then tracing out the environment (see [Partial Trace](Partial%20Trace.md)) — the Kraus operators $E_k$ arise from that partial trace and the trace-preservation condition follows from unitarity of the joint evolution.

## Supporting Formulas

- See [Depolarizing Channel](Depolarizing%20Channel.md) and [Bit-Flip Channel](Bit-Flip%20Channel.md) for concrete examples

## Derivation Outline

1. Model the system and environment as jointly evolving under one unitary $U$.
2. Expand the environment in a basis and take the partial trace after the joint unitary acts.
3. Each environment-basis branch leaves behind one Kraus operator $E_k$ acting on the system alone.
4. Summing over branches gives the general noisy map $\mathcal{E}(\rho)=\sum_k E_k\rho E_k^\dagger$.
5. Unitarity of the joint evolution forces the completeness relation $\sum_k E_k^\dagger E_k=I$.

## Physical Intuition

A qubit never really evolves in isolation — in any real device it's always coupled, at least a little, to some larger environment you don't have full control over or access to, and the honest way to describe what happens to the qubit alone is to imagine the qubit and its environment evolving together under one perfectly ordinary, reversible unitary evolution, and then admit that you only get to look at the qubit's part of the outcome. The Kraus operators are exactly what's left over once you do that bookkeeping: each one describes one particular "branch" of what could have happened to the environment, weighted by how the environment's own state contributes, and adding up all those branches, each sandwiching the qubit's density matrix from both sides, reconstructs the qubit's noisy evolution without ever having to carry the environment's degrees of freedom around explicitly. The condition that these operators sum up to the identity in a particular combination is just the statement that probabilities have to add up to one no matter which branch actually happened — it's the fingerprint left behind by the fact that the full joint evolution was unitary, even though the qubit's own evolution, once you've thrown away information about the environment, generally isn't. This is why the Kraus picture is the universal language for describing noise: bit flips, phase flips, and any other physically realizable channel are all just different specific choices of these operators.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Decoherence](Decoherence.md), [Depolarizing Channel](Depolarizing%20Channel.md), [Bit-Flip Channel](Bit-Flip%20Channel.md)
**Full Derivation:**
