---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Quantum mechanics does not allow faster-than-light communication, even though entanglement produces nonlocal correlations. A distant party's reduced local statistics never depend on another party's measurement choice. So no usable signal can be sent this way, which keeps quantum mechanics compatible with special relativity.

## Key Equation

$$

$$

**Derived From:** Bob's reduced density matrix $\rho_B$ is independent of which observable Alice chooses to measure on her half of an entangled state (see [Partial Trace](Partial%20Trace.md) — tracing out Alice's system erases any dependence on her measurement basis).

## Supporting Formulas

-

## Derivation Outline

1. Start from a shared entangled state $\rho_{AB}$ held by Alice and Bob.
2. Compute Bob's reduced state via the [Partial Trace](Partial%20Trace.md): $\rho_B=\mathrm{Tr}_A(\rho_{AB})$.
3. The partial trace sums over an orthonormal basis of $A$, erasing any dependence on which observable Alice measured (or whether she measured at all).
4. So $\rho_B$ — and hence Bob's local statistics — is identical regardless of Alice's choice, meaning no message can be sent without separate classical communication.

## Physical Intuition

Entanglement produces correlations between distant particles that are genuinely stronger than anything a classical, locally-realistic world could produce, and it's tempting to think that must mean you could use it to send a message instantly across any distance — Alice does something to her particle, and somehow that choice shows up in what Bob sees on his side, faster than light could ever carry the news. But if you actually ask what Bob sees if he only ever looks at his own particle, ignoring anything Alice tells him afterward, the answer is: exactly the same statistics no matter what Alice decided to measure, or even whether she measured anything at all. All of the strangeness of entanglement lives in the correlations between Alice's results and Bob's results, correlations that only become visible once the two of them compare notes — and comparing notes requires an ordinary classical message that travels no faster than light. Bob's own local statistics, taken in isolation, simply don't carry any fingerprint of Alice's choice, because averaging over Alice's side to get Bob's reduced description washes out any dependence on what she did. That's exactly the safety valve that keeps quantum mechanics compatible with relativity: entanglement can build correlations no classical theory can match, but it can never, by itself, be turned into a communication channel.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Locality](Locality.md), [EPR Argument](EPR%20Argument.md), [Partial Trace](Partial%20Trace.md)
**Full Derivation:**
