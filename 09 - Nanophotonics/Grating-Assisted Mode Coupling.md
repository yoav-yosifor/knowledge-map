---
tags:
  - nanophotonics
  - concept
  - technique
---
---
## Core Idea

A small perturbation of a waveguide's dielectric profile couples its guided modes to each other, but only efficiently if the perturbation contains a spatial Fourier component that makes up the propagation-constant difference between the modes (phase matching, equivalently momentum conservation with the lattice momentum).

## Key Equation

$$
\frac{dA_s^{(+)}}{dz}=\kappa^*A_m^{(+)}(z)e^{i2\Delta\beta z},\qquad
\frac{dA_m^{(+)}}{dz}=\kappa A_s^{(+)}(z)e^{-i2\Delta\beta z}
$$

**Derived From:** starting with the wave equation for the perturbed structure, expanding the field in the unperturbed guided modes with slowly varying amplitudes (SVEA), projecting onto a single mode using orthogonality, and keeping only the Fourier component of the periodic perturbation that is phase-matched — see [Grating-Assisted Coupling Derivation](Grating-Assisted%20Coupling%20Derivation.md).

- $A_m, A_s$ — slowly varying amplitudes of modes $m$ and $s$
- $\kappa=\tfrac14 i\omega\varepsilon_0\displaystyle\int\overline{\Delta\varepsilon_r}(x)\,a_q\,E_m(x)E_s(x)\,dx$ — coupling coefficient (overlap of the two mode profiles weighted by the $q$-th Fourier amplitude of the perturbation)
- $\Delta\beta=\tfrac12(\beta_s-\beta_m)-\dfrac{\pi}{\Lambda}q$ — phase mismatch; assumed $\Delta\beta\ll\beta_s,\beta_m$

## Supporting Formulas

- Perturbed permittivity: $\varepsilon_r'(\mathbf r)=\varepsilon_r(\mathbf r)+\Delta\varepsilon_r(\mathbf r)$, $\Delta\varepsilon_r\ll\varepsilon_r$ —
- Perturbed wave equation: $\nabla^2E+k_0^2\varepsilon_r E=-k_0^2\Delta\varepsilon_r E$ — the perturbation acts as a source term
- Modal expansion: $E=\sum_m A_m(z)E_m(x)\exp(-i\beta_m z)$ —
- SVEA: $\left|\dfrac{d^2A_m}{dz^2}\right|\ll\left|2\beta_m\dfrac{dA_m}{dz}\right|$ —
- Mode orthogonality: $\displaystyle\int_{-\infty}^{\infty}E_m(x)E_s(x)\,dx=\dfrac{2\omega\mu}{\beta_s}\delta_{ms}$ —
- 1D periodic perturbation: $\Delta\varepsilon_r(x,z)=\overline{\Delta\varepsilon_r}(x)\displaystyle\sum_{q=-\infty}^{\infty}a_q e^{-i\frac{2\pi}{\Lambda}qz}$ —
- Phase-matching condition: the perturbation must contain a Fourier component $e^{i\beta z}$ such that $e^{i(\beta_m\mp\beta)}=e^{\mp i\beta_s}$ —
- Momentum-conservation form: a photon in mode $m$ ($\hbar\beta_m$) scattered by the lattice ($\pm\hbar\beta$) must land on an allowed state, $\hbar(\beta_m\mp\beta)=\hbar\beta_s$ —
- For the $q$-th component: $-\beta_s\approx-\dfrac{2\pi}{\Lambda}q-\beta_m$; for positive $q$, $q$ quanta of lattice momentum are added, so $a_q$ couples modes $m$ and $s$ propagating in the same direction
- Special case $\beta_s=-\beta_m$ couples $A_s^{(+)}$ and $A_s^{(-)}$ (counter-propagating), with $\Delta\beta=\beta_s-\dfrac{\pi}{\Lambda}q$ — see [Waveguide Bragg Grating](Waveguide%20Bragg%20Grating.md)

## Derivation Outline

1. Treat the structure as the unperturbed waveguide plus a small $\Delta\varepsilon_r$, and write the field as a superposition of guided modes with slowly varying amplitudes.
2. Substitute into the wave equation, cancel the unperturbed-mode terms, drop second derivatives of the amplitudes (SVEA), and project onto mode $s$ using orthogonality.
3. The right-hand side is a "source" that drives $A_s$; it is effective only if its $z$-dependence matches that of the driven term (phase matching). Average out all non-matched terms and keep the matched Fourier component $q$ to obtain the rate equations.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Coupled Mode Theory](Coupled%20Mode%20Theory.md), [Grating Coupling](Grating%20Coupling.md), [Waveguide Coupling Condition](Waveguide%20Coupling%20Condition.md), [Reciprocal Lattice](Reciprocal%20Lattice.md), [Waveguide Bragg Grating](Waveguide%20Bragg%20Grating.md)
**Full Derivation:** [Grating-Assisted Coupling Derivation](Grating-Assisted%20Coupling%20Derivation.md)
