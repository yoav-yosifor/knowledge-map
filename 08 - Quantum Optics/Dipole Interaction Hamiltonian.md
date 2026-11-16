---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

When a laser illuminates an atom, the field pushes on the atom's dipole, adding extra potential energy to the system. That extra energy is captured by a single off-diagonal coupling term, $\hat H_\text{int}=-\hat{\vec d}\cdot\vec E(t)$, and this term is what actually drives population between atomic levels.

## Key Equation

$$
\hat{H}_\text{int} = -\hat{\vec{d}}\cdot\vec{E}(t)
$$

**Derived From:** the classical interaction energy of a dipole in an external field, $U=-\vec d\cdot\vec E$, promoted to an operator by replacing the classical dipole moment with the quantum dipole operator $\hat{\vec d}=-e\hat{\vec r}$; because it is a potential-energy term (not kinetic), it is labeled $V$ or $H_\text{int}$ rather than $T$.

## Supporting Formulas

- Two-level total Hamiltonian: $\hat H_\text{total} = \begin{pmatrix}E_1 & -d_{12}E(t)\\-d_{12}E(t) & E_2\end{pmatrix}$, built by expanding $\hat d$ in the $\{|1\rangle,|2\rangle\}$ basis, using $d_{11}=d_{22}=0$ (parity) and $d_{21}=d_{12}$ (Hermiticity) — see [Transition Dipole Moment](Transition%20Dipole%20Moment.md)
- Three-level ladder total Hamiltonian: $\hat H_\text{total}=\begin{pmatrix}E_1 & -d_{12}E(t) & 0\\-d_{12}E(t) & E_2 & -d_{23}E(t)\\0 & -d_{23}E(t) & E_3\end{pmatrix}$ — describes cascade systems such as the biexciton emission in a quantum dot, whose two emitted photons are polarization-entangled as a direct consequence of this off-diagonal structure
- Two-laser lab-frame Hamiltonian: every off-diagonal element is driven by the full field $E_\text{total}(t)=E_a\cos\omega_a t + E_b\cos\omega_b t$ — both lasers touch every transition in the lab frame; nothing filters automatically until resonance selects which laser matters for which transition
- Resonance filtering: a laser detuned from a transition ($\omega_{ij}-\omega_\text{laser}=\Delta\neq0$) time-averages to zero on that transition, $\langle e^{i\Delta t}\rangle_t=0$, while a laser tuned to resonance ($\Delta=0$) survives the average — see [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md)

## Derivation Outline

1. Split the total Hamiltonian into the field-free atom and the field coupling: $\hat H_\text{total}=\hat H_0+\hat H_\text{int}$ — see [Atomic Hamiltonian](Atomic%20Hamiltonian.md).
2. Write the interaction energy in the dipole approximation as $\hat H_\text{int}=-\hat{\vec d}\cdot\vec E(t)$, treating the field as spatially uniform across the atom (valid because the laser wavelength is vastly larger than the atom).
3. Expand $\hat d$ in the energy eigenbasis using the completeness relation, keep only the surviving off-diagonal elements (parity forces diagonal terms to vanish), and multiply by $-E(t)$ to get the explicit matrix form of the interaction.
4. Assemble $\hat H_0+\hat H_\text{int}$ into the full time-dependent Hamiltonian; inserting this into the time-dependent Schrödinger equation produces Rabi oscillations — see [Rabi Oscillations](Rabi%20Oscillations.md).

## Physical Intuition

When the laser's electric field oscillates, it pushes on the light, mobile electron cloud far more than on the heavy, nearly stationary nucleus — the same force accelerates a light object much more than a heavy one. So the laser effectively sloshes the electron cloud back and forth across a fixed nucleus, creating an oscillating dipole. The interaction Hamiltonian is exactly the energy cost of that push: since the dipole operator has no diagonal part (parity forbids a permanent displacement in a single eigenstate), the field cannot change a level's own energy directly — it can only appear as an off-diagonal term that stirs population between levels. In a lab with multiple lasers hitting a multi-level atom, every laser touches every transition mathematically, but only a laser whose frequency matches a transition's own energy gap survives the rapid time-averaging and actually drives it — every other laser's push cancels itself out over the timescale of the dynamics.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Atomic Hamiltonian](Atomic%20Hamiltonian.md), [Transition Dipole Moment](Transition%20Dipole%20Moment.md), [Rabi Oscillations](Rabi%20Oscillations.md), [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [Electric Field Operator](Electric%20Field%20Operator.md)
**Full Derivation:**
