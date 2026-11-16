---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The von Neumann equation generalizes Schrödinger evolution to mixed states: it governs how the [density matrix](Density%20Matrix.md) of a closed system evolves in time under a Hamiltonian.

## Key Equation

$$
i\hbar\frac{d\rho}{dt} = [H,\rho]
$$

**Derived From:** the Schrödinger equation applied to each pure-state component $|\psi_j\rangle$ of $\rho=\sum_j p_j|\psi_j\rangle\langle\psi_j|$, differentiated as a product and recombined into a commutator with $H$.

## Supporting Formulas

-

## Derivation Outline

1. Write $\rho=\sum_j p_j|\psi_j\rangle\langle\psi_j|$ with fixed, time-independent probabilities $p_j$.
2. Apply the Schrödinger equation $i\hbar\, d|\psi_j\rangle/dt = H|\psi_j\rangle$ to each component $|\psi_j\rangle$ individually.
3. Differentiate $\rho$ as a product, substituting the Schrödinger equation for both $|\psi_j\rangle$ and $\langle\psi_j|$.
4. Recombine the two resulting terms into a commutator: $i\hbar\, d\rho/dt = H\rho-\rho H=[H,\rho]$.

## Physical Intuition

The Schrödinger equation tells you how a single, perfectly known quantum state changes moment to moment, but a mixed state isn't a single state at all — it's a weighted mixture of several possible pure states you're uncertain between. The von Neumann equation is just what you get when you insist that each of those possible pure states, whichever one actually describes the system, obeys the ordinary Schrödinger equation on its own, and then you ask how the whole mixture, weighted by its fixed probabilities, changes as a result. Because the weights themselves never change — the system doesn't get more or less likely to have started in any particular way just because time passes — all of the time dependence has to come from each component state evolving under the same Hamiltonian. Working through what that does to the density matrix, built from products of each state with its own conjugate, naturally produces a difference of two terms: the Hamiltonian acting on the density matrix from one side, minus the density matrix acting back with the Hamiltonian from the other side. That antisymmetric combination is a hallmark of unitary, reversible evolution, and it guarantees that a closed system's mixedness, its entropy and its purity, never changes under this evolution alone, only under measurement or contact with something outside the system.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Density Matrix](Density%20Matrix.md)
**Full Derivation:**
