---
tags:
  - nanophotonics
  - concept
  - technique
---
---
## Core Idea

Instead of tracking the ring's steady-state spectrum, describe the slowly varying circulating amplitude $A_1(t)$ directly with a first-order rate equation: it is driven by the input through a coupling rate $\kappa_t$ and decays at a rate $\gamma/2$ set by the total (coupling + internal) loss per round trip. This is the same equation that describes a driven, damped harmonic oscillator or a series RLC circuit near resonance, which is where the form comes from.

## Key Equation

$$
\frac{dA_1}{dt}=-i\kappa_t\,A_{in}-\frac{\gamma}{2}\,A_1,\qquad
\kappa_t=\frac{\sqrt{\kappa}}{\tau_{RT}},\qquad
\gamma=\frac{\kappa+\alpha}{\tau_{RT}}
$$

**Derived From:** starting with the all-pass filter transmission relation $\left(1-\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}\right)A_1=-i\sqrt{\kappa}\,A_{in}$, linearizing the round-trip phase near resonance ($e^{-i\Delta\omega/\Delta\nu_{FSR}}\approx1-i\Delta\omega/\Delta\nu_{FSR}$), using the Fourier correspondence $i\Delta\omega A_1\leftrightarrow dA_1/dt$, and taking the high-$Q$ (small $\kappa,\alpha$) limit where $1-\sqrt{(1-\kappa)(1-\alpha)}\approx\tfrac12(\kappa+\alpha)$.

- $A_1(t)$ — slowly varying envelope of the circulating field, $E_1=A_1(t)e^{i\omega_0t}$ (SVEA)
- $\kappa_t$ — field-amplitude coupling rate = field coupling coefficient $\sqrt{\kappa}$ per round-trip time
- $\gamma$ — cavity linewidth (energy loss rate) = fractional power leaving via coupling + internal loss, per round trip

## Supporting Formulas

- Exact (pre-approximation) rate equation from the APF transfer function: $$\frac{dA_1}{dt}=-\frac{i\sqrt{\kappa}\,\Delta\nu_{FSR}}{\sqrt{(1-\kappa)(1-\alpha)}}A_{in}-\frac{1-\sqrt{(1-\kappa)(1-\alpha)}}{\sqrt{(1-\kappa)(1-\alpha)}}\Delta\nu_{FSR}\,A_1$$
- RLC analogue: a series $LCR$ loop driven by $v(t)$ obeys $\ddot v_c+\gamma\dot v_c+\omega_0^2v_c=\omega_0^2v(t)$ with $\omega_0^2=1/LC$, $\gamma=R/L$; under SVEA this collapses to $\dfrac{dv_0}{dt}=-i\kappa_t v_d-\dfrac{\gamma}{2}v_0$, with $\kappa_t=\dfrac{\omega_0}{2}\dfrac{R}{R+R_S}$ once a source resistor $R_S$ is added to mimic the input coupler.
- Harmonic-drive steady state of the oscillator: $v_0=\dfrac{\omega_0^2v_d}{\omega_0^2-\omega^2+i\omega\gamma}$; $\gamma$ is the FWHM of the resulting Lorentzian.
- The rate-equation picture implicitly assumes **high $Q$** and **operation near resonance** (SVEA); it is not valid far from a resonance.

## Derivation Outline

1. Take the APF relation between $A_1$ and $A_{in}$ containing the round-trip factor $\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\varphi}$.
2. Expand $e^{-i\varphi}\approx1-i\Delta\omega/\Delta\nu_{FSR}$ (near resonance) and separate the $A_1$ and $\Delta\omega A_1$ terms.
3. Replace $i\Delta\omega A_1$ by $dA_1/dt$ (Fourier transform property) to get the exact rate equation.
4. For high $Q$, use $\sqrt{(1-\kappa)(1-\alpha)}\approx1$ and $1-\sqrt{(1-\kappa)(1-\alpha)}\approx\tfrac12(\kappa+\alpha)$ to read off $\kappa_t=\sqrt{\kappa}/\tau_{RT}$ and $\gamma=(\kappa+\alpha)/\tau_{RT}$.
5. Cross-check by deriving the same equation from a series RLC circuit under SVEA.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Ring Resonator](Ring%20Resonator.md), [Cavity Q Factor and Finesse](Cavity%20Q%20Factor%20and%20Finesse.md), [All-Pass Ring Transfer Function Derivation](All-Pass%20Ring%20Transfer%20Function%20Derivation.md), [Coupled Mode Theory](Coupled%20Mode%20Theory.md)
**Full Derivation:** [Resonator Rate Equation Derivation](Resonator%20Rate%20Equation%20Derivation.md)
