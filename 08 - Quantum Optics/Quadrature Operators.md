---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Any single field mode can be fully described by two real, non-commuting amplitudes: the in-phase quadrature $\hat X$ and the in-quadrature amplitude $\hat P$. These are the field-mode analogue of position and momentum. Any field state, classical or quantum, is then a point (or a fuzzy blob) in the resulting $(X,P)$ phase space.

## Key Equation

$$
\hat a = \frac{1}{\sqrt2}\left(\hat X+i\hat P\right), \qquad [\hat X,\hat P]=i
$$

**Derived From:** decomposing a general oscillating field $E(t)=E_0\cos(\omega t-\phi)$ via the cosine-difference identity into a $\cos(\omega t)$ component and a $\sin(\omega t)$ component, defining their coefficients as $X$ and $P$, then quantizing them as the field-mode counterparts of position and momentum.

## Supporting Formulas

- $E(t) = X\cos(\omega t) + P\sin(\omega t)$ — quadrature decomposition of a classical single-mode field
- Polar form: $r=\sqrt{X^2+P^2}\propto\sqrt{\text{intensity}}\propto\sqrt{\langle\hat n\rangle}$, $\theta=\arctan(P/X)=$ optical phase
- Uncertainty relation: $\Delta X\,\Delta P\geq\tfrac12$
- Field operator: $\hat{\vec E}(z,t)\propto \hat X\cos(\omega t)+\hat P\sin(\omega t)$, equivalently $\hat a e^{-i\omega t}+\hat a^\dagger e^{i\omega t}$ — see [Electric Field Operator](Electric%20Field%20Operator.md)
- In a standing-wave cavity mode at $t=0$, $\hat E$ is determined by $\hat X$ alone and $\hat B$ by $\hat P$ alone; at general $t$ both operators mix into both fields, exactly as a pendulum's fixed initial position and momentum mix into its position and momentum at later times

## Derivation Outline

1. Write a general single-mode field with an arbitrary phase, $E(t)=E_0\cos(\omega t-\phi)$.
2. Expand via the cosine-difference identity into separate $\cos(\omega t)$ and $\sin(\omega t)$ pieces, defining their real coefficients as $X$ and $P$.
3. Promote $X,P$ to non-commuting operators through $\hat a=(\hat X+i\hat P)/\sqrt2$, so that $[\hat a,\hat a^\dagger]=1$ forces $[\hat X,\hat P]=i$.

## Physical Intuition

A single mode of light oscillating at frequency $\omega$ needs exactly two numbers to describe it completely at any instant: how much of it is "in step" with a cosine reference wave, and how much is "a quarter-cycle behind" (in step with a sine wave instead). Those two numbers are $X$ and $P$. Classically they are just two ordinary real numbers you could measure with arbitrary precision — together they say everything about the field's amplitude and phase. Quantum mechanically, though, they behave exactly like position and momentum of a particle: they don't commute, so you cannot know both perfectly at once, and any quantum state of light is smeared out into a fuzzy blob in the $(X,P)$ plane rather than sitting at one sharp point. Physically, $X$ tracks the electric-field-like part of the mode and $P$ tracks the magnetic-field-like part, and as time runs forward the two continuously trade places — exactly the way a pendulum's potential and kinetic energy trade back and forth, only here it's electric and magnetic energy doing the trading.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Electric Field Operator](Electric%20Field%20Operator.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Homodyne Detection](Homodyne%20Detection.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md), [Displacement Operator](Displacement%20Operator.md), [Squeezed States](Squeezed%20States.md), [Photon Number States](Photon%20Number%20States.md)
**Full Derivation:**
