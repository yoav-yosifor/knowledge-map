---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

For any separable state, the [entropy](Von%20Neumann%20Entropy.md) of each subsystem cannot exceed the entropy of the joint state. A violation of this inequality proves entanglement. But satisfying the inequality doesn't prove separability — it's a necessary condition, not a sufficient one.

## Key Equation

$$
S(\rho_A) \le S(\rho_{AB}), \qquad S(\rho_B) \le S(\rho_{AB})
$$

**Derived From:** subadditivity properties of the von Neumann entropy for separable (classically correlated) states.

## Supporting Formulas

-

## Derivation Outline

1. For any separable (classically correlated) state, subadditivity of the von Neumann entropy holds.
2. This gives the inequality $S(\rho_A)\le S(\rho_{AB})$ and $S(\rho_B)\le S(\rho_{AB})$.
3. Entanglement can break this: a pure joint state ($S(\rho_{AB})=0$) can still have $S(\rho_A)>0$.
4. So finding $S(\rho_A)>S(\rho_{AB})$ proves the state cannot be separable.
5. Satisfying the inequality does not prove separability — it is a one-way (necessary, not sufficient) test.

## Physical Intuition

For an ordinary classical probability distribution over two variables, there's a familiar fact: knowing both variables together can never leave you more uncertain than knowing just one of them on its own — the whole is at least as informative as any one part. That same inequality holds for any quantum state that's separable, meaning it could have been built entirely out of classical correlations between two local descriptions, because in that case the joint entropy still behaves the way ordinary classical entropy does. What's genuinely quantum, and genuinely surprising if you're used to classical intuition, is that entanglement breaks this rule outright: a globally pure, zero-entropy entangled state can have subsystems whose individual entropy is enormous, because entanglement lets the parts each look maximally uncertain while the whole is perfectly known. So checking whether a subsystem's entropy exceeds the joint entropy is a direct test for exactly this classically-impossible signature — if you find it, the state cannot possibly have been separable, full stop, no other explanation available. What this test can't do is clear a state of suspicion: plenty of entangled states still happen to satisfy the classical-looking inequality, so passing the test tells you nothing conclusive, and you're left needing a stronger, more complete criterion to actually rule entanglement out.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement Detection](Entanglement%20Detection.md), [Von Neumann Entropy](Von%20Neumann%20Entropy.md)
**Full Derivation:**
