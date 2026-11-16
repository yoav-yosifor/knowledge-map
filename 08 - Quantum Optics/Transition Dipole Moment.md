---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The transition dipole moment $d_{ij}$ is a fixed, field-independent property of an atom, measuring the geometric overlap between two electronic states. It acts as the "lock" that determines whether a laser can couple two levels at all — regardless of how strong the laser is.

## Key Equation

$$
d_{ij} = \langle i|\hat{\vec{d}}|j\rangle = -e\int \Psi_i^*(\vec{r})\cdot\vec{r}\cdot\Psi_j(\vec{r})\,d^3r
$$

**Derived From:** promoting the classical dipole moment $\vec d = q\vec r$ to a quantum operator $\hat{\vec d} = -e\hat{\vec r}$ (the electron is a probability cloud, not a point charge), then taking its matrix element between two atomic eigenstates $|i\rangle$ and $|j\rangle$.

## Supporting Formulas

- Hermiticity: $d_{ij} = d_{ji}^{*}$ (real for real wavefunctions) — absorption ($j\to i$) and stimulated emission ($i\to j$) share the same coupling strength
- Permanent dipole vanishes for symmetric states: $d_{ii}=0$, because $\Psi_i^*\,\vec r\,\Psi_i$ is an odd function of $\vec r$ and integrates to zero over all space (parity argument) — exception: asymmetric molecules like H₂O, whose charge centers do not coincide, have $d_{ii}\neq0$
- Off-diagonal elements are generally nonzero when the two states have opposite parity (e.g. s↔p), since even×odd×odd = even, and an even function does not integrate to zero
- Dipole matrix for a multi-level atom: $\hat{\vec d} = \sum_{i,j} d_{ij}|i\rangle\langle j|$, assembled by inserting the identity — see [Completeness Relation](../06%20-%20Quantum%20Mechanics%201/Completeness%20Relation.md)
- Selection rules: a transition is allowed if $d_{ij}\neq0$ and forbidden if $d_{ij}=0$; e.g. in a three-level ladder a direct $1\to3$ jump is often forbidden ($d_{13}=0$), forcing the electron through level 2 — unless two-photon excitation (absorbing two photons at half the $1\to3$ gap) bypasses the intermediate state entirely

## Derivation Outline

1. Write the classical electric dipole moment $\vec d = q\vec r$.
2. Promote position to the quantum operator $\hat{\vec r}$ and charge to the electron's $-e$, giving the dipole operator $\hat{\vec d}=-e\hat{\vec r}$.
3. Sandwich $\hat{\vec d}$ between two atomic eigenstates $|i\rangle,|j\rangle$ to form the matrix element $d_{ij}$.
4. Evaluate the resulting integral over the two wavefunctions to read off selection rules from parity/symmetry.

## Physical Intuition

Think of $d_{ij}$ as a locked door between two atomic states: it tells you whether the door can be opened at all, independent of who is pushing on it. The electric field of a laser is the person pushing — how hard, and at what frequency — but if the door itself has no handle (symmetry forbids the transition), no amount of laser power will force it open. Physically, $d_{ij}$ measures how much the electron cloud shaped like state $j$ overlaps, once stretched by the position operator, with the cloud shaped like state $i$; it exists as a fixed number the instant the atom is created, even sitting in complete darkness. Whether a given diagonal element $d_{ii}$ (a permanent dipole) is zero or not comes down to symmetry: if the electron cloud is centered exactly on the nucleus, as it is for a spherical s-orbital, there is no built-in charge separation and no permanent dipole; if the geometry is lopsided, like a bent water molecule, the charge centers are offset and a permanent dipole survives.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Atomic Hamiltonian](Atomic%20Hamiltonian.md), [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Three-Level Atom Configurations](Three-Level%20Atom%20Configurations.md)
**Full Derivation:**
