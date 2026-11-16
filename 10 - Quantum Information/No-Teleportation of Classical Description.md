---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

An unknown quantum state cannot be converted into a classical description — a set of classical bits — that fully specifies it. Measuring a single copy cannot reveal the full state; if it could, the [No-Cloning Theorem](No-Cloning%20Theorem.md) would be violated. [Quantum Teleportation](Quantum%20Teleportation.md) sidesteps this by using pre-shared entanglement, classical communication, and destruction of the original, rather than by reading the state off.

## Key Equation

$$

$$

**Derived From:** if a single measurement could extract a complete classical description of $|\psi\rangle$, that description could be used to prepare arbitrarily many copies — contradicting no-cloning.

## Supporting Formulas

-

## Derivation Outline

1. Suppose a single measurement on an unknown $|\psi\rangle$ could yield a complete classical description of it.
2. That classical description, once written down, could be freely copied and reused to prepare arbitrarily many copies of $|\psi\rangle$.
3. This would amount to cloning an unknown quantum state — contradicting the [No-Cloning Theorem](No-Cloning%20Theorem.md).
4. So no single measurement can extract a full classical description — only a partial, probabilistic glimpse is accessible.
5. [Quantum Teleportation](Quantum%20Teleportation.md) avoids the contradiction by moving the state (via entanglement + classical communication + destruction of the original) rather than reading it off.

## Physical Intuition

You might imagine a lazy way to send a quantum state somewhere: just measure it thoroughly, write down everything you learn as ordinary classical numbers, phone those numbers to whoever needs the state, and have them rebuild it on their end from your classical description — no need for anything exotic. This can't work for an unknown quantum state, and the reason is a short chain of logic rather than a technological limitation: if a single measurement really could squeeze out a complete classical description of an unknown state, then that description, once written down, could be handed out to make as many perfect copies as you like, since classical information can always be copied freely. But that would mean you'd found a backdoor way to clone an unknown quantum state, which is flatly forbidden. So the measurement simply cannot be extracting a complete description in the first place — a single copy of an unknown state only ever gives you a partial, probabilistic glimpse, never the full story. Quantum teleportation gets around this without ever contradicting it: it doesn't measure the state to learn what it is, it consumes a pre-shared entangled pair and a classical message to transplant the state onto a different particle, while destroying the original in the process — moving the state rather than reading it off and copying it.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [No-Cloning Theorem](No-Cloning%20Theorem.md), [Quantum Teleportation](Quantum%20Teleportation.md)
**Full Derivation:**
