---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

A state is separable if and only if it can be prepared using only local operations and classical communication (LOCC) between the parties. This makes LOCC conceptually fundamental: it is the operational definition of [entanglement](Entanglement.md). In practice, though, it's computationally hard to check directly.

## Key Equation

$$

$$

**Derived From:** (operational definition, no single formula — see [Entanglement Detection](Entanglement%20Detection.md) for the computable tests used in practice instead.)

## Supporting Formulas

-

## Derivation Outline

1. Two parties act only with local operations on their own subsystem, plus classical communication between them (LOCC).
2. Define a state as separable if and only if it can be prepared this way.
3. This directly captures entanglement as the resource beyond what LOCC alone can create.
4. Verifying "no LOCC protocol produces this state" requires searching over all such protocols — conceptually fundamental but computationally impractical, motivating other detection criteria.

## Physical Intuition

Imagine two experimenters, each holding one half of a shared quantum system, who are allowed to do absolutely anything they like to their own particle in their own lab, and are allowed to pick up the phone and tell each other, in ordinary classical language, what they did and what they got — but they're never allowed to physically bring the two particles together or send anything quantum between them. Whatever joint states these two experimenters can build for themselves using only that toolkit — local fiddling plus a phone call — are, by definition, the separable states: states with no genuine entanglement between the two halves. This gives entanglement its most honest, physically grounded definition, because it directly captures the intuition that entanglement is precisely the resource that lets you do something you couldn't do with local operations and a phone call alone. The catch is that this definition, exactly because it's phrased as "can you or can't you build it this way," doesn't hand you a simple formula or a quick calculation to check — you'd have to search over every conceivable sequence of local operations and classical messages to be sure no LOCC protocol produces a given state, which is why, useful as this criterion is for defining what entanglement means, physicists reach for other, more computable tests when they actually need to detect it in practice.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement Detection](Entanglement%20Detection.md), [Entanglement](Entanglement.md)
**Full Derivation:**
