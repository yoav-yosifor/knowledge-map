---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

In a real ensemble of atoms, each atom sees its own slightly different effective detuning, caused by things like Doppler shifts, spatial field variation, or stray fields. Every individual atom still stays perfectly coherent, but the ensemble-averaged signal decays as the atoms' phases fan out and cancel each other. Unlike true decoherence, this dephasing is deterministic, so it can in principle be reversed.

## Key Equation

$$
T_2^* = \frac{1}{\Delta\Omega}
$$

**Derived From:** modeling the ensemble as a Gaussian distribution of detunings with rms width $\Delta\Omega$; after a $\pi/2$-pulse each atom precesses freely at its own $\Delta_k$, and the ensemble-averaged coherence is the Fourier transform of that Gaussian distribution, itself a Gaussian decay $\langle\sigma_x(t)\rangle=e^{-(\Delta\Omega\,t)^2/2}\cos(\Omega_0 t)$.

## Supporting Formulas

- Sources of spread in $\Delta_k=\omega_{A,k}-\omega_L$: Doppler shift from thermal atomic velocities ($\Delta\omega_D\sim\omega_L\sqrt{k_BT/mc^2}$, typically hundreds of MHz for alkali atoms), inhomogeneous laser beam intensity, inhomogeneous static (magnetic/electric) fields, laser frequency noise
- Ensemble-averaged coherence: $\langle\rho'_{21}(t)\rangle = \int \rho'_{21}(t;\Delta_k)\,P(\Delta_k)\,d\Delta_k$ — decays not because any atom loses coherence, but because different atoms' phases $\Delta_k t$ interfere destructively when summed
- Relationship to the total dephasing rate: $1/T_2 = 1/T_2^{(\text{inhomog})} + 1/T_2^{(\text{homog})}$ — see [T1 and T2 Relaxation](T1%20and%20T2%20Relaxation.md); $T_2^*\ll T_2$ in a thermal ensemble, since the inhomogeneous term normally dominates
- Reversibility: fully recoverable via [Spin Echo (Photon Echo)](Spin%20Echo.md), in contrast to the irreversible homogeneous contributions

## Derivation Outline

1. Recognize that every atom in a real ensemble has its own effective detuning $\Delta_k$, due to Doppler shifts, spatial inhomogeneities, or local field variation.
2. Model the spread of detunings across the ensemble as a probability distribution $P(\Delta_k)$ (Gaussian, for thermal Doppler broadening).
3. Average the individually-coherent, individually-precessing atomic responses over this distribution; because atoms with different $\Delta_k$ accumulate different phases at different rates, the ensemble average decays even though no single atom has actually lost coherence.

## Physical Intuition

Imagine a large group of perfectly synchronized runners all starting a lap at the same instant, but each running at a very slightly different, fixed pace — after some time, purely because of that spread in speeds, the group spreads out around the track and no longer looks synchronized from a distance, even though every individual runner is still running at their own perfectly steady, predictable pace. That is exactly what inhomogeneous dephasing is: nothing random or irreversible has happened to any individual atom, but the group average washes out because the atoms have "unfair" personal detunings baked in by things like their individual velocities. Because each atom's rate is fixed and known in principle, this kind of dephasing can be completely undone — a well-timed pulse that flips every atom's position mid-race lets the fast ones, now placed behind, catch back up to the slow ones exactly when they all needed to realign, recovering the full signal.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [T1 and T2 Relaxation](T1%20and%20T2%20Relaxation.md), [Spin Echo (Photon Echo)](Spin%20Echo.md), [Adiabatic Rapid Passage](Adiabatic%20Rapid%20Passage.md)
**Full Derivation:**
