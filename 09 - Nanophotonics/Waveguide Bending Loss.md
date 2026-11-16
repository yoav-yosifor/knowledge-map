---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

When a waveguide is bent, the part of the mode on the outside of the curve has to travel a longer path in the same time as the core, so its phase velocity grows linearly with radius. Beyond some radius that velocity would have to exceed $c$ — which it cannot — so the outer tail of the field detaches from the mode and radiates away. A bent waveguide therefore has **no true bound mode**: it always leaks, and the leakage is intrinsic to the bend, independent of material absorption or surface scattering.

## Key Equation

$$
n_{eq}(u)=n(u)\,e^{u/R}
$$

**Derived From:** applying the conformal coordinate map $u=R\ln(\rho/R)$, $v=R\theta$ to the wave equation in cylindrical coordinates; in the new $(u,v)$ coordinates the equation is identical to a *straight* waveguide in Cartesian coordinates but with the index profile replaced by this equivalent index $n_{eq}$.

- $\rho,\theta$ — polar coordinates in the plane of the bend; $R$ — an arbitrary reference radius (the radius mapped to $u=0$)
- $u$ — transformed transverse coordinate; $\rho=0\to u=-\infty$ and $\rho\to\infty\to u=+\infty$, so $u$ spans $\pm\infty$
- $n(u)$ — the physical (step) index profile; $e^{u/R}$ — the exponential tilt the bend adds

## Supporting Formulas

- Wave equation in cylindrical coordinates: $$\frac{\partial^2E}{\partial\rho^2}+\frac{1}{\rho}\frac{\partial E}{\partial\rho}+\frac{1}{\rho^2}\frac{\partial^2E}{\partial\theta^2}+k_0^2\,n^2(\rho)\,E=0$$
- Transformed (straight-guide-like) wave equation: $$\frac{\partial^2E}{\partial u^2}+\frac{\partial^2E}{\partial v^2}+k_0^2\left[n(u)\,e^{u/R}\right]^2E=0$$
- Local phase velocity of the field grows with radius as $V(\rho)=V(R)\cdot\rho/R$; where it reaches $c$, phase fronts detach and radiate.
- Because $n_{eq}\to\infty$ as $u\to+\infty$, there is no formal guided mode; the mode profile shifts toward higher $n_{eq}$, i.e. toward the **outer** edge of the bend — an asymmetric profile whose radial tail never reaches zero.
- Bending loss cannot be eliminated but is reduced by **high index contrast** and **large bend radius**. Additional (non-intrinsic) loss channels: material absorption, and surface-roughness scattering — the latter worse than in a straight guide because the field piles up on the outer wall.

## Derivation Outline

1. Start from the scalar wave equation in cylindrical coordinates for the bend.
2. Apply the conformal map $u=R\ln(\rho/R)$, $v=R\theta$, which straightens the curved guide into a straight one in $(u,v)$.
3. The transformed equation looks Cartesian, but the index becomes $n_{eq}(u)=n(u)e^{u/R}$ — a step profile multiplied by an exponential ramp.
4. Read off the physics: the ramp destroys confinement at large $u$ (no bound mode), pushes the mode outward, and the point where the equivalent index can no longer support a guided ray marks the onset of radiation loss.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Leaky Waveguide Modes](Leaky%20Waveguide%20Modes.md), [Radiation Condition](Radiation%20Condition.md), [Ring Resonator](Ring%20Resonator.md), [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md)
**Full Derivation:** [Bent Waveguide Conformal Transformation](Bent%20Waveguide%20Conformal%20Transformation.md)
