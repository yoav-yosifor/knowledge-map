---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

Sensitivity is the smallest change in a physical parameter that a measurement can statistically distinguish from no change at all. It's a sharper question than the SNR, because it doesn't ask "how clear is the signal" but rather "how far apart do two nearby parameter values have to be before their outcomes can be told apart."

## Key Equation

$$
\Delta\phi_{min} = \frac{\Delta\hat O(\phi_0)}{\partial_\phi\langle\hat O(\phi_0)\rangle}
$$

**Derived From:** requiring that the change in the mean of a measured observable $\hat O$ between two nearby parameter values $\phi_0$ and $\phi_0+\Delta\phi$ exceed the observable's own standard deviation, $\left|\langle\hat O(\phi_0)\rangle-\langle\hat O(\phi_0+\Delta\phi)\rangle\right|\geq\Delta\hat O(\phi_0)$, then linearizing the left side for small $\Delta\phi$ and solving for the smallest resolvable $\Delta\phi$.

## Supporting Formulas

- A change in the measured observable is only statistically real once it exceeds the observable's own noise — this is the single inequality the whole definition rests on
- An improvement in sensitivity is expected specifically when the measured observable is aligned with whichever quadrature a non-linear (squeezing) process has attenuated, since squeezing leaves the *mean* of a coherent state's quadrature unchanged but reduces its noise

## Derivation Outline

1. Take two measurements of an observable $\hat O$ at parameter values $\phi_0$ and $\phi_0+\Delta\phi$ and require their means to differ by at least one standard deviation to be statistically distinguishable.
2. Multiply and divide the left side by $\Delta\phi$ and take $\Delta\phi$ small, turning the mean difference into a derivative.
3. Solve for $\Delta\phi$ to isolate the smallest resolvable parameter change, $\Delta\phi_{min}$.

## Physical Intuition

Signal-to-noise ratio tells you how clean a single measurement looks, but it doesn't directly answer the question an experimentalist actually cares about: if I nudge some knob by a tiny amount, will my instrument even notice? Sensitivity answers exactly that — it compares how much the average reading shifts per unit change of the parameter against how noisy any single reading already is. A measurement is only useful for detecting a small change if that change moves the average by more than the reading jitters around on its own. This is why squeezed light helps: an ordinary coherent state has the same amount of noise in every direction of phase space, but a squeezed state has quieter noise in one particular direction. If you arrange your measurement so the parameter you care about shows up specifically in that quiet direction, you get to keep the full signal while suffering less of the noise that would otherwise mask it — directly sharpening the sensitivity.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Standard Quantum Limit](Standard%20Quantum%20Limit.md), [Squeezed-Light Mach-Zehnder Interferometer](Squeezed-Light%20Mach-Zehnder%20Interferometer.md), [SU(1,1) Interferometer](SU(1,1)%20Interferometer.md)
**Full Derivation:**
