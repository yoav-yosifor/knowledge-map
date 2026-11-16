---
tags:
  - optics
  - concept
---
---
## Core Idea

Past the critical angle, the [Fresnel reflection coefficient](../02%20-%20Electromagnetism/Fresnel%20Coefficients.md) stops being a real amplitude ratio and becomes a pure phase factor. Total internal reflection sends back 100% of the amplitude, but stamps it with a phase shift that depends on angle and polarization.

## Key Equation

$$
\tan(\phi_{TE}) = \frac{\sqrt{n_1^2\sin^2\theta_1 - n_2^2}}{n_1\cos\theta_1}
$$

**Derived From:** given directly once $\theta_{in}>\theta_{cr}$, where $\sin\theta_{cr}=n_2/n_1$ (from Snell's law with $n_2<n_1$) forces $r=e^{i2\phi(\theta)}$; the source states this result without deriving it from the Fresnel coefficients.

## Supporting Formulas

- Critical angle: $\sin\theta_{cr} = n_2/n_1$ if $n_2<n_1$
- TM phase from TE phase: $\tan(\phi_{TM}) = \dfrac{n_1^2}{n_2^2}\tan(\phi_{TE})$
- Beyond critical angle: $r=e^{i2\phi(\theta)}$, and note that $t\neq0$ even though all power is reflected

## Derivation Outline

1. Start from the Fresnel $r_{TE}$ formula and let $\theta_{in}$ exceed the critical angle.
2. Note that $\cos\theta_t$ becomes imaginary once $\sin\theta_t>1$, turning $r_{TE}$ into a ratio of two complex conjugates.
3. A ratio of a complex number to its own conjugate always has unit magnitude and a well-defined phase — write $r=e^{i2\phi}$.
4. Take the argument of that ratio to read off $\tan\phi_{TE}$ in terms of $n_1$, $n_2$, $\theta_1$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Fresnel Coefficients](../02%20-%20Electromagnetism/Fresnel%20Coefficients.md), [Goos-Hänschen Shift](../09%20-%20Nanophotonics/Goos-Hänschen%20Shift.md), [TIR Self-Consistency Derivation](../09%20-%20Nanophotonics/TIR%20Self-Consistency%20Derivation.md)
**Full Derivation:**
