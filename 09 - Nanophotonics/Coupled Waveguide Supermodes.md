---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A compound waveguide made of two coupled single-mode waveguides supports exactly two eigenmodes ("supermodes") — a symmetric and an antisymmetric combination of the two individual waveguides' own mode profiles, each with its own propagation constant.

## Key Equation

$$
\beta_{1,2}=\beta_0\pm|\kappa|,\qquad E_1=\frac{1}{\sqrt2}(E_a+E_b),\qquad E_2=\frac{1}{\sqrt2}(E_a-E_b)
$$

**Derived From:** starting with a trial eigenmode written as a fixed superposition $C_aE_a+C_bE_b$, applying the wave equation and the power-normalization condition, for the case of two identical waveguides.

- $\beta_0$ — the common propagation constant of the two individual waveguides on their own (identical, so $\beta_a=\beta_b=\beta_0$)
- $\kappa$ — the same coupling coefficient as in [Coupled Mode Theory](Coupled%20Mode%20Theory.md)
- $\beta_1,\beta_2$ — the propagation constants of the two supermodes, split symmetrically above and below $\beta_0$
- $E_1,E_2$ — the symmetric and antisymmetric mode profiles of the compound waveguide

This is the $N=2$ case of a more general pattern — for $N>2$ coupled waveguides, see [Waveguide Array Supermodes](Waveguide%20Array%20Supermodes.md).

## Supporting Formulas

- General (non-identical waveguide) overlap-integral form: $\beta_1^2=\beta_0^2+\dfrac{K+J}{1+I}$, $\beta_2^2=\beta_0^2+\dfrac{K-J}{1-I}$, with $I=\int E_b^*E_a\,dx$ and $J,K$ the corresponding coupling overlap integrals —
- Cross-checked directly from CMT: for identical waveguides $\beta_a=\beta_b$ and $M_{aa}=M_{bb}$, so $\delta=0$ automatically, and the CMT eigenvalue problem gives $\gamma=\pm|\kappa|$, with eigenvectors $E_1=(1,1)$, $E_2=(1,-1)$ — matching $\beta_{1,2}=\beta_0\pm|\kappa|$ above —

## Derivation Outline

1. Write a trial eigenmode as a fixed superposition of the two waveguides' own mode profiles, with an overall propagation constant $\beta$ to be found.
2. Substitute into the wave equation to get a 2×2 eigenvalue problem for the expansion coefficients $C_a$, $C_b$.
3. Set the determinant to zero; for two identical waveguides this gives two eigenvalues $\beta_{1,2}=\beta_0\pm|\kappa|$ with symmetric/antisymmetric eigenvectors.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Coupled Mode Theory](Coupled%20Mode%20Theory.md), [Waveguide Array Supermodes](Waveguide%20Array%20Supermodes.md)
**Full Derivation:** [Coupled Waveguide Supermodes Derivation](Coupled%20Waveguide%20Supermodes%20Derivation.md)
