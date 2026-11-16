---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

A classical light field with constant intensity produces photodetector clicks that are Poisson distributed in any counting window. A classically fluctuating intensity only ever broadens this distribution further (super-Poissonian). So any measured narrowing below Poisson ([sub-Poissonian statistics](Second-Order%20Coherence%20Function.md)) is impossible for a classical field, and signals genuinely quantum light.

## Key Equation

$$
P(n,T) = \frac{\langle n\rangle^n}{n!}\,e^{-\langle n\rangle}, \qquad \langle n\rangle = \zeta\,\bar I(t,T)\,T
$$

**Derived From:** the single assumption that a detector clicks in $(t,t+dt)$ with probability proportional to the instantaneous intensity, $p(t)\,dt=\zeta I(t)\,dt$; solving the resulting [Mandel Recurrence Formula](Mandel%20Recurrence%20Formula.md) gives the Poisson distribution exactly when the intensity is deterministic.

## Supporting Formulas

- $\Delta n^2 = \langle n\rangle$ — variance equals the mean, the defining signature of Poissonian shot noise
- $\text{SNR} = \sqrt{\langle n\rangle}$ — shot-noise-limited signal-to-noise ratio, improving with intensity for any classical source
- Super-Poissonian statistics: if the intensity itself fluctuates and is averaged over its distribution $P(I)$, $P(n,T)=\int dI\,P(I)\,\frac{(\eta IT)^n}{n!}e^{-\eta IT}$, giving excess variance $\Delta\lambda^2=\eta^2\langle I\rangle+\eta^2\Delta I^2$
- Sub-Poissonian statistics ($\Delta n^2<\langle n\rangle$) cannot arise from any classical field — see [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md) for the equivalent statement in terms of $g^{(2)}(0)<1$
- A coherent state of light reproduces exactly this Poisson law quantum mechanically, $\Delta n^2=\langle n\rangle=|\alpha|^2$ — see [Coherent States](Coherent%20States.md)

## Derivation Outline

1. Postulate a click probability proportional to instantaneous intensity, $p(t)\,dt=\zeta I(t)\,dt$.
2. Build the exact recurrence relating the probability of $m$ counts over a window to $m-1$ and $m$ counts over a slightly shorter window — the [Mandel Recurrence Formula](Mandel%20Recurrence%20Formula.md).
3. Solve the recurrence exactly for constant intensity, obtaining a Poisson distribution parameterized by the mean expected count.
4. Average over a distribution of intensities to see how classical fluctuations only ever broaden the count distribution.

## Physical Intuition

Imagine raindrops falling onto a fixed patch of ground at a perfectly steady average rate: even though the rate is constant, the exact number of drops landing in any given minute still varies randomly from one minute to the next, and the spread of that variation is fully determined by the average rate itself — nothing more. That is exactly what Poisson statistics mean for a photodetector watching a steady beam of light: the mean count sets the variance too, with no independent "extra" noise. If the light source itself is unsteady — its intensity drifting up and down over time — then counting windows land on different_local rates, adding an extra layer of randomness on top of the shot noise and broadening the distribution further (super-Poissonian). The one thing no classical, however-noisy light source can ever do is make the count distribution *narrower* than plain shot noise, because classical intensity fluctuations can only add noise, never subtract it — a distribution narrower than Poisson requires photons to somehow "avoid" arriving too close together, which is a genuinely particle-like, quantum effect.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Mandel Recurrence Formula](Mandel%20Recurrence%20Formula.md), [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md), [Coherent States](Coherent%20States.md)
**Full Derivation:** [Mandel Recurrence Formula](Mandel%20Recurrence%20Formula.md)
