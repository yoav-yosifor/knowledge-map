---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

An array of $N$ identical, evenly-spaced waveguides with nearest-neighbor coupling supports $N$ discrete eigenmodes ("supermodes"), generalizing the two-waveguide symmetric/antisymmetric case to $N$ guides — directly analogous to the tight-binding model in solid-state physics.

## Key Equation

$$
\Delta_m=2\kappa\cos\!\left(\frac{m\pi}{N+1}\right),\qquad m=1,2,\dots,N
$$

**Derived From:** starting with the nearest-neighbor coupled-mode difference equation for the array, applying a plane-wave trial solution and the boundary condition that the field vanishes outside the array.

- $\kappa$ — coupling coefficient between adjacent waveguides, same role as in [Coupled Mode Theory](Coupled%20Mode%20Theory.md)
- $N$ — number of waveguides in the array; the array supports exactly $N$ discrete supermodes
- $m$ — mode index, $m=1,\dots,N$, labeling each discrete supermode
- $\Delta_m$ — the shift of the $m$-th supermode's propagation constant away from the single-waveguide value $\beta_0$

Setting $N=2$ recovers the two-waveguide result: $\Delta_{1,2}=2\kappa\cos(\pi/3),\,2\kappa\cos(2\pi/3)=\pm\kappa$, exactly $\beta_{1,2}=\beta_0\pm|\kappa|$ from [Coupled Waveguide Supermodes](Coupled%20Waveguide%20Supermodes.md).

## Supporting Formulas

- Nearest-neighbor coupled equations: $\dfrac{\partial\varepsilon_n}{\partial z}=-i\kappa\varepsilon_{n-1}-i\kappa\varepsilon_{n+1}$, $n=1,\dots,N$, with boundary condition $\varepsilon_0=\varepsilon_{N+1}=0$ —
- Unquantized dispersion relation: $\Delta=2\kappa\cos(S)$, valid for $-2\kappa<\Delta<2\kappa$ before the boundary condition is imposed —
- Mode profile: $C_n^S=\sin(Sn)$, $S=m\pi/(N+1)$ —

## Derivation Outline

1. Model the array with only nearest-neighbor coupling between identical waveguides, giving a set of coupled difference equations for each guide's amplitude.
2. Try a plane-wave solution along the array index $n$; this gives an (unquantized) dispersion relation between the propagation-constant detuning $\Delta$ and the trial wavenumber $S$.
3. Impose the boundary condition that the field must vanish just outside the first and last waveguide; this quantizes $S$ (and hence $\Delta$) into $N$ discrete values.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Coupled Waveguide Supermodes](Coupled%20Waveguide%20Supermodes.md), [Coupled Mode Theory](Coupled%20Mode%20Theory.md)
**Full Derivation:** [Waveguide Array Supermodes Derivation](Waveguide%20Array%20Supermodes%20Derivation.md)
