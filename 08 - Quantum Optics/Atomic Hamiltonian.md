---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The atomic Hamiltonian isn't derived from the Schrödinger equation. Instead, it's built from the classical energy of the nucleus and electrons — kinetic energy plus Coulomb potential — then quantized by the correspondence principle and simplified by treating the heavy nucleus as fixed.

## Key Equation

$$
\hat{H}_\text{elec} = -\sum_{i=1}^N \frac{\hbar^2}{2m_e}\nabla_i^2 - \sum_{i=1}^N \frac{Ze^2}{4\pi\epsilon_0 r_i} + \sum_{i<j}\frac{e^2}{4\pi\epsilon_0 r_{ij}}
$$

**Derived From:** starting with the classical $H=T+V$ for a nucleus (mass $M$, charge $Ze$) and $N$ electrons (mass $m_e$); applying the correspondence principle $\vec p \to -i\hbar\nabla$ to quantize the kinetic terms; then invoking the Born–Oppenheimer approximation ($M \gg m_e$, so the nucleus barely moves) to drop the nuclear kinetic term, leaving only the electronic Hamiltonian.

## Supporting Formulas

- Full (unreduced) Hamiltonian, before Born–Oppenheimer: $\hat H = -\frac{\hbar^2}{2M}\nabla_n^2 - \sum_i\frac{\hbar^2}{2m_e}\nabla_i^2 - \sum_i\frac{Ze^2}{4\pi\epsilon_0 r_i} + \sum_{i<j}\frac{e^2}{4\pi\epsilon_0 r_{ij}}$
- Time-independent Schrödinger equation: $\hat H|E_j\rangle = E_j|E_j\rangle$ — used to find energy levels and stationary states (no time variable; a static eigenvalue problem)
- Time-dependent Schrödinger equation: $i\hbar\,\partial_t|\Psi(t)\rangle = \hat H|\Psi(t)\rangle$ — used once the atom is driven by a field and evolves in time
- Full driven-atom Hamiltonian: $\hat H_\text{total} = \hat H_0 + \hat H_\text{int}$, where $\hat H_0$ is this atomic Hamiltonian and $\hat H_\text{int}$ is the light–matter coupling — see [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md)

## Derivation Outline

1. Write the classical energy $H=T+V$: kinetic energy of the nucleus and each electron, plus Coulomb attraction (nucleus–electron) and repulsion (electron–electron) potential energy.
2. Quantize by the correspondence principle: replace each classical momentum $\vec p$ with the operator $-i\hbar\nabla$, turning kinetic energy into a Laplacian; potential energy, depending only on position, carries over unchanged.
3. Apply the Born–Oppenheimer approximation: because the nucleus is thousands of times heavier than an electron, it barely accelerates on the electrons' timescale, so its kinetic energy term is dropped, leaving the electronic Hamiltonian used to find atomic orbitals and energy levels.

## Physical Intuition

You cannot derive what the total energy of a system is — you have to know the physics and write it down, the same way you would for any classical system, and only afterward hand it to the Schrödinger equation to find out how that energy plays out. For an atom, the ingredients are simple: how fast the pieces move (kinetic energy) and how the charges pull and push on each other (Coulomb energy). The one physical shortcut that makes atoms tractable is that the nucleus is enormously heavier than the electrons — thousands of times more massive — so on any timescale where the electrons are doing something interesting, the nucleus is essentially standing still. That lets you freeze the nucleus in place and solve for the electrons moving around it, which is the electronic Hamiltonian actually used to compute atomic structure.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Completeness Relation](../06%20-%20Quantum%20Mechanics%201/Completeness%20Relation.md), [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Transition Dipole Moment](Transition%20Dipole%20Moment.md)
**Full Derivation:**
