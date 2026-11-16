---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A waveguide with a periodic perturbation of period $\Lambda$ couples the forward and backward propagating waves; near the Bragg wavelength the coupling opens a band of frequencies (the optical bandgap or stop-band) in which no wave propagates and light is reflected, making the structure a spectrally selective mirror (the basis of photonic crystals).

## Key Equation

$$
\Lambda=\frac{q\lambda_0}{2n_{eff}}
$$

**Derived From:** starting with the counter-propagating coupled-mode equations, finding the exponential/propagating solutions $e^{\gamma z}$ with $\gamma=i\Delta\beta\pm\sqrt{|\kappa|^2-\Delta\beta^2}$, and setting the band centre at $\Delta\beta=0$, i.e. $\beta_0=\frac{n_{eff}}{c}\omega_0=\frac{\pi q}{\Lambda}$ — see [Bragg Grating Solution Derivation](Bragg%20Grating%20Solution%20Derivation.md).

For $q=1$ this is the famous $\lambda/2$ periodicity.

## Supporting Formulas

- Definitions: $A\equiv A_s^{(+)}$, $B\equiv A_s^{(-)}$, $\beta\equiv\beta_s$, $\Delta\beta=\beta_s-\dfrac{\pi}{\Lambda}q$ —
- Coupled equations: $\dfrac{dA}{dz}=\kappa^*Be^{i2\Delta\beta z}$, $\dfrac{dB}{dz}=\kappa Ae^{-i2\Delta\beta z}$ —
- Second-order equation: $A_{zz}-2i\Delta\beta A_z-|\kappa|^2A=0$, so $A\propto\exp(\gamma z)$ —
- Eigenvalues: $\gamma=i\Delta\beta\pm\sqrt{|\kappa|^2-\Delta\beta^2}=\pm S+i\Delta\beta$ —
- Regimes: $|\kappa|<|\Delta\beta|$ → $S$ imaginary, propagating solutions; $|\kappa|>|\Delta\beta|$ (better phase matching) → $S$ real, exponentially decaying/growing solutions; for $-\kappa<\Delta\beta<\kappa$ there are no propagating waves — the **optical bandgap**, in analogy with the forbidden gap in semiconductor physics
- Bandgap condition (assuming $\beta(\omega)=n_{eff}\omega/c$, $n_{eff}$ frequency independent): $|\Delta\beta|=|\beta-\beta_0|<\kappa$, i.e. $\dfrac{n_{eff}}{c}|\omega-\omega_0|<|\kappa|$ —
- Bandgap width: $\Delta\omega_{BG}=\dfrac{2|\kappa|c}{n_{eff}}$ —
- Band centre: $\beta_0=\dfrac{n_{eff}}{c}\omega_0=\dfrac{\pi q}{\Lambda}\Rightarrow\omega_0=\dfrac{\pi q}{\Lambda}\dfrac{c}{n_{eff}}=\dfrac{2\pi c}{\lambda_0}$ —
- Reflection coefficient (with $A(0)=1$, $B(L)=0$): $r=\dfrac{B(0)}{A(0)}=\dfrac{\kappa\sinh(SL)}{S\cosh(SL)+i\Delta\beta\sinh(SL)}$ —
- At $\Delta\beta=0$, $S=|\kappa|$ and the reflectivity is $|r|=\tanh(|\kappa|L)$ —
- Band structure: forward/backward waves have propagation coefficient $\beta'=\beta_0\mp iS$, so $\beta'-\beta_0=\mp i\dfrac{n_{eff}}{c}\sqrt{\omega_\kappa^2-(\omega-\omega_0)^2}$ with $\omega_\kappa=\dfrac{c}{n_{eff}}|\kappa|$ —
- Inside the gap: $\mathrm{Re}(\beta')=\beta_0$, $\mathrm{Im}(\beta')=\dfrac{n_{eff}}{c}\sqrt{\omega_\kappa^2-(\omega-\omega_0)^2}$; outside: $\mathrm{Re}(\beta')=\beta_0\pm\dfrac{n_{eff}}{c}\sqrt{(\omega-\omega_0)^2-\omega_\kappa^2}$, $\mathrm{Im}(\beta')=0$ — inside the gap the phase accumulates according to $\beta_0$; outside, the propagation coefficient is modified
- Example ($A(0)=1$, $B(L)=0$, $\kappa L=1$, $\Delta\beta=0$): $|A|^2$ falls from 1 to about 0.42 at $z=L$, $|B|^2$ falls from about 0.58 to 0 (values read from the lecture plot)

## Derivation Outline

1. Specialise the grating-assisted coupling equations to $\beta_s=-\beta_m$, which couples the forward wave $A$ to the backward wave $B$.
2. Substitute the two first-order equations into each other to get a second-order equation for $A$, and solve with $A\propto e^{\gamma z}$.
3. Fix the constants by the boundary conditions $A(0)=1$, $B(L)=0$ to get $A(z)$, $B(z)$, hence $r$ and the stop-band.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Grating-Assisted Mode Coupling](Grating-Assisted%20Mode%20Coupling.md), [Distributed Bragg Reflector](Distributed%20Bragg%20Reflector.md), [Bloch Theorem](Bloch%20Theorem.md), [Reciprocal Lattice](Reciprocal%20Lattice.md)
**Full Derivation:** [Bragg Grating Solution Derivation](Bragg%20Grating%20Solution%20Derivation.md)
