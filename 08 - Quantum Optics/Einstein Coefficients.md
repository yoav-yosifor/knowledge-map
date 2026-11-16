---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Light and a two-level atom exchange energy through exactly three processes: spontaneous emission, absorption, and stimulated emission. Requiring that these three processes drive an ensemble of atoms to the correct thermal equilibrium with the radiation field fixes the ratio between their rate coefficients. That ratio reveals an irreducible asymmetry — spontaneous emission — that has no classical analogue.

## Key Equation

$$
B_{12} = B_{21} \equiv B, \qquad \frac{A}{B} = \frac{\hbar\omega^3}{\pi^2 c^3}
$$

**Derived From:** writing the population rate equation $\dot n_2 = -[A_{21}+B_{21}u(\omega)]n_2 + B_{12}u(\omega)n_1$ for atoms in thermal equilibrium with a radiation field, imposing $\dot n_1=\dot n_2=0$ together with the Boltzmann population ratio $n_2/n_1=e^{-\beta\hbar\omega}$, solving for $u(\omega)$, and matching the result term-by-term against [Planck's Law](Plancks%20Law.md).

## Supporting Formulas

- Three processes: spontaneous emission at rate $A_{21}=\tau_{sp}^{-1}$ (field-independent); absorption at rate $B_{12}u(\omega)$; stimulated emission at rate $B_{21}u(\omega)$ (both proportional to the field energy density)
- Total rates in terms of mean photon number $\langle n\rangle=(e^{\beta\hbar\omega}-1)^{-1}$: $W_\text{em}=A(\langle n\rangle+1)$, $W_\text{abs}=A\langle n\rangle$ — the "+1" is spontaneous emission, with no classical counterpart
- Ratio of spontaneous to stimulated emission: $A/(Bu(\omega)) = 1/\langle n\rangle = e^{\beta\hbar\omega}-1$ — spontaneous emission dominates at optical frequencies and room temperature ($\beta\hbar\omega\gg1$); stimulated processes dominate at low frequency/high temperature ($\beta\hbar\omega\ll1$)
- Explicit atomic formulas in terms of the transition dipole moment: $A_{eg}=\omega_a^3|d|^2/(3\pi\epsilon_0\hbar c^3)$, $B_{ge}=\pi|d|^2/(3\epsilon_0\hbar^2)$ — see [Transition Dipole Moment](Transition%20Dipole%20Moment.md); the $\omega^3$ scaling means spontaneous emission dominates in the UV and is negligible at microwave frequencies
- Quantum (equilibrium-independent) derivation: see [Einstein Coefficients from Fermi's Golden Rule](Einstein%20Coefficients%20Derivation.md)
- Rate-equation solution for resonant incoherent light from the ground state: $P_e(t)=P_e^\infty(1-e^{-\gamma t})$, $P_e^\infty\leq0.5$ — contrast with the coherent-drive result in [Rabi Oscillations](Rabi%20Oscillations.md)

## Derivation Outline

1. Write the population rate equation for a two-level ensemble under all three Einstein processes.
2. Impose thermal equilibrium (zero net population change) and the Boltzmann population ratio between levels.
3. Solve the resulting algebraic equation for the equilibrium energy density $u(\omega)$ and compare it term-by-term to the independently known Planck spectrum, reading off the relations between $A$, $B_{12}$, and $B_{21}$.

## Physical Intuition

Absorption and stimulated emission are mirror images of each other — a photon striking an atom in the lower state kicks it up, and an identical photon striking an atom in the upper state kicks it down, with equal ease in both directions, which is why $B_{12}=B_{21}$. Spontaneous emission is different in kind: an excited atom can fall on its own, with no photon required to trigger it, simply because coupling to the vacuum electromagnetic field is unavoidable. Because these are only three possible things that can happen, and because whatever their individual rates are, they must collectively reproduce the known equilibrium (Planck) spectrum when many atoms interact with a thermal bath of light, the ratio between spontaneous and stimulated rates is not a free parameter — it is locked in by frequency alone. That ratio explains a striking asymmetry in everyday experience: microwave and radio sources are dominated by stimulated-like, coherent, wave-like behavior, while visible light sources are dominated by spontaneous emission, which is exactly why lasers (built on stimulated emission) are comparatively hard to make at optical frequencies but easy to make at microwave frequencies (masers).

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Plancks Law](Plancks%20Law.md), [Transition Dipole Moment](Transition%20Dipole%20Moment.md), [Rabi Oscillations](Rabi%20Oscillations.md)
**Full Derivation:** [Einstein Coefficients from Fermi's Golden Rule](Einstein%20Coefficients%20Derivation.md)
