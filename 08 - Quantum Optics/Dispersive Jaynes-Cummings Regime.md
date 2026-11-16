---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Far off resonance, the atom and cavity barely exchange real excitations, but they still shift each other's frequencies. The cavity frequency picks up a shift that depends on the atomic state but not on photon number, while the atom's frequency picks up a shift proportional to the [photon number](Photon%20Number%20States.md). This lets the photon number be measured through the atom's frequency without ever absorbing a photon.

## Key Equation

$$
\hat H \approx \hbar\left(\omega_c+\frac{g^2}{\Delta}\hat\sigma_z\right)\hat a^\dagger\hat a + \frac{\hbar}{2}\left(-\Delta+\frac{g^2}{2\Delta}\right)\hat\sigma_z
$$

**Derived From:** expanding the [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md) to second order in $g/\Delta$ in the dispersive limit $|\Delta|\gg2g$, where $\Delta=\omega_c-\omega_{eg}$.

## Supporting Formulas

- Dispersive (quantum non-demolition) interaction term: $\hat H_{int}=\dfrac{g^2}{\Delta}\hat\sigma_z\,\hat a^\dagger\hat a$
- Since $[\hat H_{int},\hat a^\dagger\hat a]=0$, the photon number is a conserved quantity of the dispersive dynamics — a **quantum non-demolition (QND)** coupling, allowing photon number to be inferred from its effect on the atomic transition frequency without disturbing the photon number itself
- Non-linear (photon-number-dependent) atomic frequency shift: $\dfrac{g^2}{\Delta}\hat\sigma_z$ — acts like a spin-dependent index of refraction, the cavity-QED analogue of the classical AC Stark shift $\Omega^2/4\Delta$; see [Dressed States](Dressed%20States.md) for the classical-drive AC Stark effect this generalizes
- Lamb shift: $\dfrac{g^2}{2\Delta}$ — a shift of the atomic energy that persists even with zero photons present in the cavity

## Derivation Outline

1. Take the exact Jaynes-Cummings eigenstructure and expand it perturbatively in the small parameter $g/\Delta$, valid when the detuning greatly exceeds the coupling strength.
2. Retain terms to second order in $g/\Delta$, yielding an effective Hamiltonian with no remaining direct atom-photon exchange term.
3. Identify the resulting cavity-frequency shift (state-dependent, photon-number-independent) and atomic-frequency shift (photon-number-dependent) as separate physical effects.

## Physical Intuition

When the cavity and atom are tuned far apart in frequency, they can no longer trade a real photon back and forth — there just isn't enough energy overlap for that exchange to conserve energy. But they still "feel" each other, the same way two off-resonant coupled pendulums still slightly repel each other's natural frequencies even without ever fully exchanging their motion. That gentle repulsion shows up as two distinct shifts: the atom nudges the cavity's resonance depending on which atomic state it's in, and — more usefully — the cavity photons nudge the atom's own transition frequency by an amount that grows with how many photons are present. Because this interaction commutes with the photon-number operator, it never actually removes or adds photons while it does this — it just reads out how many are there via a change in the atom's frequency, which is exactly what makes it a "quantum non-demolition" measurement: you learn the photon number without disturbing it. Even in the complete absence of light, the atom's energy is still nudged slightly by its coupling to the empty cavity mode — this residual shift is the Lamb shift, a real, measurable signature of the atom's coupling to the vacuum itself.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md), [Dressed States](Dressed%20States.md), [Photon Number States](Photon%20Number%20States.md)
**Full Derivation:**
