---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Von Neumann entropy is the quantum analogue of [Shannon entropy](Shannon%20Entropy.md), applied to a [density matrix](Density%20Matrix.md) instead of a classical probability distribution. It vanishes exactly for pure states, and it stays invariant under unitary evolution.

## Key Equation

$$
S(\rho) = -\mathrm{Tr}(\rho\log\rho) = -\sum_i \lambda_i \log \lambda_i
$$

**Derived From:** [Shannon Entropy](Shannon%20Entropy.md) applied to the eigenvalues $\lambda_i$ of $\rho$, since $\rho$ is diagonalizable with the $\lambda_i$ forming a genuine probability distribution.

## Supporting Formulas

- $S(\rho)=0$ iff $\rho$ is pure; $S(\rho)\le\log d$ for a $d$-dimensional system
- Entropy is invariant under unitary evolution

## Derivation Outline

1. Diagonalize $\rho$ (always possible since it's Hermitian): $\rho=\sum_i\lambda_i|i\rangle\langle i|$, with the $\lambda_i$ forming a genuine probability distribution.
2. Apply the [Shannon Entropy](Shannon%20Entropy.md) formula to these eigenvalues: $S(\rho)=-\sum_i\lambda_i\log\lambda_i=-\mathrm{Tr}(\rho\log\rho)$.
3. For a pure state exactly one $\lambda_i=1$, so $S(\rho)=0$; entropy grows toward $\log d$ as the mixture spreads out.
4. Since unitary evolution only rotates the diagonalizing basis without changing the $\lambda_i$, $S(\rho)$ is invariant under it.

## Physical Intuition

Von Neumann entropy answers the same question Shannon entropy does — how much genuine uncertainty is baked into this description — except now the description is a density matrix rather than a classical list of probabilities. The trick that makes this work is that any density matrix, no matter how it was built up, can always be diagonalized, meaning it has some special basis in which it looks exactly like a classical probability distribution over a set of definite states. Von Neumann entropy is just Shannon's formula applied to those eigenvalues. This immediately tells you why a pure state has zero entropy: a pure state is already a single definite state vector, so in its own diagonal basis there's exactly one nonzero probability, equal to one, and no uncertainty left to quantify — the classical formula for a sure thing gives zero, and that carries straight over. A mixed state, by contrast, is genuinely spread across more than one such possibility, so its entropy is positive, growing larger the more evenly that spread is distributed, up to a maximum set by the size of the system. And because ordinary unitary evolution just rotates that diagonal basis around without ever creating or destroying probability weight on the underlying possibilities, it can't change how spread out those weights are — which is exactly why entropy stays fixed under any evolution that doesn't involve measurement or contact with an external system.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Shannon Entropy](Shannon%20Entropy.md), [Entanglement Entropy](Entanglement%20Entropy.md), [Density Matrix](Density%20Matrix.md)
**Full Derivation:**
