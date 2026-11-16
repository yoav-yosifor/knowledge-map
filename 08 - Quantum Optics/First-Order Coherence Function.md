---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The first-order coherence function $G^{(1)}(\tau)$ measures how well a fluctuating light field correlates with a time-delayed copy of itself. Its normalized modulus sets the visibility of the interference fringes that copy can produce.

## Key Equation

$$
g^{(1)}(\tau) = \frac{G^{(1)}(\tau)}{I_0} = \frac{\langle E^*(0)\,E(\tau)\rangle}{\langle E^*(0)\,E(0)\rangle}
$$

**Derived From:** splitting a field into two paths of a Mach-Zehnder interferometer with relative delay $\tau$, recombining them, and identifying the $\tau$-dependent cross term in the ensemble-averaged output intensity as $G^{(1)}(\tau)=\langle E^*(t)E(t+\tau)\rangle$; normalizing by the mean intensity $I_0$ gives the dimensionless degree of coherence.

## Supporting Formulas

- $\langle I_\text{out}\rangle = I_0\bigl[1+|g^{(1)}(\tau)|\cos(\omega\tau-\phi(\tau))\bigr]$ — interferometer output intensity
- $V = \dfrac{I_\text{max}-I_\text{min}}{I_\text{max}+I_\text{min}} = |g^{(1)}(\tau)|$ — fringe visibility equals the modulus of the degree of coherence
- $g^{(1)}(0)=1$; for stationary light $g^{(1)}(\tau)=[g^{(1)}(-\tau)]^*$
- $\tau_c = \pi/\delta\omega$ — coherence time from spectral linewidth, via the [Wiener-Khinchin Theorem](Wiener-Khinchin%20Theorem.md)
- Monochromatic field with independent random phases: $g^{(1)}(\tau)=e^{-i\omega_0\tau}$, $|g^{(1)}|=1$ for all $\tau$ — perfect coherence despite the randomness, because every mode shares the same frequency
- Collision-broadened field: $g^{(1)}(\tau)=e^{-i\omega_0\tau}e^{-\gamma|\tau|}$ — Lorentzian power spectrum
- Doppler-broadened field: $g^{(1)}(\tau)=e^{-i\omega_0\tau}e^{-\frac12\Delta^2\tau^2}$ — Gaussian power spectrum
- Balanced homodyne readout: $\langle I_1-I_2\rangle \propto \text{Re}\,\langle E(t)E^*(t+\tau)\rangle$ isolates the real part of $G^{(1)}$ directly — see [Homodyne Detection](Homodyne%20Detection.md)

## Derivation Outline

1. Split the field into two interferometer arms with a relative delay $\tau$ and recombine them at a detector.
2. Average the output intensity over the field's random statistics, assuming stationarity (statistics depend only on $\tau$).
3. Identify the interference cross term as $G^{(1)}(\tau)=\langle E^*(t)E(t+\tau)\rangle$ and normalize by $I_0$ to get $g^{(1)}(\tau)$.

## Physical Intuition

Real light is never a perfect, endless sine wave — its amplitude and phase wander randomly. Two copies of such a field can only interfere cleanly if the copies are still "in step" with each other, and $g^{(1)}(\tau)$ is just a number that says how in-step a field is with a delayed version of itself. If the delay is short compared to how fast the field's phase wanders, the two copies still line up and you get sharp fringes; if the delay is long, the phase has scrambled and the fringes wash out. The coherence time $\tau_c$ is simply the delay at which this washing-out happens, and it is tied by Fourier transform to how spectrally pure the light is — a narrower range of frequencies means a longer memory of its own phase.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md), [Wiener-Khinchin Theorem](Wiener-Khinchin%20Theorem.md), [Homodyne Detection](Homodyne%20Detection.md)
**Full Derivation:**
