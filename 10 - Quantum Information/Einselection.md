---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Einselection (environment-induced superselection) is the mechanism that picks out a preferred, effectively classical basis for a [decohering](Decoherence.md) system. It works because the environmental states correlated with different system states become macroscopically distinguishable from each other. Once that happens, interference between them disappears.

## Key Equation

$$
\langle e_i | e_j \rangle \approx \delta_{ij}
$$

**Derived From:** after system-environment interaction, $|\Psi\rangle=\sum_i\psi_i|i\rangle\otimes|e_i\rangle$; when the environmental branches $|e_i\rangle$ become nearly orthogonal, the reduced density matrix of the system becomes diagonal in the $\{|i\rangle\}$ basis.

## Supporting Formulas

-

## Derivation Outline

1. System-environment interaction produces the correlated state $|\Psi\rangle=\sum_i\psi_i|i\rangle\otimes|e_i\rangle$.
2. The environment records "which-$i$" information physically, so the branches become nearly orthogonal: $\langle e_i|e_j\rangle\approx\delta_{ij}$.
3. The reduced density matrix $\rho_{\text{sys}}=\mathrm{Tr}_{\text{env}}(|\Psi\rangle\langle\Psi|)$ then has its off-diagonal terms suppressed by these vanishing overlaps.
4. Result: $\rho_{\text{sys}}$ becomes (near-)diagonal in the $\{|i\rangle\}$ basis — this is the basis "einselected" as classical.
5. Whichever system basis produces distinguishable environmental records is the one that survives decoherence.

## Physical Intuition

Decoherence tells you that a system's coherence gets smeared out into correlations with the environment, but it doesn't by itself explain a puzzle that follows immediately: why does the world always seem to decohere into one particular, familiar set of classical-looking states — position, say, or "cat alive" versus "cat dead" — rather than some arbitrary superposition of those? Einselection answers that. When a system interacts with its environment, different states of the system tend to leave physically distinguishable imprints on that environment — a photon scattered one way if the cat is alive, another way if it's dead — and the crucial point is that those environmental imprints are, for all practical purposes, never able to overlap with each other again once they're different enough; two macroscopically distinct environmental records simply don't interfere. Whichever basis of system states happens to produce environmental records like that — records that stay distinguishable rather than blurring back together — is the basis that survives as "classical" from the system's point of view, while every other basis gets washed out by the same process. It isn't that nature has a built-in preference for position or any other particular variable in the abstract; it's that whatever variable happens to get robustly copied into the environment by the actual physical interactions at play is the one that ends up looking classical, and for ordinary macroscopic objects that's almost always something like position.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Decoherence](Decoherence.md), [Entanglement](Entanglement.md)
**Full Derivation:**
