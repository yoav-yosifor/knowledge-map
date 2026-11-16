---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

In a high-index-contrast (HIC) waveguide the field is squeezed so tightly into the core that the effective index $n_{eff}$ depends strongly on wavelength *purely from the geometry* — even when every material in the structure is perfectly non-dispersive. This geometric wavelength dependence is called **structural dispersion**, and it is what makes the group index $n_g$ (which governs how fast a pulse or its energy travels) differ substantially — by 25–30% in HIC guides — from the phase index $n_{eff}$.

## Key Equation

$$
n_g=n_{eff}+\omega\,\frac{dn_{eff}}{d\omega}
$$

**Derived From:** starting with the phase-index definition $c\,k=\omega\,n_{eff}$, differentiating both sides with respect to $\omega$, and identifying $c\,\dfrac{dk}{d\omega}=\dfrac{c}{V_g}=n_g$.

- $n_{eff}=n_{ph}$ — phase index; sets the phase velocity $V_{ph}=\omega/k=c/n_{eff}$
- $n_g$ — group index; sets the group velocity $V_g=d\omega/dk=c/n_g$
- $\dfrac{dn_{eff}}{d\omega}$ — the structural-dispersion slope; nonzero even for non-dispersive materials because the mode's confinement (and hence $n_{eff}$) changes with $\omega$

## Supporting Formulas

- $$V_{ph}=\dfrac{\omega}{k}=\dfrac{c}{n_{ph}}$$ — phase velocity
- $$V_{g}=\dfrac{d\omega}{dk}=\dfrac{c}{n_{g}}$$ — group velocity
- Worked example from the source (buried-ridge guide, core $n=2.035$ of $1.0\ \mu\text{m}\times0.34\ \mu\text{m}$, cladding $n=1.48$, substrate $n=1.45$): $n_{eff}\approx1.644$, $\dfrac{\partial n_{eff}}{\partial\omega}=3.0228\times10^{-4}$ (per THz), giving $n_g=n_{eff}+\omega\dfrac{\partial n_{eff}}{\partial\omega}=2.0106$ — about 22% above $n_{eff}$.

## Derivation Outline

1. Write the phase-index relation $c\,k=\omega\,n_{eff}(\omega)$.
2. Differentiate with respect to $\omega$: $c\,\dfrac{dk}{d\omega}=n_{eff}+\omega\,\dfrac{dn_{eff}}{d\omega}$.
3. Recognize the left side as $c/V_g=n_g$, giving $n_g=n_{eff}+\omega\,dn_{eff}/d\omega$.
4. Note that in a HIC waveguide $dn_{eff}/d\omega$ is large from geometry alone, so $n_g$ departs strongly from $n_{eff}$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Free Spectral Range](Free%20Spectral%20Range.md), [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md), [Leaky Waveguide Modes](Leaky%20Waveguide%20Modes.md)
**Full Derivation:**
