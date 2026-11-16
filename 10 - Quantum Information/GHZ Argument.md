---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The GHZ argument uses three entangled qubits to produce a deterministic contradiction with [local realism](Local%20Realism.md). Unlike Bell's theorem, which is statistical, GHZ works in a single run. Assuming predetermined outcomes for a specific set of Pauli measurements leads to constraints that cannot all be satisfied at once — yet quantum mechanics satisfies all of them. This is why it's known as "Bell's theorem without inequalities."

## Key Equation

$$
|\text{GHZ}\rangle = \frac{|000\rangle + |111\rangle}{\sqrt2}
$$

**Derived From:** a three-qubit generalization of the Bell state construction (see [Bell States](Bell%20States.md)).

## Supporting Formulas

-

## Derivation Outline

1. Assume predetermined outcomes exist for Pauli $X$ and $Y$ measurements on each of the three qubits (local realism)
2. Quantum mechanics' predictions for products of these measurements impose a set of sign constraints
3. Those constraints cannot all be satisfied simultaneously by any predetermined assignment
4. Quantum mechanics itself satisfies all of them — local realism cannot

## Physical Intuition

With two entangled particles, a hidden-variable defender can always shrug off the correlations with a statistical argument — "maybe it's just a numbers game, run the experiment enough times and any predetermined-outcome story could still sneak within the observed statistics." Three-way entanglement of the GHZ kind closes that escape hatch completely. Instead of comparing average correlations over many runs, you look at a small handful of very particular measurement combinations on each of the three particles, and ask whether it's even logically possible to write down, in advance, a definite answer for each possible measurement on each particle — an assignment that doesn't know or care what's about to be measured on the other two. It turns out you can't: the pattern of plus and minus signs that quantum mechanics guarantees for these particular combinations, when you try to explain it with predetermined answers, forces one of the combinations to come out with the wrong sign no matter how you fill in the assignment. There's no probability involved and no statistics to gather — a single, perfect run of the experiment is enough to catch nature contradicting any story where the three particles carried pre-agreed answers all along. That's why physicists call this "Bell's theorem without inequalities" — it's not that local realism becomes improbable, it becomes logically impossible, all-or-nothing, in one shot.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [CHSH Inequality](CHSH%20Inequality.md), [Local Realism](Local%20Realism.md), [Bell States](Bell%20States.md)
**Full Derivation:**
