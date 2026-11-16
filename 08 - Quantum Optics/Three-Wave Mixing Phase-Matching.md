---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

A medium with a second-order nonlinear response couples three optical fields together, generating new frequencies at the sum and difference of the inputs. This coupling only builds up efficiently over the length of the medium, though, if the three waves stay in phase with each other as they propagate. That requirement is the condition of phase matching.

## Key Equation

$$
\frac{dA_3}{dz} = 2\pi i\frac{\omega_3}{cn_3}\tilde\chi^{(2)}A_1A_2e^{i\Delta k z}, \qquad \Delta k \equiv k_1+k_2-k_3
$$

**Derived From:** substituting the second-order nonlinear polarization $P^{(2)}\propto\chi^{(2)}E^2$ as a source term into the nonlinear wave equation, Fourier-transforming to follow a single frequency component, and applying the slowly-varying-envelope approximation ($dA/dz\ll kA$) to reduce the second-order wave equation to a first-order coupled-mode equation for each of the three interacting frequencies.

## Supporting Formulas

- Nonlinear polarization expansion: $P=\chi^{(1)}E+\chi^{(2)}E^2+\chi^{(3)}E^3+\cdots$
- Nonlinear wave equation: $\left(\nabla^2-\dfrac{n}{c^2}\partial_t^2\right)E=\dfrac{4\pi}{c^2}\partial_t^2P_{NL}$ — an ordinary wave equation with the nonlinear polarization as a driving source term
- Full set of three coupled-mode equations for sum-frequency ($\omega_3=\omega_1+\omega_2$) and difference-frequency generation, related by cyclic permutation of the three frequency/index labels
- Perfect phase matching, $\Delta k=0$: the generated field stays in phase with the polarization driving it throughout the medium, so the interaction builds up coherently (and, for undepleted-pump amplification, hyperbolically) with propagation length; away from $\Delta k=0$, the interaction only oscillates in and out of phase and never accumulates

## Derivation Outline

1. Expand the medium's polarization response to second order in the applied field, giving a term that couples pairs of frequency components into sum and difference frequencies.
2. Insert this polarization as a source in the wave equation and Fourier-decompose into individual frequency components.
3. Apply the slowly-varying-envelope approximation, converting the second-order wave equation into a set of coupled first-order equations for the complex amplitude of each interacting frequency.
4. Identify the accumulated phase mismatch $\Delta k=k_1+k_2-k_3$ between the three waves as the factor controlling whether the interaction builds up coherently or washes out with propagation.

## Physical Intuition

Ordinary (linear) optical media respond to light in direct proportion to the field, so different frequencies of light pass through independently and never talk to each other. A nonlinear medium is different: strong enough light bends the medium's response into a quadratic term, and that quadratic term is exactly what lets two input frequencies combine to drive a polarization oscillating at their sum or difference — effectively creating a new color of light from two others. But just creating the right driving polarization isn't enough for that new field to actually grow as it propagates: the newly generated wave and the polarization driving it have to stay "in step" with each other all along the medium, the same way pushing a swing only builds up amplitude if your pushes stay synchronized with its motion. If the three waves' wavevectors don't satisfy $\Delta k=0$, the newly generated field slips in and out of phase with its own source term as it travels, so the contributions from different points in the medium partially cancel instead of adding up — phase matching is simply the condition that keeps every point in the medium contributing constructively to the growing new field.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md), [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md), [Squeezed States](Squeezed%20States.md)
**Full Derivation:**
