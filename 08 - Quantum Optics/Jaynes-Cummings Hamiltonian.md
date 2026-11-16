---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Once the field is quantized, the classical Rabi-driving amplitude gets replaced with the annihilation operator $\hat a$. Applying the [rotating wave approximation](Rotating%20Wave%20Approximation.md) to a single cavity mode then gives the Jaynes-Cummings Hamiltonian. It's an exactly solvable model of a two-level atom exchanging single quanta of excitation with a quantized field mode.

## Key Equation

$$
\hat H_{AF} = \hbar g\left(\hat a\,\hat\sigma_++\hat a^\dagger\,\hat\sigma_-\right)
$$

**Derived From:** starting from the dipole-approximation interaction Hamiltonian for a two-level atom coupled to the full multimode quantized field, $\hat H_{AF}=\sum_{k,\lambda}(\hbar g_{k,\lambda}\hat a_{k,\lambda}+\hbar g_{k,\lambda}^*\hat a_{k,\lambda}^\dagger)(\hat\sigma_++\hat\sigma_-)$; moving to the interaction picture, dropping the counter-rotating (non-energy-conserving) terms via the [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md); and restricting to a single field mode as inside a cavity.

## Supporting Formulas

- Single-photon Rabi frequency: $\hbar g_{k,\lambda}=-\sqrt{2\pi\hbar\omega_k}\,d_{eg}\cdot u_{k,\lambda}(\vec R)$ — the interaction energy of the atom with a single quantum of one field mode; see [Transition Dipole Moment](Transition%20Dipole%20Moment.md)
- Total excitation number is conserved: $\hat N_T=\hat a^\dagger\hat a+\hat\sigma_+\hat\sigma_-$, $[\hat H,\hat N_T]=0$ — this is what makes the model exactly solvable, since $\hat H$ block-diagonalizes within each fixed-$N_T$ subspace
- The counter-rotating terms dropped by the RWA (energy-non-conserving processes) are responsible for the atom's self-interaction with the field and induce the Lamb shift
- Strong-coupling condition: $g\gg\kappa,\Gamma$ (coupling dominates over cavity photon loss $\kappa$ and spontaneous emission $\Gamma$) — required to observe coherent exchange of excitation rather than irreversible decay
- Family of related light-matter models, distinguished by whether the RWA is kept and how many two-level systems couple to the mode: Jaynes-Cummings (one atom, RWA), ultra-strong coupling (one atom, no RWA), Tavis-Cummings (many atoms, RWA — equivalent to a single collective angular momentum), Dicke (many atoms, no RWA); the multi-atom models are non-integrable and exhibit chaos, unlike the exactly solvable single-atom JC model

## Derivation Outline

1. Write the fundamental dipole-approximation Hamiltonian for a point charge coupled to the quantized field, splitting it into atomic, field, and interaction pieces.
2. Restrict the atomic part to a single near-resonant transition, reducing it to a two-level (Pauli) Hamiltonian, and expand the dipole operator in ladder-operator form, $\hat d=d_{eg}(\hat\sigma_++\hat\sigma_-)$.
3. Move to the interaction picture and identify the energy-conserving (co-rotating) versus non-energy-conserving (counter-rotating) terms; drop the latter under the rotating wave approximation.
4. Restrict the field to a single mode (a cavity), giving the Jaynes-Cummings interaction Hamiltonian.

## Physical Intuition

Ordinary Rabi oscillations treat the driving field as a classical wave, but once the field itself is quantized, the picture changes: instead of a smooth classical amplitude pushing the atom back and forth, the atom now exchanges *individual photons* with a specific mode of the field, one quantum of excitation at a time. The Jaynes-Cummings Hamiltonian is what is left once you throw away the unphysical bookkeeping trick of simultaneously creating a photon and exciting the atom (or destroying a photon while de-exciting it) — processes that would require energy to appear from nowhere — and keep only the physically sensible events: absorbing a photon while exciting the atom, or emitting one while decaying. Because these processes always trade one unit of "excitation" between the atom and the field, the total number of excitations never changes, which is exactly why the whole infinite-dimensional problem breaks apart into a sequence of simple two-by-two problems, one for each possible excitation number — this is what makes an otherwise complicated coupled quantum system solvable exactly, in closed form.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [Jaynes-Cummings Dressed States](Jaynes-Cummings%20Dressed%20States.md), [Vacuum Rabi Oscillations](Vacuum%20Rabi%20Oscillations.md), [Dispersive Jaynes-Cummings Regime](Dispersive%20Jaynes-Cummings%20Regime.md), [Strong Coherent Field Approximation](Strong%20Coherent%20Field%20Approximation.md)
**Full Derivation:** [Jaynes-Cummings Hamiltonian Derivation](Jaynes-Cummings%20Hamiltonian%20Derivation.md)
