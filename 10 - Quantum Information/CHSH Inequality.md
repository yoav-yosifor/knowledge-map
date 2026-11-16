---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Bell proved that any [local hidden-variable theory](Local%20Realism.md) must obey certain inequalities on the correlations between distant measurements. Quantum mechanics predicts that these inequalities can be violated, and experiments confirm it. That violation means no locally realistic theory can reproduce all of quantum mechanics' predictions.

## Key Equation

$$
\langle QS\rangle + \langle RS\rangle + \langle RT\rangle - \langle QT\rangle \le 2 \qquad \text{(CHSH, local realism)}
\qquad\qquad
\langle B_{\text{CHSH}}\rangle = 2\sqrt2 > 2 \qquad \text{(quantum prediction)}
$$

**Derived From:** four observables — Alice's $Q,R$ and Bob's $S,T$ — combined under the assumption of [Local Realism](Local%20Realism.md); the bound of 2 follows from that assumption alone, and quantum mechanics exceeds it for suitable measurements on an entangled state.

## Supporting Formulas

- Assumptions behind the inequality: realism (pre-existing outcomes), locality (no distant influence), measurement independence (free choice of settings) — at least one must fail in nature
- Experiments confirm the quantum violation $2\sqrt2$

## Derivation Outline

1. Assume local realism: each particle carries predetermined outcomes $Q,R,S,T\in\{\pm1\}$, fixed before measurement.
2. Note the algebraic identity: for any fixed values, $QS+RS+RT-QT=\pm2$.
3. Average over the hidden-variable distribution: $|\langle QS\rangle+\langle RS\rangle+\langle RT\rangle-\langle QT\rangle|\le2$.
4. Compute the same combination quantum mechanically on an entangled state with suitable settings, giving $2\sqrt2$.
5. Since $2\sqrt2>2$, the local-realist bound is violated.

## Physical Intuition

Suppose two distant experimenters each get to choose between two possible measurement settings on their half of a shared pair, and suppose further that each particle actually carried a definite, pre-agreed answer to every possible question before it ever left the source — the "local hidden variable" picture Einstein favored. Under that picture alone, with no reference to quantum mechanics at all, you can prove that a specific combination of correlations between the two sides' results, added and subtracted in a particular pattern, can never exceed a fixed bound. That bound isn't a feature of any particular physical theory; it's pure logic about what's achievable by any scheme where the particles' answers were fixed in advance and neither side can influence the other faster than light. The surprise is that entangled quantum particles, measured this same way, produce correlations that blow straight past that bound, and real experiments confirm it. Since the bound followed from nothing but locality, pre-existing answers, and free choice of settings, a violation forces you to give up at least one of those three assumptions about how nature works — you can keep locality and lose realism, or vice versa, but you can't keep both. That's what makes this a genuine no-go theorem rather than just an interesting statistic.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Local Realism](Local%20Realism.md), [EPR Argument](EPR%20Argument.md), [GHZ Argument](GHZ%20Argument.md), [Entanglement Detection](Entanglement%20Detection.md)
**Full Derivation:**
