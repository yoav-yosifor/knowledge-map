---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

It is impossible to gain information about a quantum state without disturbing it, unless the candidate states are orthogonal. Non-orthogonal states cannot be perfectly distinguished, and any measurement that extracts information about them necessarily alters the state. This is the physical principle underlying the security of [BB84](BB84%20Protocol.md).

## Key Equation

$$

$$

**Derived From:** the relevant observables that distinguish non-orthogonal states do not commute (see [Uncertainty Relations](Uncertainty%20Relations.md)); measurement requires coupling the system to a device or environment, which inevitably introduces back-action.

## Supporting Formulas

- There is a fundamental tradeoff between information gain and disturbance: the more information extracted, the greater the disturbance

## Derivation Outline

1. If candidate states are orthogonal, a measurement exists that distinguishes them perfectly without altering them.
2. If candidate states are non-orthogonal, the observables that would distinguish them do not commute.
3. Measurement requires coupling the system to a device sensitive to that non-commuting observable, which inevitably back-acts on the state.
4. Hence any information gained about non-orthogonal states necessarily disturbs them, with more information forcing more disturbance.
5. This tradeoff is what lets protocols like BB84 detect an eavesdropper via the errors that disturbance leaves behind.

## Physical Intuition

If someone hands you a qubit prepared in one of two possible states that happen to be orthogonal — completely distinguishable, like straight up versus straight down — you can measure it and learn exactly which one it was without leaving any trace on the state at all, because there's a measurement perfectly matched to telling those two apart cleanly. The moment the two candidate states are not orthogonal, that clean measurement doesn't exist: any way of asking a question that gives you real information about which state it was is also a way of nudging the state itself, because the very act of coupling your measuring device to the qubit in a way that's sensitive to the difference between two overlapping states inevitably changes those states. This isn't a matter of clumsy engineering — it is built into the structure of quantum mechanics, since the observables that would perfectly reveal one candidate state at all necessarily fail to leave the other one alone. The more aggressively you try to squeeze information out of the qubit, the more violently you have to disturb it to do so, and there's a hard tradeoff between the two that no measurement strategy can cheat. This is exactly the physical fact that lets a quantum key distribution protocol catch an eavesdropper: anyone trying to learn something about the qubits in transit is physically forced to leave fingerprints on them, and those fingerprints show up as detectable errors.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Uncertainty Relations](Uncertainty%20Relations.md), [BB84 Protocol](BB84%20Protocol.md)
**Full Derivation:**
