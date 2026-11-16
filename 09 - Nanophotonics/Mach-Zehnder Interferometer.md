---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

Two directional couplers connected by two waveguide arms of different length interfere at the second coupler, redistributing the input power between two outputs according to the optical path difference between the arms — realized either in bulk optics (mirrors and beamsplitters) or as an integrated waveguide device.

## Key Equation

$$
|E_1|^2=1-4\kappa_p(1-\kappa_p)\cos^2\!\left(\frac{\beta\Delta L}{2}\right),\qquad |E_2|^2=4\kappa_p(1-\kappa_p)\cos^2\!\left(\frac{\beta\Delta L}{2}\right)
$$

**Derived From:** cascading two identical [directional couplers](Directional%20Coupler.md) (power-coupling ratio $\kappa_p$) through arms of length $L$ and $L+\Delta L$, then taking $|E|^2$ of the recombined output field amplitudes.

## Supporting Formulas

- **Power coupling ratio:** $\kappa_p=\sin^2(\kappa d)$ — the fraction of input power transferred to the cross port of each coupler; $\kappa_p=0.5$ is a symmetric "3 dB" coupler (50/50 split), $\kappa_p=0$ or $1$ passes all power straight through or fully across —
- **Output field amplitudes**, input into one arm only: $E_1=e^{-i\beta L}(1-\kappa_p)\left(1+e^{-i\beta\Delta L}\right)$, $E_2=-i\sqrt{\kappa_p(1-\kappa_p)}\,e^{-i\beta\left(L+\frac{\Delta L}{2}\right)}\cdot2\cos\!\left(\frac{\beta\Delta L}{2}\right)$ —
- **General 2-port coupler matrix:** $\bar E_{out}=\begin{pmatrix}\sqrt{1-\kappa_p}&-i\sqrt{\kappa_p}\\-i\sqrt{\kappa_p}&\sqrt{1-\kappa_p}\end{pmatrix}\bar E_{in}$ (convention: positive propagation $\propto e^{-i\beta z}$; the imaginary-part signs flip if $e^{i\beta z}$ is used instead) —
- **Power conservation:** $|E_1|^2+|E_2|^2=1$ —
- Full power transfer (output oscillating all the way between 0 and 1 as $\lambda$ or $\Delta L$ is swept) occurs only for a symmetric coupler, $\kappa_p=0.5$; for $\kappa_p\neq0.5$ the modulation depth shrinks and residual power stays trapped in one output at every wavelength —

## Derivation Outline

1. Input excites one arm of the first directional coupler; the coupler matrix splits it into amplitudes $\sqrt{1-\kappa_p}$ and $-i\sqrt{\kappa_p}$ in the two arms.
2. Each arm accumulates its own propagation phase over its own length ($L$ vs. $L+\Delta L$).
3. The second coupler recombines the two arms; taking $|E|^2$ of each output gives the interference pattern as a function of $\Delta\phi=\beta\Delta L/2$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Directional Coupler](Directional%20Coupler.md)
**Full Derivation:** 
