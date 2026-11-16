---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Because the [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md) conserves total excitation number, it block-diagonalizes into a sequence of independent 2×2 problems, one per excitation number $n$. Diagonalizing each block mixes the bare atom-plus-$n$-photon states into hybrid "[dressed state](Dressed%20States.md)" polaritons. Their energy splitting grows as $\sqrt n$, producing an anharmonic ladder of levels unlike an ordinary harmonic oscillator.

## Key Equation

$$
E_\pm^{(n)} = \hbar\left(n\omega_c-\frac{\Delta}{2}\right) \pm \frac{\hbar}{2}\sqrt{4ng^2+\Delta^2}
$$

**Derived From:** diagonalizing the $2\times2$ block of the [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md) in the $\{|e,n-1\rangle,|g,n\rangle\}$ basis, $\hat H_n=\hbar(n\omega_c-\Delta/2)\hat I-\tfrac{\hbar\Delta}{2}\hat\sigma_3+\hbar\sqrt n\,g\,\hat\sigma_1$, where $\Delta=\omega_c-\omega_{eg}$ is the cavity-atom detuning.

## Supporting Formulas

- Dressed-state eigenvectors: $|+^{(n)}\rangle=\cos\tfrac{\theta_n}{2}|e,n-1\rangle+\sin\tfrac{\theta_n}{2}|g,n\rangle$, $|-^{(n)}\rangle=\cos\tfrac{\theta_n}{2}|g,n\rangle-\sin\tfrac{\theta_n}{2}|e,n-1\rangle$, with mixing angle $\theta_n=\tan^{-1}(\Omega_n/-\Delta)$
- $n$-photon vacuum Rabi frequency: $\Omega_n\equiv2\sqrt n\,g$ — the coupling term in the block Hamiltonian is $\tfrac{\hbar\Omega_n}{2}\hat\sigma_1$
- On resonance ($\Delta=0$): $\lambda_\pm=\pm\hbar\sqrt n\,g$, an exact analogue of the Autler-Townes splitting, but growing as $\sqrt n$ rather than being fixed — see [Dressed States](Dressed%20States.md) for the classical-field (fixed-amplitude) version of this splitting
- The energy spacing between successive rungs is $\hbar\sqrt{4ng^2+\Delta^2}$, which is *not* proportional to $n$ — unlike a harmonic oscillator's equally-spaced levels, this **anharmonic Jaynes-Cummings ladder** is a direct consequence of the two-level (saturable) atom; the analogous non-linear element in circuit QED is a Josephson junction

## Derivation Outline

1. Use conservation of total excitation number $\hat N_T$ to restrict the Hamiltonian to the two-dimensional subspace $\{|e,n-1\rangle,|g,n\rangle\}$ for each fixed $n$.
2. Write out the matrix elements of $\hat H$ in this basis directly, giving diagonal entries set by the bare atom and field energies and an off-diagonal coupling $\hbar g\sqrt n$.
3. Diagonalize this 2×2 block to obtain the two dressed-state eigenenergies and eigenvectors for each $n$.
4. Take the resonant limit ($\Delta=0$) to read off the symmetric splitting, and note that the $\sqrt n$-dependence of the coupling makes the resulting energy ladder anharmonic.

## Physical Intuition

Once the atom and cavity field are coupled, it no longer makes sense to talk about "the atom's energy" or "the field's energy" separately — the true stationary states are hybrids of both, a mix of "atom excited with $n-1$ photons" and "atom in the ground state with $n$ photons." What makes this system different from the classical-drive case is that the coupling strength itself depends on how many photons are already present: the off-diagonal coupling scales as $g\sqrt n$, so each rung of the excitation ladder splits by a different amount. A harmonic oscillator's levels are all evenly spaced no matter how high you climb, but here the splitting grows more slowly than linearly in $n$ — the ladder becomes anharmonic precisely because a two-level atom can only ever hold one quantum of excitation, so it "saturates" and cannot keep up with an ever-larger field the way a genuine harmonic oscillator would. This saturation-driven anharmonicity is the atomic-physics analogue of what a Josephson junction provides in a superconducting circuit.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md), [Dressed States](Dressed%20States.md), [Vacuum Rabi Oscillations](Vacuum%20Rabi%20Oscillations.md), [Rabi Oscillations](Rabi%20Oscillations.md)
**Full Derivation:**
