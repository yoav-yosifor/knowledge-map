---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Probability amplitudes are complex numbers, so outcome probabilities emerge only after those amplitudes are summed coherently. This is why quantum algorithms get their speedup: not from trying every answer at once, but from engineering constructive interference on the correct answers and destructive interference on the wrong ones.

## Key Equation

$$
P = \left| \sum_i a_i \right|^2
$$

**Derived From:** the Born rule applied to a state that is a coherent sum of amplitudes $a_i$ rather than a single term — probabilities add only after the amplitudes are summed and squared, not term by term.

## Supporting Formulas

- Constructive interference amplifies the correct answer's amplitude —
- Destructive interference suppresses incorrect paths' amplitude —

## Derivation Outline

1. Write the amplitude for an outcome as a coherent sum over contributing paths: $\sum_i a_i$.
2. Apply the Born rule to the full sum, not term by term: $P=|\sum_i a_i|^2$.
3. Expanding the square produces cross terms: constructive interference amplifies the correct answer's amplitude, destructive interference suppresses wrong paths.
4. Quantum algorithms engineer these cross terms so wrong answers cancel and the right answer reinforces.

## Physical Intuition

Quantum speedup does not come from "trying all answers" simultaneously — it comes from engineering the interference pattern so that wrong answers cancel out and the right answer reinforces. Quantum algorithms are phase-manipulation protocols, not brute-force parallelism.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Superposition](Superposition.md), [Quantum Parallelism](Quantum%20Parallelism.md)
**Full Derivation:**
