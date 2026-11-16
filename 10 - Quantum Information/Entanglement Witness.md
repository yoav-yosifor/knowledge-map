---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

An entanglement witness is an observable that gives a negative expectation value on some [entangled](Entanglement.md) states, while staying non-negative on every separable state. Every entangled state has at least one witness that can detect it. But a given witness is specific: it is tailored to the particular states it was designed to catch.

## Key Equation

$$
\mathrm{Tr}(W\rho) < 0 \ \Rightarrow\ \rho \text{ entangled}, \qquad \mathrm{Tr}(W\sigma) \ge 0 \ \ \forall\, \sigma \text{ separable}
$$

**Derived From:** the geometric separation between the (convex) set of separable states and an entangled state outside it — a hyperplane (the witness) can always be found that separates them.

## Supporting Formulas

-

## Derivation Outline

1. Picture the convex set of all separable states inside the space of all quantum states.
2. An entangled state $\rho$ lies outside this convex set.
3. By the hyperplane separation theorem, there exists an operator $W$ that is non-negative on the entire separable set: $\mathrm{Tr}(W\sigma)\ge0$ for all separable $\sigma$.
4. That same $W$ gives $\mathrm{Tr}(W\rho)<0$ for the entangled state (and nearby entangled states) on the other side.
5. Measuring $\langle W\rangle<0$ in the lab therefore certifies entanglement directly.

## Physical Intuition

Picture the set of all separable, unentangled states as some convex blob sitting inside the much larger space of all possible quantum states — convex because mixing two separable states classically can never create entanglement. If a particular state you care about is entangled, it sits somewhere outside that blob, and a basic fact about convex sets is that you can always find a flat dividing surface — a hyperplane — that has the blob entirely on one side and your point on the other. An entanglement witness is exactly that dividing surface, translated into something you can measure in the lab: it's built so that its expectation value comes out non-negative for absolutely every separable state, no exceptions, but dips negative for the specific entangled state, and often a neighborhood of similar states, it was designed around. That's why a single measurement of the witness's expectation value being negative is enough to certify entanglement with total confidence, no reconstruction of the full state required — but it's also why a witness is never universal: the flat dividing surface that separates the separable blob from one entangled state generally won't separate it from some other entangled state sitting in a completely different direction, so you need a different witness, tailored to each region of entangled states you want to be able to catch.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement Detection](Entanglement%20Detection.md), [Entanglement](Entanglement.md)
**Full Derivation:**
