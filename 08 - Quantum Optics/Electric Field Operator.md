---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The quantized electric field at a point in space and time is not a number but a Hermitian operator built from each mode's photon creation and annihilation operators — the field-mode analogue of the position operator of a harmonic oscillator.

## Key Equation

$$
\hat{\vec E}(\vec r,t)=\sum_{\vec k,\lambda} i\sqrt{\frac{\hbar\omega_k}{2\varepsilon_0 V}}\,\hat e_{\vec k,\lambda}\left(\hat a_{\vec k,\lambda}e^{i(\vec k\cdot\vec r-\omega_k t)}-\hat a^\dagger_{\vec k,\lambda}e^{-i(\vec k\cdot\vec r-\omega_k t)}\right)
$$

**Derived From:** applying $\vec E=-\partial_t\vec A$ (Coulomb gauge) to the plane-wave mode expansion of $\vec A$, then substituting the same operator-normalized mode amplitude $A_{\vec k,\lambda}\to\sqrt{\hbar/2\varepsilon_0V\omega_k}\,\hat a_{\vec k,\lambda}$ used to reach $\hat H_\text{EM}=\sum\hbar\omega_k(\hat n+\tfrac12)$ — full chain in [Electromagnetic Field Quantization Derivation](Electromagnetic%20Field%20Quantization%20Derivation.md).

## Supporting Formulas

- Single-mode form, dropping the quantization-volume/vector-potential bookkeeping: $\hat E(z,t)\propto\hat a\,e^{-i\omega t}+\hat a^\dagger e^{i\omega t}$ — manifestly Hermitian, since it is an operator plus its own adjoint
- Quadrature form: $\hat E(z,t)\propto \hat X\cos\omega t+\hat P\sin\omega t$, the same field written in terms of the in-phase/in-quadrature amplitudes — see [Quadrature Operators](Quadrature%20Operators.md)
- Field operator at a fixed atomic position, used for dipole coupling: $\hat{\vec E}(\vec R)=\sum_{\vec k,\lambda}E_{\vec k,\lambda}(\vec R)\left(\hat a_{\vec k,\lambda}+\hat a_{\vec k,\lambda}^\dagger\right)$, folding the per-photon amplitude and spatial phase into $E_{\vec k,\lambda}(\vec R)$ — see [Jaynes-Cummings Hamiltonian Derivation](Jaynes-Cummings%20Hamiltonian%20Derivation.md)
- Vacuum expectation: $\langle 0|\hat{\vec E}|0\rangle=0$ but $\langle 0|\hat E^2|0\rangle\neq0$ — the field averages to zero even with no photons present, but its fluctuations don't
- Fock-state expectation: $\langle n|\hat E(\vec r,t)|n\rangle=0$ for every $n$ — see [Photon Number States](Photon%20Number%20States.md)

## Derivation Outline

1. Start from $\vec E=-\partial_t\vec A$ in the Coulomb gauge, applied to the classical plane-wave mode expansion of $\vec A$.
2. Differentiate each mode in time: this pulls out a factor of $i\omega_k$ and flips the relative sign between the two conjugate terms (since $\partial_t e^{\mp i\omega_k t}=\mp i\omega_k e^{\mp i\omega_k t}$).
3. Promote $A_{\vec k,\lambda}\to\hat a_{\vec k,\lambda}$ using the same operator-normalized amplitude that turns the classical mode energy into $\hbar\omega_k(\hat n+\tfrac12)$, yielding a Hermitian per-mode operator built from one annihilation and one creation operator.

## Physical Intuition

Once the field is quantized, asking "what is the electric field right here, right now" no longer has a single answer — it has an operator, and that operator is built the same way a harmonic oscillator's position is built from ladder operators: a photon being destroyed contributes one piece, a photon being created contributes its mirror-image piece, and the field value is what's left when you add them together. That structure has an immediate consequence: because the field operator doesn't commute with the photon-number operator, a state with a perfectly definite number of photons has a completely undefined field value — its phase is totally random, so the average field is exactly zero even though photons are present. This is the same complementarity as position and momentum, now playing out between photon number and field phase. It also means the vacuum itself — the state with zero photons — is not a state of zero field. The field operator's expectation value is zero, but it still fluctuates around that zero, because an operator built from $\hat a$ and $\hat a^\dagger$ never truly vanishes even when there is nothing to annihilate or create yet. Those vacuum fluctuations are not a mathematical artifact; they are the same zero-point restlessness every quantum harmonic oscillator has in its ground state, and they are what eventually drives an excited atom to spontaneously emit even in perfectly empty space.

## Isomorphisms

- Identical in structure to the position operator of a single mechanical harmonic oscillator, $\hat x=\sqrt{\hbar/2m\omega}\,(\hat a+\hat a^\dagger)$ — the field operator is literally "the position of that mode's oscillator," rescaled into field units. See [Harmonic Oscillator Ladder Operators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md).

## Open Questions

- [ ]

---

## Links

**Related:** [Electromagnetic Field Quantization](Electromagnetic%20Field%20Quantization.md), [Quadrature Operators](Quadrature%20Operators.md), [Photon Number States](Photon%20Number%20States.md), [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Harmonic Oscillator Ladder Operators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md)
**Full Derivation:** [Electromagnetic Field Quantization Derivation](Electromagnetic%20Field%20Quantization%20Derivation.md)
