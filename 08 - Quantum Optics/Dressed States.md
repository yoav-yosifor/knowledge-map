---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Diagonalizing the [RWA Hamiltonian](Rotating%20Wave%20Approximation.md) mixes the bare atom-plus-field states into new hybrid eigenstates called "dressed states." How this hybridization shows up depends on how far the laser is detuned. On resonance, it splits the absorption line into two resolvable peaks; far off resonance, it instead produces a small shift of the atomic energy levels.

## Key Equation

$$
\lambda_\pm = \frac{\Delta}{2} \pm \frac{1}{2}\sqrt{\Delta^2+\Omega_0^2}
$$

**Derived From:** diagonalizing the RWA Hamiltonian $H_\text{RWA}=\hbar\begin{pmatrix}0&\Omega_0/2\\\Omega_0/2&\Delta\end{pmatrix}$ — see [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md); the eigenvalues are the dressed-state energies and the eigenvectors are the dressed states.

## Supporting Formulas

- On resonance ($\Delta=0$, Autler-Townes limit): eigenstates are the equal superpositions $|\pm\rangle=\tfrac{1}{\sqrt2}(|g\rangle\pm|e\rangle)$ with energies $\lambda_\pm=\pm\Omega_0/2$; the original degenerate levels split by $\hbar\Omega_0$, so instead of one absorption line at $\omega_a$ one observes two lines at $\omega_a\pm\Omega_0/2$ (the **Autler–Townes splitting**), with the coupling strength read directly off the splitting
- Far off resonance ($\Delta\gg\Omega_0$, AC Stark limit): $\lambda_\pm\approx\Delta-\Omega_0^2/(4\Delta)$ and $\Omega_0^2/(4\Delta)$ — the ground state is shifted down (more stable) and the excited state shifted up by $\Omega_0^2/(4\Delta)$, even though no real photon is absorbed; this is the **AC Stark effect**, and it is the mechanism behind optical tweezers (atoms are attracted to high-intensity regions of a red-detuned trap, repelled in a blue-detuned trap)

## Derivation Outline

1. Start from the time-independent RWA Hamiltonian, whose diagonal entries are $0$ and $\Delta$ and whose off-diagonal entries are the coupling $\Omega_0/2$.
2. Diagonalize this $2\times2$ matrix to find its two eigenvalues (the dressed-state energies) and eigenvectors (the dressed states, hybrid atom-field superpositions).
3. Take the two physically distinct limits — zero detuning versus large detuning — to read off the Autler-Townes splitting and the AC Stark shift respectively.

## Physical Intuition

Once a laser is coupling two atomic levels, it no longer makes sense to think of "the atom's energy levels" as fixed quantities independent of the light shining on it — the atom and the field's coupling together define new, hybrid energy levels, the dressed states. Exactly on resonance, the coupling is strong enough to fully split what used to be a single, degenerate pair of levels into two distinguishable dressed levels separated by the Rabi frequency — so instead of one absorption peak you see two, and the gap between them is a direct, calibration-free measurement of how strongly the laser couples to the atom. Tune the laser far away from resonance instead, and the levels barely mix — but they still repel each other slightly, the way two nearly-decoupled oscillators always push each other's frequencies apart a little when weakly coupled. That small repulsion is the AC Stark shift: the atom's energy levels move even though it never actually absorbs the light, simply because the light is "nearby" in energy and always pushes.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [Rabi Oscillations](Rabi%20Oscillations.md), [Dark State](Dark%20State.md)
**Full Derivation:**
