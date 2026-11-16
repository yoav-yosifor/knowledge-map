---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

Both the **Q factor** and the **Finesse** measure how long light survives in the resonator before leaking out — they just use different clocks. Q counts the photon lifetime in units of the optical period ($1/\nu$); Finesse counts it in units of the round-trip time. Q is the natural figure of merit when comparing to the absolute frequency (linewidth, sensing); Finesse is the natural one when asking "how many times does a photon go around?"

## Key Equation

$$
Q=\omega_0\tau_c\approx\frac{\lambda}{\lambda_{FWHM}},\qquad
F=\frac{\tau_c}{\tau_{RT}}=\tau_c\,\Delta\nu_{FSR}
$$

**Derived From:** starting with the definition that the stored energy decays as $|E(t)|^2=E_0^2e^{-t/\tau_c}$, so $Q\equiv\omega_0\tau_c$; and from the general relation $Q=F\,\omega_0/\Delta\nu_{FSR}$ (with $\Delta\nu_{FSR}=1/\tau_{RT}$) solving for $F$.

- $\tau_c$ — cavity (photon) lifetime; also called the ring-down or energy-decay time
- $\tau_{RT}=1/\Delta\nu_{FSR}$ — round-trip time (see [Free Spectral Range](Free%20Spectral%20Range.md))
- $\lambda_{FWHM}$ — full width at half maximum of a resonance notch/peak

## Supporting Formulas

- For a ring, the cavity lifetime follows from the loss + coupling per round trip; for small loss $\alpha$ and coupling $\kappa$ the Finesse is simply $$F\approx\frac{1}{\alpha}\quad(\kappa\to0)$$
- **Loaded** Q — includes the power lost through the bus coupler ($\kappa$): $$Q=\frac{\omega_0\sqrt{(1-\alpha)(1-\kappa)}}{2\left[1-\sqrt{(1-\alpha)(1-\kappa)}\right]\Delta\nu_{FSR}}$$
- **Intrinsic** Q — the $\kappa\to0$ limit, set by internal loss alone: $$Q_{int}=\frac{\omega_0\sqrt{1-\alpha}}{2\left[1-\sqrt{1-\alpha}\right]\Delta\nu_{FSR}}\approx\frac{\omega_0}{\alpha\,\Delta\nu_{FSR}}$$
- Q depends on **both** loss and coupling because both drain power from the resonator. Fabricated micro-rings in the source reach $Q\sim10^4$.

## Derivation Outline

1. Define the photon lifetime through the energy decay $|E(t)|^2\propto e^{-t/\tau_c}$; set $Q=\omega_0\tau_c$ (photon lifetime measured in optical cycles).
2. Get $\tau_c$ for a ring either from the time-domain rate equation (input switched off → exponential ring-down) or from the per-round-trip power loss $e^{-\tau_{RT}/\tau_c}=1-\alpha$.
3. Substitute $\tau_c$ into $Q=\omega_0\tau_c$ for the loaded/intrinsic expressions; take small-$\alpha$ limits.
4. For the Finesse, combine $Q=\omega_0\tau_c$ with $Q=F\,\omega_0/\Delta\nu_{FSR}$ to get $F=\tau_c\,\Delta\nu_{FSR}=\tau_c/\tau_{RT}$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Free Spectral Range](Free%20Spectral%20Range.md), [Ring Resonator](Ring%20Resonator.md), [Ring Resonator Rate Equations](Ring%20Resonator%20Rate%20Equations.md), [Critical Coupling](Critical%20Coupling.md)
**Full Derivation:** [Cavity Q Factor Derivation](Cavity%20Q%20Factor%20Derivation.md)
