---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

An atom initially excited inside an otherwise-empty cavity coherently exchanges its single quantum of excitation back and forth with the cavity field. These are [Rabi oscillations](Rabi%20Oscillations.md) driven by the vacuum coupling alone, with no classical field present at all.

## Key Equation

$$
|\psi(t)\rangle = \cos(gt)\,|e,0\rangle - i\sin(gt)\,|g,1\rangle
$$

**Derived From:** evolving the initial state $|\psi(0)\rangle=|e,0\rangle$, which lies entirely within the $N_T=1$ block of the [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md) spanned by $\{|e,0\rangle,|g,1\rangle\}$, under $e^{-\frac{i}{\hbar}\hat H_1t}=e^{-ig\hat\sigma_1t}$.

## Supporting Formulas

- Oscillation frequency for this single-quantum exchange: $\Omega_1=2g$ — the $n=1$ case of the general $n$-photon vacuum Rabi frequency $\Omega_n=2\sqrt n\,g$; see [Jaynes-Cummings Dressed States](Jaynes-Cummings%20Dressed%20States.md)
- Observable only in the strong-coupling regime, $g\gg\kappa,\Gamma$, where the coherent atom-field exchange outpaces cavity photon loss ($\kappa$) and spontaneous emission into uncontrolled modes ($\Gamma$); otherwise dissipation interrupts the exchange before a full cycle completes

## Derivation Outline

1. Note that the initial state $|e,0\rangle$ is not an eigenstate of the Jaynes-Cummings Hamiltonian, so it must evolve in time.
2. Restrict attention to the $N_T=1$ block, the only subspace $|e,0\rangle$ couples into, spanned by $\{|e,0\rangle,|g,1\rangle\}$.
3. Apply the time-evolution operator for this 2×2 block directly to $|e,0\rangle$, giving a sinusoidal oscillation between the two basis states at frequency $2g$.

## Physical Intuition

This is the single most striking demonstration that the field is genuinely quantized: put one atom in its excited state inside a cavity with literally zero photons in it, and the atom does not simply decay once and stay decayed — it coherently swaps its excitation back and forth with the cavity field, atom-excited-cavity-empty becoming atom-ground-cavity-with-one-photon and back again, indefinitely, purely because the vacuum field still couples to the atom even with no photons present. A classical field of zero amplitude could never drive any such oscillation, since a classical Rabi oscillation requires a nonzero field amplitude to begin with — this exchange is powered entirely by the same single-photon coupling strength $g$ that also produces the dressed-state splitting. Seeing it in the lab requires the atom-cavity coupling to be faster than any competing loss process, which is exactly the "strong-coupling regime" that defines high-quality cavity QED experiments.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md), [Jaynes-Cummings Dressed States](Jaynes-Cummings%20Dressed%20States.md), [Rabi Oscillations](Rabi%20Oscillations.md)
**Full Derivation:**
