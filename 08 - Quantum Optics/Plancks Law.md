---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Quantizing the energy each [electromagnetic mode](Electromagnetic%20Mode%20Density.md) can carry, rather than letting every mode share the same classical thermal energy, exponentially suppresses high-frequency modes. This replaces classical physics's prediction of infinite radiated power with a finite, correctly peaked blackbody spectrum.

## Key Equation

$$
u(\omega)\,d\omega = \frac{\hbar\omega^3}{\pi^2 c^3}\cdot\frac{1}{e^{\beta\hbar\omega}-1}\,d\omega
$$

**Derived From:** multiplying the density of electromagnetic modes $g(\omega)=\omega^2/\pi^2c^3$ (see [Electromagnetic Mode Density](Electromagnetic%20Mode%20Density.md)) by the energy per quantum $\hbar\omega$ and by the mean occupation number of each mode, $\langle n(\omega)\rangle = 1/(e^{\beta\hbar\omega}-1)$, obtained from Bose–Einstein statistics applied to Planck's postulate that each mode's energy is quantized as $\varepsilon_n=n\hbar\omega$.

## Supporting Formulas

- Bose–Einstein mode probability: $P_n = e^{-n\beta\hbar\omega}(1-e^{-\beta\hbar\omega})$
- Mean occupation number: $\langle n(\omega)\rangle = 1/(e^{\beta\hbar\omega}-1)$
- Classical (Rayleigh–Jeans) limit: at low frequency, $e^{\beta\hbar\omega}-1\approx\hbar\omega/k_BT$, recovering $u_{RJ}(\omega)=k_BT\cdot g(\omega)$ — consistent with the classical equipartition theorem, and the regime where the UV catastrophe would otherwise diverge

## Derivation Outline

1. Postulate that each electromagnetic mode's energy is quantized in units of $\hbar\omega$, rather than continuously variable.
2. Use Bose–Einstein statistics at temperature $T$ to find the mean number of quanta occupying a mode of frequency $\omega$.
3. Multiply the mean energy per mode ($\hbar\omega$ times the mean occupation number) by the density of modes to get the spectral energy density.

## Physical Intuition

Classical equipartition treats every electromagnetic mode as equally entitled to the same average thermal energy $k_BT$, no matter its frequency — and because there are more and more modes available at higher frequencies, this predicts that a hot object should radiate an infinite amount of power, mostly at very short wavelengths. Planck's fix is that energy in each mode can only come in discrete chunks of size $\hbar\omega$: exciting a high-frequency mode costs a large energy quantum, and at any finite temperature the probability of paying that cost falls off exponentially. So instead of every mode carrying the same energy, high-frequency modes are almost always found empty — the classically inevitable pileup of energy at short wavelengths simply never accumulates, and the total radiated power stays finite and correctly matches what is measured.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Electromagnetic Mode Density](Electromagnetic%20Mode%20Density.md), [Einstein Coefficients](Einstein%20Coefficients.md)
**Full Derivation:**
