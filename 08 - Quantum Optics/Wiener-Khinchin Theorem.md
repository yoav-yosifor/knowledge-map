---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

For a stationary random field, the power spectral density is the Fourier transform of the field's own [autocorrelation function](First-Order%20Coherence%20Function.md). This means a spectrometer and an interferometer are, in principle, measuring exactly the same physical information.

## Key Equation

$$
S(\omega) = \frac{1}{2\pi}\int_{-\infty}^{\infty} g^{(1)}(\tau)\,e^{i\omega\tau}\,d\tau = |E(\omega)|^2
$$

**Derived From:** Fourier-transforming the time-domain autocorrelation function $G^{(1)}(\tau)=\lim_{T\to\infty}\frac1T\int_{-T/2}^{T/2}E(t)E^*(t+\tau)\,dt$ of a stationary, ergodic field, valid because for such fields time averages equal ensemble averages.

## Supporting Formulas

- $\tau_c = \dfrac{\pi}{\delta\omega}$ — coherence time from the half-width $\delta\omega$ of the spectrum
- $G^{(1)}(\tau) = \lim_{T\to\infty}\frac{1}{T}\int_{-T/2}^{T/2}E(t)E^*(t+\tau)\,dt$ — the ergodic (time-average) form of the autocorrelation, equal to the ensemble-average form for stationary ergodic light

## Derivation Outline

1. Assume the field is stationary (statistics depend only on the time difference $\tau$) and ergodic (time averages equal ensemble averages).
2. Write the field autocorrelation as a long-time average, $G^{(1)}(\tau)$.
3. Fourier transform in $\tau$ to obtain the power spectral density $S(\omega)$.

## Physical Intuition

This theorem is the bridge between two completely different-looking experiments. A spectrometer sorts light by frequency and tells you its spectral shape directly. An interferometer instead delays a copy of the light and watches how well it still interferes with itself as the delay grows. The Wiener-Khinchin theorem says these two pictures are Fourier transforms of each other: a light source with a narrow spectral line keeps its phase memory for a long time (long coherence time), while a source with a broad, smeared-out spectrum forgets its phase almost immediately. Either measurement — spectral width or coherence-time decay — tells you the same thing about the underlying randomness of the source.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [First-Order Coherence Function](First-Order%20Coherence%20Function.md)
**Full Derivation:**
