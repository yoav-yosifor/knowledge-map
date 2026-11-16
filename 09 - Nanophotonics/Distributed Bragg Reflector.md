---
tags:
  - nanophotonics
  - system
  - device
---
---
## Overview

A DBR is a 1D periodic stack whose unit cell is two dielectric layers ($n_1,d_1$ and $n_2,d_2$); it reflects over a range of incidence angles for a given wavelength, and is analysed with a transfer matrix per unit cell.

## Prerequisite Concepts

- [Bloch Theorem](Bloch%20Theorem.md) — a periodic stack supports Bloch waves; crossing one cell gives phase $e^{-iK\Lambda}$
- [Multilayer Waveguide Transfer Matrix](Multilayer%20Waveguide%20Transfer%20Matrix.md) — same transfer-matrix method for a stack of layers
- [Reciprocal Lattice](Reciprocal%20Lattice.md) — 1D reciprocal lattice $G_n=\tfrac{2\pi}{\Lambda}n$ for the period $\Lambda=d_1+d_2$

Full matrix analysis: [DBR Transfer Matrix Derivation](DBR%20Transfer%20Matrix%20Derivation.md).

## Regimes and Parameters

- **Number of layers $N$:** more layers → stronger reflection.
- **Index contrast $n_1$ vs $n_2$:** larger contrast → broader range of reflected angles (the contrast defines the range of reflected angles). The same considerations hold for the dependence on wavelength.
- **Layer indices and thicknesses:** changing them modifies the range of angles.
- **Bragg condition:** reflection is obtained for $d_1+d_2\sim\tfrac12\lambda/\cos\theta$. The wavelength inside the structure therefore sets the centre angle — a different wavelength in the structure shifts the centre angle of the reflected range (incidence angle ↔ reflection band relation).
- **Lecture example (TE):** $\lambda=1.5\,\mu$m, $n_1=1.49$, $n_2=1.51$, $d_1=d_2=0.25\,\mu$m, $N=90$. Reflection $|r|^2$ rises to a plateau of about 0.7 (read from the plot) for incidence angles within roughly $\pm 8^\circ$ of normal, and is near zero outside it; transmission is the complement.

*The first two bullets and the wavelength/centre-angle point are the user's own notes added at capture, consistent with the lecture's "DBR properties" slide.*

## Physical Intuition


## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [DBR Transfer Matrix Derivation](DBR%20Transfer%20Matrix%20Derivation.md)
**Concepts Used:** [Bloch Theorem](Bloch%20Theorem.md), [Multilayer Waveguide Transfer Matrix](Multilayer%20Waveguide%20Transfer%20Matrix.md)
