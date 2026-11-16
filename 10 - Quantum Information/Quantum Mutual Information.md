---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Quantum mutual information measures the total correlations between two subsystems of a joint state, classical and quantum combined. It vanishes exactly when the state is a product state.

## Key Equation

$$
I(A:B) = S(\rho_A) + S(\rho_B) - S(\rho_{AB})
$$

**Derived From:** [Von Neumann Entropy](Von%20Neumann%20Entropy.md) of each marginal minus the joint entropy — the quantum generalization of classical mutual information.

## Supporting Formulas

- $I(A:B)=0$ iff $\rho_{AB}=\rho_A\otimes\rho_B$
- For pure entangled states: $I(A:B) = 2S(\rho_A)$
- $S(\rho_A)$: local uncertainty about $A$ alone; $S(\rho_B)$: local uncertainty about $B$ alone; $S(\rho_{AB})$: whether the joint state is pure or mixed (by itself does not indicate entanglement)

## Derivation Outline

1. Take the marginal [Von Neumann Entropy](Von%20Neumann%20Entropy.md)s $S(\rho_A)$, $S(\rho_B)$ and the joint entropy $S(\rho_{AB})$.
2. Define $I(A:B)=S(\rho_A)+S(\rho_B)-S(\rho_{AB})$, the quantum generalization of classical mutual information.
3. Check $I(A:B)=0$ exactly when $\rho_{AB}=\rho_A\otimes\rho_B$ — no shared correlations.
4. For a pure entangled state, $S(\rho_{AB})=0$ and $S(\rho_A)=S(\rho_B)$, so $I(A:B)=2S(\rho_A)$.

## Physical Intuition

Imagine trying to describe two subsystems together versus describing each one separately. If they don't know anything about each other, then the uncertainty in describing them jointly is just the sum of the uncertainty in describing each one alone — nothing is gained or lost by considering them together instead of apart. Quantum mutual information measures exactly the shortfall from that independent-description baseline: it's the amount by which the joint description is more compact, more predictable, than the sum of the two separate descriptions would suggest, and that shortfall exists precisely because the two subsystems share correlations, whether those correlations are the everyday classical kind or the distinctively quantum kind coming from entanglement. When the joint state truly factorizes into independent pieces, there's nothing shared to exploit, and the quantity vanishes exactly, not approximately. At the other extreme, a pure entangled pair has no uncertainty at all when you consider the whole system together, since a pure state is fully specified, yet each half individually looks maximally uncertain when you can only access it on its own — so all of the joint state's information content shows up as correlation between the two halves rather than as a well-defined value for either half, and this is why the double-counting works out to exactly twice the local uncertainty of just one of the two subsystems.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Von Neumann Entropy](Von%20Neumann%20Entropy.md), [Quantum Discord](Quantum%20Discord.md), [Entanglement Entropy](Entanglement%20Entropy.md)
**Full Derivation:**
