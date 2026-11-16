---
tags:
  - quantum-information
  - system
  - framework
---
---
## Overview

This is the decision framework for choosing which [entanglement](Entanglement.md) test to apply, given the type and size of the bipartite (or multipartite) system in question. No single method is both complete and easy to apply for every case.

## Prerequisite Concepts

- [Schmidt Decomposition](Schmidt%20Decomposition.md) — complete and exact for pure bipartite states
- [PPT Criterion](PPT%20Criterion.md) — complete for $2\times2$ and $2\times3$ mixed states; only necessary above that
- [Concurrence](Concurrence.md) — complete, closed-form for two-qubit mixed states
- [Entanglement Witness](Entanglement%20Witness.md) — state-dependent, works in general but not universal
- [Entropic Separability Criterion](Entropic%20Separability%20Criterion.md) — necessary, not complete
- [LOCC Criterion](LOCC%20Criterion.md) — the operational ground truth, computationally hard

## Regimes and Parameters

1. Pure bipartite state → Schmidt decomposition or reduced density matrix — complete and exact
2. Mixed state, two qubits ($2\times2$) → PPT or concurrence — complete and exact
3. Mixed state, qubit–qutrit ($2\times3$) → PPT — complete and exact
4. Mixed state, higher dimensions ($\ge 3\times3$) → PPT, then negativity/witnesses, then SDP hierarchies (DPS, NPA) if needed — no single complete simple test
5. Multipartite systems (3+ subsystems) → witnesses, Bell-type inequalities, SDP methods — Schmidt decomposition does not apply

## Physical Intuition

Entanglement is about nonclassical correlations, not purity — the right test to use depends entirely on how big and how mixed the system is, and there is no universal one-shot recipe.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement](Entanglement.md), [CHSH Inequality](CHSH%20Inequality.md)
**Concepts Used:** [Schmidt Decomposition](Schmidt%20Decomposition.md), [PPT Criterion](PPT%20Criterion.md), [Concurrence](Concurrence.md), [Entanglement Witness](Entanglement%20Witness.md), [Entropic Separability Criterion](Entropic%20Separability%20Criterion.md), [LOCC Criterion](LOCC%20Criterion.md)
