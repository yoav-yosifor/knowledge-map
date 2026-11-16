---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A ring resonator supports a comb of resonances — every frequency whose round-trip phase is an integer multiple of $2\pi$. The **free spectral range** is the frequency spacing between two neighbouring resonances. Because a full extra wavelength must be fit into the loop as the frequency steps from one resonance to the next, the relevant "how much does phase build per unit frequency" quantity is the group index, not the phase index — so the FSR is set by $n_g$, not $n_{eff}$.

## Key Equation

$$
\Delta\omega_{FSR}=\frac{2\pi c}{L\,n_g},\qquad
\Delta\nu_{FSR}=\frac{\Delta\omega_{FSR}}{2\pi}=\frac{c}{L\,n_g}=\frac{1}{\tau_{RT}}
$$

**Derived From:** starting with the ring resonance condition $\dfrac{\omega_m}{c}n_{eff}(\omega)L=2\pi m$, writing the same condition for resonance $m+1$ at $\omega_m+\Delta\omega_{FSR}$ with $n_{eff}$ linearized in $\Delta\omega$, subtracting, and keeping only first order in $\Delta\omega_{FSR}$.

- $L$ — round-trip (circumference) length of the ring
- $n_g=n_{eff}+\omega\,dn_{eff}/d\omega$ — group index (see [Structural Dispersion and Group Index](Structural%20Dispersion%20and%20Group%20Index.md))
- $\tau_{RT}=L/(c/n_g)=1/\Delta\nu_{FSR}$ — round-trip time; the FSR is its inverse

## Supporting Formulas

- Resonance condition: $$\frac{\omega_m}{c}\,n_{eff}(\omega_m)\,L=2\pi m$$ — round-trip phase is a multiple of $2\pi$
- Near-resonance round-trip phase (used throughout the ring analysis): $$\varphi=\frac{L}{c}\,n_g\,\Delta\omega=\frac{\Delta\omega}{\Delta\nu_{FSR}}\pmod{2\pi}$$
- If structural dispersion is neglected ($n_g\to n_{eff}$) the FSR reduces to the naive $2\pi c/(L\,n_{eff})$; in HIC rings this overestimates the FSR by 25–30%.

## Derivation Outline

1. Write the resonance condition at $\omega_m$ (integer $m$) and at $\omega_m+\Delta\omega_{FSR}$ (integer $m+1$).
2. In the second, linearize $n_{eff}(\omega)\approx n_{eff}(\omega_m)+\dfrac{dn_{eff}}{d\omega}\Delta\omega_{FSR}$.
3. Expand the product $(\omega_m+\Delta\omega_{FSR})\,n_{eff}(\omega_m+\Delta\omega_{FSR})$ and subtract the $\omega_m$ equation.
4. Drop the $\Delta\omega_{FSR}^2$ term; the surviving bracket is $n_{eff}+\omega_m\,dn_{eff}/d\omega=n_g$, leaving $\dfrac{L}{c}n_g\,\Delta\omega_{FSR}=2\pi$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Structural Dispersion and Group Index](Structural%20Dispersion%20and%20Group%20Index.md), [Ring Resonator](Ring%20Resonator.md), [Cavity Q Factor and Finesse](Cavity%20Q%20Factor%20and%20Finesse.md)
**Full Derivation:** [Free Spectral Range Derivation](Free%20Spectral%20Range%20Derivation.md)
