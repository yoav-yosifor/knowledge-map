---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

A single photon need not live in one field mode. It can instead be a coherent superposition spread across many modes, described by a collective creation operator. This multimode superposition is exactly what allows a "particle" of light to be localized in space and time, with its spectral width fixed by the inverse of its temporal duration.

## Key Equation

$$
|1(t)\rangle = \sum_i c_i\,\hat a_i^\dagger\,e^{-i\omega_i t}|0\rangle = \hat b^\dagger(t)|0\rangle, \qquad \sum_i|c_i|^2=1
$$

**Derived From:** superposing single-photon-in-one-mode states $|1\rangle_i=\hat a_i^\dagger|0\rangle$ with amplitudes $c_i$, then restoring each mode's free time evolution $\hat a_i^\dagger\to\hat a_i^\dagger e^{-i\omega_it}$.

## Supporting Formulas

- $\hat b^\dagger \equiv \sum_i c_i\hat a_i^\dagger$ — the collective "wave-packet" creation operator for the whole superposition
- Envelope $\mathcal E(t)=\sum_i c_i\,e^{-i\omega_it}$ — the same Fourier relationship that connects a classical pulse shape to its frequency components
- Spontaneous-emission example: the emitted wave packet decays over a characteristic time $T_s$, with emission linewidth $\Delta\omega_A\sim1/T_s$

## Derivation Outline

1. Write a single photon confined to mode $i$ as $\hat a_i^\dagger|0\rangle$.
2. Superpose over many modes with complex amplitudes $c_i$, normalized so $\sum_i|c_i|^2=1$.
3. Restore each mode's free time evolution to obtain the time-dependent wave-packet state and its envelope $\mathcal E(t)$.

## Physical Intuition

A single photon in one perfectly sharp mode would be a plane wave stretching across all of space and lasting forever — not remotely like the localized flash of light we usually picture when we say "one photon." To get something localized in time and space, a single photon has to be spread across a whole range of modes at once, each with its own small amplitude, so that they interfere constructively only in a limited region and destructively everywhere else — exactly the same trick a classical pulse uses to be localized rather than an endless sine wave. This is most concrete in spontaneous emission: an excited atom doesn't release a single-frequency photon instantly, it releases a decaying wave packet over its characteristic lifetime $T_s$, and because that packet has a finite duration, its frequency content necessarily has a finite spread — the shorter the emission, the broader the linewidth, which is the same time–frequency trade-off already seen as the photon-number–phase uncertainty.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Photon Number States](Photon%20Number%20States.md), [Electromagnetic Field Quantization](Electromagnetic%20Field%20Quantization.md), [Hong-Ou-Mandel Effect](Hong-Ou-Mandel%20Effect.md)
**Full Derivation:**
