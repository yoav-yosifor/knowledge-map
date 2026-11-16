---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

A real atom's Rabi oscillations don't continue forever. Population decays back to the ground state on a timescale $T_1$ (spontaneous emission), while the phase coherence between ground and excited state is destroyed on a timescale $T_2\leq T_1$. $T_2$ is always shorter because population decay always randomizes phase, but phase can also be scrambled without touching populations at all (pure dephasing).

## Key Equation

$$
T_2 \leq T_1
$$

**Derived From:** every spontaneous emission event irreversibly resets the atom's excited-to-ground amplitude and randomizes its phase, so it always contributes to $T_2$; additional processes (collisions, field fluctuations) can degrade the phase without changing populations, so $T_2$ can only be shorter than, never longer than, $T_1$.

## Supporting Formulas

- $T_1$ (population decay time): rate at which $w\to-1$ (back to ground state) via spontaneous emission — the atom irreversibly loses energy $\hbar\omega_a$ by emitting a photon
- $T_2$ (coherence/decoherence time): rate at which the equatorial Bloch components $u,v\to0$ — loss of the well-defined relative phase between $|g\rangle$ and $|e\rangle$; see [Optical Bloch Vector](Optical%20Bloch%20Vector.md)
- Decomposition into two physically distinct contributions: $1/T_2 = 1/T_2^{(\text{inhomog})} + 1/T_2^{(\text{homog})}$
  - **Homogeneous** ($T_2^{(\text{homog})}$): a random, irreversible phase kick that every atom receives independently — spontaneous emission (contributing $1/2T_1$) and collisions (pressure broadening, $1/T_2^{(\text{collision})}=\gamma_c\propto n\sigma v_\text{rel}$); genuinely irreversible, cannot be undone by any pulse sequence
  - **Inhomogeneous** ($T_2^{(\text{inhomog})}$): different atoms in an ensemble precess at slightly different rates (Doppler shift, spatial field variation, stray static fields); each atom stays perfectly coherent on its own, but the ensemble average washes out as the atoms fan out in phase — see [Inhomogeneous Broadening](Inhomogeneous%20Broadening.md); this contribution **is** reversible, via [Spin Echo (Photon Echo)](Spin%20Echo.md)
- Related, more general concept: [Decoherence](../10%20-%20Quantum%20Information/Decoherence.md) (system–environment entanglement, in the general open-systems sense)

## Derivation Outline

1. Add a phenomenological decay term $-(w+1)/T_1$ to the population (Bloch) equation, representing irreversible spontaneous emission back to the ground state.
2. Add phenomenological decay terms $-u/T_2$, $-v/T_2$ to the coherence equations, representing loss of phase information.
3. Note that spontaneous emission necessarily randomizes phase whenever it happens, so it always contributes to both $1/T_1$ and $1/T_2$; any additional dephasing-only process can only shorten $T_2$ further, giving the inequality $T_2\leq T_1$ (in fact $T_2\leq2T_1$ in the most general convention).

## Physical Intuition

$T_1$ answers "how long does the atom stay excited before it falls back down and emits a photon?" — it is about energy, and once that photon is gone the process cannot be reversed. $T_2$ answers a different question: "how long does the atom remember the precise phase relationship it had with the driving laser?" That memory can be lost in two very different ways. It can be lost because the atom actually falls to the ground state (which necessarily scrambles the phase too, since there's no longer a superposition to have a phase) — that's an unavoidable floor set by $T_1$. Or it can be lost because something perturbs the atom's energy gap for a moment without changing which state it's in — a passing collision, say — leaving the populations untouched but the phase randomized. Since phase loss happens through at least as many channels as population loss, and often more, coherence is always at least as fragile as, and usually more fragile than, population — hence $T_2 \le T_1$.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Optical Bloch Equations](Optical%20Bloch%20Equations.md), [Inhomogeneous Broadening](Inhomogeneous%20Broadening.md), [Spin Echo (Photon Echo)](Spin%20Echo.md), [Decoherence](../10%20-%20Quantum%20Information/Decoherence.md)
**Full Derivation:**
