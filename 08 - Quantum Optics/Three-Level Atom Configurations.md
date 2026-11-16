---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Extending from two to three levels opens up three topologically distinct wiring diagrams — Lambda, V, and ladder — depending on which pairs of states each of two laser fields couples. The Lambda configuration is especially important: two stable ground states are bridged through one excited state. That structure is what makes long-lived coherences, [dark states](Dark%20State.md), and [STIRAP](STIRAP.md) possible.

## Key Equation

$$
H_{\text{RWA}} = \hbar \begin{pmatrix} 0 & \Omega_1 & 0 \\ \Omega_1^* & \Delta_1 & \Omega_2 \\ 0 & \Omega_2^* & \Delta_1-\Delta_2 \end{pmatrix}
$$

**Derived From:** the full Lambda-system Hamiltonian $H=H_0+\hat d_{13}E_1(t)+\hat d_{23}E_2(t)$, moved to a rotating frame that removes the fast optical oscillations (via a unitary that absorbs each laser's phase) and truncated by the rotating wave approximation — in the basis $\{|1\rangle,|3\rangle,|2\rangle\}$, dropping the counter-rotating terms exactly as in the two-level case; see [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md).

## Supporting Formulas

- Rabi frequencies for each leg: $\Omega_1=d_{13}E_1/\hbar$, $\Omega_2=d_{23}E_2/\hbar$ — see [Transition Dipole Moment](Transition%20Dipole%20Moment.md)
- Single-photon detunings: $\Delta_1=\omega_{L1}-\omega_{31}$, $\Delta_2=\omega_{L2}-\omega_{32}$
- Two-photon (Raman) detuning: $\delta=\Delta_1-\Delta_2$ — the Raman resonance condition is $\delta=0$; the ground-state coherence evolves at this rate and can be very long-lived when both lasers are phase-locked near two-photon resonance
- Configurations: **Lambda** — two ground states $|1\rangle,|2\rangle$ coupled to one excited state $|3\rangle$, with $|1\rangle\leftrightarrow|2\rangle$ dipole-forbidden; **V** — one ground state coupled to two excited states; **Ladder (cascade)** — three states in an energy staircase, each field coupling adjacent rungs
- Off-diagonal structure: only the excited state directly couples to both ground states in a Lambda system — the $|1\rangle\leftrightarrow|2\rangle$ matrix element is exactly zero, consistent with the topology
- Open-system extension: spontaneous emission from the excited state feeds both ground states via a Lindblad dissipator with rates $\gamma_{31},\gamma_{32}$ (total $\gamma_3=\gamma_{31}+\gamma_{32}$), damping the optical coherences on timescale $1/\gamma_3$ while leaving the ground-state coherence comparatively protected

## Derivation Outline

1. Write the bare three-level Hamiltonian $H_0$ (diagonal, one entry per level) and add the two dipole-coupling terms, one per laser field, each connecting the excited state to one of the other two levels.
2. Choose a rotating-frame ansatz that strips the fast optical-frequency oscillation from each amplitude, using each laser's own frequency as the reference for the state(s) it couples to.
3. Apply the RWA (drop counter-rotating terms) to obtain the time-independent matrix above, whose off-diagonal pattern encodes exactly which pairs of levels are coupled — i.e. the configuration (Lambda, V, or ladder).

## Physical Intuition

A two-level atom can only ever do one thing: oscillate between "up" and "down." Adding a third level and a second laser opens up qualitatively new behavior, because now there are two coupling pathways that can interfere with each other. The Lambda configuration is special because its two "ground" states are both metastable — neither one wants to decay on its own — so any coherence built up between them can survive far longer than any coherence involving the fragile, fast-decaying excited state. That long-lived ground-state coherence, protected from the leaky excited state, is exactly the resource that dark states and STIRAP exploit: population can be shuttled between the two stable ground states while spending as little time as possible actually sitting in the lossy excited state.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Dark State](Dark%20State.md), [STIRAP](STIRAP.md), [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Saturation Parameter](Saturation%20Parameter.md)
**Full Derivation:**
