---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A wide, high-index-contrast multimode slab waveguide (a Multi-Mode Interference, "MMI", device) exploits self-imaging — the Talbot effect: an input beam excites many of the waveguide's guided modes at once, and their interference while co-propagating periodically reproduces images of the input field profile, including translated, multiplied, and mirror-reflected copies.

## Key Equation

$$
\psi\!\left(y,\tfrac{p}{2}3L_\pi\right)=\frac{1+i^p}{2}\,\psi(y,0)+\frac{1-i^p}{2}\,\psi(-y,0),\qquad p=1,3,5,\dots
$$

**Derived From:** decomposing the input field into the MMI's guided modes, propagating each mode with its own phase $\beta_\nu$, and using the fact that every mode-pair's propagation-constant spacing is an integer multiple of the same beat length $L_\pi$ — full steps in [MMI Self-Imaging Derivation](MMI%20Self-Imaging%20Derivation.md).

## Supporting Formulas

- **Guided-mode dispersion relation:** $k_{y\nu}^2+\beta_\nu^2=k_0^2n_f^2$, $k_0=\omega/c$, $k_{y\nu}=(\nu+1)\pi/w_{eq}$, $\nu=0,\dots,m-1$, for a device of width $w_m$, core index $n_f$, cladding index $n_c$ —
- **Effective width** $w_{eq}$ (device width plus the [Goos-Hänschen](Goos-Hänschen%20Shift.md) penetration depth), approximated using the fundamental mode: $w_{eq}\approx w_m+\dfrac{\lambda_0}{\pi}\left(n_f^2-n_c^2\right)^{-1/2}$ (TE), $w_{eq}\approx w_m+\dfrac{\lambda_0}{\pi}\left(\dfrac{n_c}{n_f}\right)^2\left(n_f^2-n_c^2\right)^{-1/2}$ (TM) — often assumed the same for every mode, $w_{eq,0}=w_{eq,\nu}$ —
- **Beat length** between the first two modes: $L_\pi=\dfrac{\pi}{\beta_0-\beta_1}\approx\dfrac{4n_fw_{eq}^2}{3\lambda_0}$ —
- **Single-image condition:** $L=p\cdot3L_\pi$, $p=1,2,\dots$ — perfect image of the input for even $p$, mirror image for odd $p$ —

## Derivation Outline

1. Find the guided-mode dispersion relation and effective width $w_{eq}$ of the wide multimode waveguide.
2. Get the paraxial propagation constant $\beta_\nu$ of each mode, and show every mode-pair spacing is an integer multiple of one beat length $L_\pi$.
3. Decompose the input field into guided modes and propagate each to distance $L$.
4. Find the phase condition for the propagated sum to reproduce, mirror, or multiply the input — full steps: [MMI Self-Imaging Derivation](MMI%20Self-Imaging%20Derivation.md).

## Physical Intuition

The beat length is defined from just the closest pair of modes — the fundamental and the first excited one — but it ends up governing the spacing between every mode in the waveguide, not only that pair. That's because each mode's propagation constant depends on the mode number only through a single square term, so the "distance" between any two modes' propagation constants is always a whole-number multiple of the same basic step, and the beat length measures that one basic step. This is why every imaging distance in this device — the perfect image, the mirror image, the power-splitter positions — comes out as a simple multiple of the beat length: there's only one length scale in the problem, so everything the interference produces has to happen at multiples of it. Compared to a directional coupler, an MMI is shorter and supports broader bandwidth.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md), [Goos-Hänschen Shift](Goos-Hänschen%20Shift.md)
**Full Derivation:** [MMI Self-Imaging Derivation](MMI%20Self-Imaging%20Derivation.md)
