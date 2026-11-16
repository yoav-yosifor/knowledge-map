---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

Every pure bipartite state can be written as a single sum over matched orthonormal basis pairs, with non-negative coefficients. The number of nonzero coefficients — the Schmidt rank — is a complete, exact test of [entanglement](Entanglement.md) for pure states. Rank 1 means separable; rank 2 or higher means entangled.

## Key Equation

$$
|\psi_{AB}\rangle = \sum_i \lambda_i\, |i_A\rangle|i_B\rangle, \qquad \lambda_i \ge 0
$$

**Derived From:** the singular value decomposition of the coefficient matrix of $|\psi_{AB}\rangle$ expressed in any product basis.

## Supporting Formulas

- Exactly one nonzero $\lambda_i$ $\Rightarrow$ separable; two or more $\Rightarrow$ entangled
- Eigenvalues of the reduced state $\rho_A$ (via [Partial Trace](Partial%20Trace.md)) are exactly $\{\lambda_i^2\}$
- Maximally entangled iff all Schmidt coefficients are equal, $\lambda_i = 1/\sqrt d$, equivalently $\rho_A=\rho_B=I_d/d$
- Feeds directly into [Entanglement Entropy](Entanglement%20Entropy.md): $S_{\text{ent}} = -\sum_i \lambda_i^2 \log \lambda_i^2$

## Derivation Outline

1. Write $|\psi_{AB}\rangle$ in any product basis; its coefficients form a matrix $C$.
2. Take the singular value decomposition $C=U\Sigma V^\dagger$, with $\Sigma$ diagonal and non-negative (the $\lambda_i$).
3. Absorb $U$ and $V^\dagger$ into new orthonormal bases $\{|i_A\rangle\}$, $\{|i_B\rangle\}$ for each subsystem.
4. The state collapses to $|\psi_{AB}\rangle=\sum_i\lambda_i|i_A\rangle|i_B\rangle$ — matched pairs, one term per basis vector.
5. Count nonzero $\lambda_i$ (Schmidt rank): one ⇒ separable, two or more ⇒ entangled; the $\lambda_i^2$ are exactly $\rho_A$'s eigenvalues.

## Physical Intuition

Take any pure state of two systems glued together and ask: is there a smart choice of basis, made independently for each half, that makes the joint state look as simple as possible? The Schmidt decomposition says yes — no matter how complicated the state looks in the basis you started with, there always exists a special pairing of basis vectors, one set for each subsystem, such that the whole state collapses into a simple weighted sum where each term pairs up exactly one basis vector from each side. The number of terms you actually need, once you've found this best possible basis, is a property of the state itself, not an artifact of how you chose to write it down, and that number turns out to be exactly the right thing to check for entanglement. If you only ever need one term, the state is just two independent pieces sitting side by side with no genuine correlation between them — pull them apart and each still has a perfectly definite description on its own. The moment you need two or more terms, the two halves can no longer be described independently at all; asking about one half necessarily drags in information about the other. This is also why the coefficients themselves double as a direct readout of how mixed each subsystem looks on its own, and of how much entanglement entropy the pair contains — the more evenly spread these coefficients are, the more thoroughly entangled the state is.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement](Entanglement.md), [Partial Trace](Partial%20Trace.md), [Entanglement Entropy](Entanglement%20Entropy.md), [Entanglement Detection](Entanglement%20Detection.md)
**Full Derivation:**
