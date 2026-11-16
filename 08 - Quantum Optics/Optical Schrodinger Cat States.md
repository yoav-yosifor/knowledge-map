---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

A [coherent state](Coherent%20States.md) evolved for exactly the right time under a Kerr nonlinearity splits into a macroscopic quantum superposition of two coherent states with opposite phase. This is a genuine "Schrödinger cat" made of light: a large, classical-looking field placed in superposition with its own phase-flipped twin.

## Key Equation

$$
|\text{CAT}\rangle = \frac{1}{\sqrt2}\left(e^{-i\pi/4}|i\alpha\rangle+e^{i\pi/4}|-i\alpha\rangle\right)
$$

**Derived From:** evolving a coherent state $|\alpha\rangle$ under the full (non-linearized) Kerr Hamiltonian $\hat H=\tfrac{\hbar\chi^{(3)}}{2}(\hat n^2-\hat n)$ for the special interaction time $\chi^{(3)}t=\pi$ — full derivation in [Kerr Cat State Derivation](Kerr%20Cat%20State%20Derivation.md).

## Supporting Formulas

- Full Kerr evolution operator: $\hat U(t)=\exp\left[-\tfrac{i\chi^{(3)}t}{2}(\hat n^2-\hat n)\right]$ — quadratic, not linear, in the photon number, which is what allows it to do more than merely squeeze the state (contrast with [Kerr-Effect Squeezing](Kerr-Effect%20Squeezing.md), the linearized, small-fluctuation limit of the same Hamiltonian)
- The cat state is an equal-weight superposition of two coherent states of amplitude $i\alpha$ and $-i\alpha$ — macroscopically distinct for large $|\alpha|$, since $|\langle i\alpha|-i\alpha\rangle|^2=e^{-2|\alpha|^2}\to0$

## Derivation Outline

1. Take the full (non-linearized) Kerr time-evolution operator and expand the input coherent state in the Fock basis.
2. Evaluate the resulting phase factor $(-i)^{n^2}$ at the special time $\chi^{(3)}t=\pi$, and note it takes only two distinct values depending on the parity of $n$.
3. Split the sum over Fock states into its even-$n$ and odd-$n$ parts using this parity dependence, and recognize each part as the Fock-basis expansion of a coherent state with a rotated amplitude.

## Physical Intuition

Squeezing reshapes a coherent state's noise but keeps it looking, in a broad sense, like a single classical field with an ellipse-shaped uncertainty blob. Evolving under the *full* Kerr Hamiltonian for long enough does something much stranger: because different photon numbers accumulate nonlinear phase at different rates (the phase shift per photon grows with $n$), a coherent state's initially smooth phase-space blob gets sheared and wrapped around itself. At the special moment $\chi^{(3)}t=\pi$, this wrapping resolves into something extremely clean — the state splits exactly in two, into a coherent state rotated one way and a coherent state rotated the opposite way, added together in quantum superposition. For a field with any appreciable brightness, these two components are essentially perfectly distinguishable classical states, so this really is a macroscopic "cat" — a genuinely mesoscopic-to-macroscopic quantum superposition, not merely reduced quantum noise. In practice this exact degree of coherence is essentially never observed for light itself, because loss and other decoherence destroy the delicate phase relationship long before the required nonlinear phase can accumulate; the equivalent experiment has, however, been successfully performed with Bose-Einstein condensates of atoms, which show the same underlying nonlinear dynamics.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Kerr-Effect Squeezing](Kerr-Effect%20Squeezing.md), [Coherent States](Coherent%20States.md), [Photon Number States](Photon%20Number%20States.md)
**Full Derivation:** [Kerr Cat State Derivation](Kerr%20Cat%20State%20Derivation.md)
