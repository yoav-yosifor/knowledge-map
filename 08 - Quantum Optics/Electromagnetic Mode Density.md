---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Counting how many electromagnetic standing-wave modes fit inside a cavity, per unit frequency, gives a density of states that grows as $\omega^2$. Left unmodified, that geometric fact is exactly what makes classical physics predict infinite radiated power from a hot object.

## Key Equation

$$
g(\omega) = \frac{\omega^2}{\pi^2 c^3}
$$

**Derived From:** a cubic cavity of side $L$ with periodic boundary conditions, so allowed wavevectors form a lattice $\mathbf k = \tfrac{2\pi}{L}(n_1,n_2,n_3)$ with $n_i\in\mathbb Z$; counting lattice points in a thin spherical shell of $k$-space (using $\omega=c|\mathbf k|$) and including a factor of 2 for the two polarizations per mode.

## Supporting Formulas

- Mode counting integral: $g(\omega)\,d\omega = 2\cdot\frac{1}{L^3}\cdot\left(\frac{L}{2\pi}\right)^3\cdot4\pi k^2\,dk$
- Combined with quantized mode energy and Bose–Einstein statistics, this feeds directly into Planck's law — see [Planck's Law](Plancks%20Law.md)

## Derivation Outline

1. Impose periodic boundary conditions on a cubic cavity of side $L$, which restricts allowed wavevectors to a discrete lattice with spacing $2\pi/L$ in each direction.
2. Count how many lattice points (modes) fall inside a thin spherical shell of radius $k$ and thickness $dk$ in $k$-space, using the mode density per unit $k$-space volume, $(L/2\pi)^3$.
3. Convert from $k$ to $\omega$ via the vacuum dispersion relation $\omega=ck$, and double the count to include both polarizations, giving the number of modes per unit volume per unit frequency.

## Physical Intuition

A cavity can only support standing electromagnetic waves that fit its boundaries exactly, the same way a guitar string can only vibrate at specific resonant wavelengths. As you look at higher and higher frequencies, there are simply more and more ways to fit a shorter wavelength inside the same box — the number of available "slots" grows without bound as $\omega^2$. If classical physics is naively allowed to assign the same average thermal energy to every one of these slots regardless of frequency, then a diverging number of high-frequency slots each carrying a fixed chunk of energy adds up to infinite total energy — the ultraviolet catastrophe. Quantum mechanics fixes this not by changing how many slots exist, but by changing how much energy, on average, ends up in each one: high-frequency slots become exponentially unlikely to be occupied at all.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Planck's Law](Plancks%20Law.md), [Einstein Coefficients](Einstein%20Coefficients.md)
**Full Derivation:**
