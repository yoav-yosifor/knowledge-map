---
tags:
  - nanophotonics
  - system
  - device
---
---
## Overview

Two waveguides brought into close proximity so their evanescent fields overlap and exchange power along the propagation direction $z$ — the integrated-optics equivalent of a beam-splitter, used for power splitting/combining and for coupling light into other devices and waveguides. The source material notes this power exchange is "similar to resonant tunneling in QM."

## Prerequisite Concepts

- [Coupled Mode Theory](Coupled%20Mode%20Theory.md) — the coupling coefficient $\kappa$ and phase-mismatch $\delta$ that govern the power exchange come directly from CMT.

## Regimes and Parameters

- Solving the coupled-mode equations with the input condition $A(0)=A_0$, $B(0)=0$ gives $A(L)=A_0e^{i\delta L}\left[\cos(SL)-i\frac{\delta}{S}\sin(SL)\right]$, $B(L)=-iA_0e^{-i\delta L}\frac{\kappa}{S}\sin(SL)$, with $S=\sqrt{|\kappa|^2+\delta^2}$.
- Power flow: $P_b(L)=P_0\dfrac{|\kappa|^2}{S^2}\sin^2(SL)$, $P_a(L)=P_0-P_b(L)$.
- The power transfer is periodic in the propagation length $L$ (coupling length).
- Maximal transfer at any given $L$ is $P_0|\kappa|^2/S^2$; **complete** power transfer to the other waveguide requires phase matching, $\delta=0$.
- Two **identical** waveguides ($\beta_a=\beta_b$, $M_{aa}=M_{bb}$) give $\delta=0$ automatically, so a coupler built from two identical guides always reaches complete power transfer periodically, at $L$ such that $\kappa L=\pi/2, 3\pi/2,\dots$
- **Power-coupling parametrization** (phase-matched, $\delta=0$ case): defining the **power coupling ratio** $\kappa_p=\sin^2(\kappa d)$ for a coupler of length $d$, the phase-matched solution above becomes $A(d)=\sqrt{1-\kappa_p}\,A_0$, $B(d)=-i\sqrt{\kappa_p}\,A_0$ — a $90°$ phase shift between the through and cross-coupled amplitudes.
- **General 2-port matrix form:** as a linear device, an arbitrary two-input excitation of a coupler with power-coupling ratio $\kappa_p$ gives $\bar E_{out}=\begin{pmatrix}\sqrt{1-\kappa_p}&-i\sqrt{\kappa_p}\\-i\sqrt{\kappa_p}&\sqrt{1-\kappa_p}\end{pmatrix}\bar E_{in}$ (convention: positive propagation $\propto e^{-i\beta z}$; the imaginary-part signs flip if $e^{i\beta z}$ is used instead). Used to cascade couplers, e.g. in a [Mach-Zehnder Interferometer](Mach-Zehnder%20Interferometer.md).

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Coupled Waveguide Supermodes](Coupled%20Waveguide%20Supermodes.md)
**Concepts Used:** [Coupled Mode Theory](Coupled%20Mode%20Theory.md)
