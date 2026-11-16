---
tags:
  - nanophotonics
  - concept
  - technique
---
---
## Core Idea

Two adjacent single-mode waveguides exchange power through the overlap of their evanescent mode tails; the coupling is treated as a small perturbation on each waveguide's own wave equation, valid under the slowly-varying envelope approximation (SVEA).

## Key Equation

$$
\frac{\partial A}{\partial z}=-i\kappa B(z)e^{2i\delta z},\qquad\frac{\partial B}{\partial z}=-i\kappa A(z)e^{-2i\delta z}
$$

**Derived From:** starting with the wave equation for the full two-waveguide structure, applying a slowly-varying-amplitude ansatz built from each waveguide's own mode, and projecting onto each mode via the power-normalization condition.

- $A(z), B(z)$ — slowly varying amplitudes of the wave in waveguide $a$ and waveguide $b$
- $\kappa$ — coupling coefficient, sets the rate of power exchange between the two waveguides
- $\delta$ — phase-mismatch parameter, $2\delta=(\beta_a+M_{aa})-(\beta_b+M_{bb})$, half the difference between the two waveguides' (shifted) propagation constants; $\delta=0$ means the waveguides are phase-matched — the condition for complete power transfer (see [Directional Coupler](Directional%20Coupler.md)). For two **identical** waveguides, $\beta_a=\beta_b$ and $M_{aa}=M_{bb}$ by symmetry, so $\delta=0$ automatically — this is the case used in [Coupled Waveguide Supermodes](Coupled%20Waveguide%20Supermodes.md).

## Supporting Formulas

- Coupling coefficients: $\kappa_{ab}=\dfrac{\omega}{4}\varepsilon_0\displaystyle\int_{-\infty}^{\infty}E_a^*\Delta n_a^2E_b\,dx$, $\kappa_{ba}=\dfrac{\omega}{4}\varepsilon_0\displaystyle\int_{-\infty}^{\infty}E_b^*\Delta n_b^2E_a\,dx$, with $\kappa_{ab}=\kappa_{ba}^*$ —
- Self-frequency shifts: $M_{aa}=\dfrac{\omega}{4}\varepsilon_0\displaystyle\int_{-\infty}^{\infty}E_a^*\Delta n_b^2E_a\,dx$, $M_{bb}=\dfrac{\omega}{4}\varepsilon_0\displaystyle\int_{-\infty}^{\infty}E_b^*\Delta n_a^2E_b\,dx$ — the shift in each waveguide's own propagation constant caused merely by the presence of the other waveguide
- $M_{aa}$'s integrand is $E_a^*\Delta n_b^2E_a$ — waveguide $a$'s own field on both sides, just weighted by waveguide $b$'s index bump $\Delta n_b^2$. No $E_b$ appears, so no power moves between the guides; it only nudges $a$'s own $\beta_a$, as if mode $a$ feels a slightly different effective index because guide $b$'s core sits nearby — hence "self". That's the opposite role from $\kappa_{ab}$, whose integrand mixes $E_a^*$ and $E_b$ and is what actually transfers power.
- Power conservation: $\dfrac{\partial}{\partial z}\left(|A|^2+|B|^2\right)=0$ 

## Derivation Outline

1. Write the exact field as a superposition of the two waveguides' own modes with slowly varying amplitudes $A(z)$, $B(z)$ (SVEA).
2. Substitute into the full wave equation, drop second derivatives of $A$, $B$ (SVEA), and use each waveguide's own unperturbed mode equation to cancel most terms.
3. Project onto $E_a^*$ and $E_b^*$ and integrate over $x$, using the normalization of the modes, to get the coupled-mode equations for $A(z)$, $B(z)$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Directional Coupler](Directional%20Coupler.md), [Coupled Waveguide Supermodes](Coupled%20Waveguide%20Supermodes.md)
**Full Derivation:** [Coupled Mode Equations Derivation](Coupled%20Mode%20Equations%20Derivation.md)
