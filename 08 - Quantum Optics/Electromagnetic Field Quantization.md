---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The free electromagnetic field, expanded into plane-wave modes under the Coulomb gauge, is mathematically identical to an infinite collection of independent [harmonic oscillators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md) — one per mode $(\vec k,\lambda)$. Quantizing the field then means promoting each mode's classical amplitude to a creation/annihilation operator pair.

## Key Equation

$$
\hat H_\text{EM} = \sum_{\vec k,\lambda}\varepsilon_0 V\omega_k^2\left(\hat n_{\vec k,\lambda}+\frac12\right)
$$

**Derived From:** computing the total classical field energy $U=\frac12\int(E^2+B^2)\,d\vec r$ in the plane-wave eigenmode expansion, recognizing it as a sum of independent oscillator energies, then replacing the classical mode amplitude $A_{\vec k,\lambda}\to\hat a_{\vec k,\lambda}$ — full chain in [Electromagnetic Field Quantization Derivation](Electromagnetic%20Field%20Quantization%20Derivation.md).

## Supporting Formulas

- Coulomb (transverse) gauge condition: $\nabla\cdot\vec A=0$
- Free-photon dispersion relation: $\omega_k=c|\vec k|$
- Bosonic commutation relation: $[\hat a,\hat a^\dagger]=1$
- Photon number operator per mode: $\hat n_{\vec k,\lambda}=\hat a^\dagger_{\vec k,\lambda}\hat a_{\vec k,\lambda}$
- With standard normalization $A_{\vec k,\lambda}=\sqrt{\hbar/2\varepsilon_0V\omega_k}\,\hat a_{\vec k,\lambda}$, the familiar form $\hat H_\text{EM}=\sum\hbar\omega_k(\hat n_{\vec k,\lambda}+\tfrac12)$ follows
- Same normalization, applied to $\vec E=-\partial_t\vec A$, gives the quantized field itself as a mode sum of $\hat a,\hat a^\dagger$ — see [Electric Field Operator](Electric%20Field%20Operator.md)

## Derivation Outline

1. Start from Maxwell's equations in free space and introduce the vector/scalar potentials $\vec A,\phi$.
2. Fix the Coulomb gauge, which collapses the coupled potential equations to a single wave equation for $\vec A$.
3. Expand $\vec A$ in plane-wave eigenmodes; each mode amplitude then obeys a harmonic-oscillator equation of motion.
4. Compute the total field energy — cross-mode terms vanish by orthogonality, leaving a sum of independent oscillator energies.
5. Promote each classical mode amplitude to a ladder operator, imposing the bosonic commutator.

## Physical Intuition

Before any quantum mechanics is invoked, Maxwell's equations already force each independent "shape" the field can take — each plane wave of a given direction, frequency and polarization — to oscillate in time exactly like a mass on a spring. That is not an analogy imposed from outside; it falls straight out of the wave equation once you decompose the field into its natural modes. Quantizing the field then means nothing more exotic than doing to each of those infinitely many independent springs exactly what is done to a single quantum harmonic oscillator: replacing its classical amplitude with a pair of operators that create and destroy one quantum of energy at a time. Each quantum in mode $(\vec k,\lambda)$ is a photon of that mode's frequency and direction, and the total field energy is just the sum of all these independent oscillators' energies, including an unavoidable half-quantum of zero-point energy in every single mode.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Electric Field Operator](Electric%20Field%20Operator.md), [Quadrature Operators](Quadrature%20Operators.md), [Photon Number States](Photon%20Number%20States.md), [Harmonic Oscillator Ladder Operators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md)
**Full Derivation:** [Electromagnetic Field Quantization Derivation](Electromagnetic%20Field%20Quantization%20Derivation.md)
