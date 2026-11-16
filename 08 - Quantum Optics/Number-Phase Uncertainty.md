---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

[Photon number](Photon%20Number%20States.md) and optical phase behave as an approximately conjugate pair. However, no Hermitian phase operator exists on the full Fock space. Well-defined phase states only exist on a truncated, finite-photon-number space, and it's from these that a proper phase probability distribution and an approximate number-phase uncertainty relation can be built.

## Key Equation

$$
\Delta n\,\Delta\varphi \approx \frac{1}{\sqrt2}
$$

**Derived From:** the polar decomposition $\hat a=\sqrt{\hat n}\,\hat e^{i\varphi}$ of the annihilation operator, whose phase factor $\hat e^{i\varphi}=\sum_n|n\rangle\langle n+1|$ turns out not to be unitary — showing directly that no genuine Hermitian phase operator exists — which motivates the finite-dimensional phase-state construction used instead.

## Supporting Formulas

- $(\hat e^{i\varphi})^\dagger\hat e^{i\varphi}=\hat I-|0\rangle\langle0|$ — the Susskind–Glogower operator fails unitarity only at $n=0$, which is exactly why it cannot be a genuine phase operator
- Finite-$N$ phase states: $|\varphi_m\rangle=\dfrac{1}{\sqrt{N+1}}\displaystyle\sum_{n=0}^N e^{in\varphi_m}|n\rangle$, $\varphi_m=\dfrac{2\pi m}{N+1}$ — orthonormal and complete on the truncated space, and $\hat n$ generates phase shifts on them, $e^{i\hat n\varphi_l}|\varphi_m\rangle=|\varphi_l+\varphi_m\rangle$
- Phase probability distribution: $P(\varphi)=\dfrac{1}{2\pi}\Bigl|\sum_n c_n e^{-in\varphi}\Bigr|^2$ for a state $|\psi\rangle=\sum_n c_n|n\rangle$
- Number state $|n\rangle$: phase totally undefined, $P_n(\varphi)=1/2\pi$ uniform, $\Delta\varphi=\pi/\sqrt3$
- Coherent state, $|\alpha|\gg1$: $\Delta\varphi^2=1/(2|\alpha|^2)$, and since $\Delta n=|\alpha|$ this reproduces $\Delta n\,\Delta\varphi=1/\sqrt2$

## Derivation Outline

1. Polar-decompose $\hat a$ into a positive operator $\sqrt{\hat n}$ and a phase factor $\hat e^{i\varphi}$.
2. Show the phase factor fails to be unitary — it is missing exactly the $n=0$ piece — so no Hermitian phase operator can exist.
3. Construct finite-$N$ phase states as a discrete Fourier transform of number states, and verify their orthogonality, completeness, and role as phase-shift generators.
4. Take the continuum limit $N\to\infty$ to get a genuine phase probability distribution, and evaluate it for number states and coherent states.

## Physical Intuition

Position and momentum have a clean, standard uncertainty relation because both have honest Hermitian operators behind them. Phase and photon number don't get that luxury: there simply is no well-behaved operator whose eigenvalues are "the phase of the field," because trying to build one from the natural candidate — factoring $\hat a$ into a magnitude and a phase, the way you'd factor a complex number — produces an object that fails to be unitary right at the bottom of the ladder, at zero photons. The physical reason is intuitive: you can't sensibly ask "what is the phase" of a state with zero photons, because there's no field there to have a phase at all. The workaround is to only ask the phase question on a space with a fixed maximum photon number, where a genuine, well-behaved family of phase states can be built; in that setting, the trade-off between knowing $n$ and knowing $\varphi$ becomes precise, and it interpolates smoothly between a number state (photon number is exact, phase is completely unknown) and a bright coherent state (phase is sharply defined, and the *relative* uncertainty in photon number becomes small).

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Photon Number States](Photon%20Number%20States.md), [Coherent States](Coherent%20States.md)
**Full Derivation:**
