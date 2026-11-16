---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The counter-rotating terms thrown away by the [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md) are not entirely fictitious. Treated as a small perturbation, they push the ground and excited state energies toward each other, shifting the true resonance frequency slightly away from the naive expectation $\omega_L=\omega_a$.

## Key Equation

$$
\Delta\omega_\text{BS} = \frac{\Omega_0^2}{4\omega_a}
$$

**Derived From:** treating the discarded counter-rotating term $\tfrac{\hbar\Omega_0}{2}\sigma_+e^{2i\omega_L t}$ as a second-order perturbation oscillating at frequency $2\omega_L$, and applying the standard second-order energy-shift formula $\delta E_k=\sum_{n\neq k}|\langle n|A|k\rangle|^2/(E_k^{(0)}-E_n^{(0)}-\hbar\alpha)$ to the ground and excited states.

## Supporting Formulas

- Effective detuning with the correction included: $\Delta_\text{eff} = \Delta - \Omega_0^2/(4\omega_a)$
- True resonance condition: $\omega_L = \omega_a + \Omega_0^2/(4\omega_a)$, not $\omega_L=\omega_a$
- Validity/size: negligible for ordinary optical driving ($\Omega_0/\omega_L\sim10^{-6}$, shift $\sim10^{-3}$ Hz), but measurable in NMR and in strongly-driven microwave/RF systems where $\Omega_0/\omega_L$ is not tiny

## Derivation Outline

1. Start from the full (non-RWA) light-matter Hamiltonian, keeping the counter-rotating term the RWA normally discards.
2. Treat that counter-rotating term as a small perturbation acting on the ground and excited atomic states.
3. Apply the standard second-order energy-shift formula to each of the two levels.
4. Take the difference of the two shifts to get the correction $\Delta\omega_\text{BS}$ to the naive resonance frequency.

## Physical Intuition

The Rotating Wave Approximation throws away the counter-rotating terms because their direct, first-order effect on the populations averages to zero — but "averages to zero" is not the same as "has no effect at all." Treated more carefully as a weak perturbation, these terms still nudge the ground and excited state energies slightly, always in the direction of pushing the two levels closer together. That means the atom's transition frequency isn't exactly what the bare RWA picture predicts — the true point of maximum population transfer sits a little off from naive resonance. This is a small, second-order bookkeeping correction rather than a new physical mechanism, and it is a way of quantifying just how good an approximation the RWA actually is: it was first seen experimentally in nuclear magnetic resonance, where the coupling can be a large enough fraction of the drive frequency for this tiny shift to become detectable.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [RWA Rotating-Frame Derivation](RWA%20Rotating-Frame%20Derivation.md)
**Full Derivation:**
