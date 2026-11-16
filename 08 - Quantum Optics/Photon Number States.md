---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Number (Fock) states $|n\rangle$ are the energy eigenstates of a single quantized field mode, containing exactly $n$ photons with a completely undefined phase. The mean field of a Fock state vanishes identically — the extreme opposite of a classical wave.

## Key Equation

$$
\hat N|n\rangle = n|n\rangle, \qquad \hat H|n\rangle = \hbar\omega\left(n+\frac12\right)|n\rangle
$$

**Derived From:** specializing the general quantum harmonic oscillator ladder-operator algebra (see [Harmonic Oscillator Ladder Operators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md)) to a single field mode, where $\hat N=\hat a^\dagger\hat a$ literally counts the photons occupying that mode.

## Supporting Formulas

- $\langle n|\hat X|n\rangle=0=\langle n|\hat P|n\rangle \implies \langle n|\hat E(\vec r,t)|n\rangle=0$ — the mean field of any Fock state is exactly zero
- Number–phase trade-off: $\Delta n\,\Delta\varphi\approx\dfrac{1}{\sqrt2}$ — see [Number-Phase Uncertainty](Number-Phase%20Uncertainty.md)
- In phase space, a Fock state looks like a perfect circle: fixed radius (fixed photon number $n$), uniform in angle (completely undefined phase)

## Derivation Outline

1. Take the general harmonic-oscillator ladder algebra and specialize $\hat a,\hat a^\dagger,\hat N$ to a single field mode.
2. Interpret $\hat N=\hat a^\dagger\hat a$ physically as the photon-number operator for that mode.
3. Evaluate $\hat X,\hat P$ (and hence the field operator) in a number-state expectation value, finding it vanishes because $|n\rangle$ carries no phase information.

## Physical Intuition

A Fock state is what you get if you insist on knowing *exactly* how many photons are present in a mode — no more, no less. That certainty about photon number comes at a steep price: the state has absolutely no preferred phase, so if you ask "which way is the electric field pointing right now," the honest answer is that every direction is equally likely, and the average field is exactly zero. This is the polar opposite of a classical light wave, which has a perfectly well-defined amplitude and phase but no sharp photon number at all. In the phase-space picture, a Fock state is a thin ring centered on the origin — its distance from the center (set by $n$) is fixed, but it is smeared uniformly all the way around in angle. This number/phase trade-off is a genuine uncertainty relation in its own right, distinct from (though related to) the ordinary quadrature uncertainty.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Harmonic Oscillator Ladder Operators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md), [Coherent States](Coherent%20States.md), [Number-Phase Uncertainty](Number-Phase%20Uncertainty.md), [Quadrature Operators](Quadrature%20Operators.md), [Electric Field Operator](Electric%20Field%20Operator.md)
**Full Derivation:**
