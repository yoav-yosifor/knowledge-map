---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The second-order coherence function $g^{(2)}(\tau)$ measures correlations between the *intensity* at two different times, rather than the field itself. It's the quantity that separates classical light, which always bunches or stays flat ($g^{(2)}(0)\geq1$), from genuinely quantum light, which can show antibunching ($g^{(2)}(0)<1$).

## Key Equation

$$
g^{(2)}(\tau) = \frac{\langle I(t)\,I(t+\tau)\rangle}{\langle I(t)\rangle^2}
$$

**Derived From:** normalizing the intensity-intensity correlation function $G^{(2)}(\tau)=\langle I(t)I(t+\tau)\rangle$ by the squared mean intensity, in direct analogy to how $g^{(1)}$ normalizes the field autocorrelation $G^{(1)}$.

## Supporting Formulas

- $g^{(2)}(0)\geq 1$ for any classical field — a direct consequence of the Cauchy–Schwarz inequality $\langle I^2\rangle\geq\langle I\rangle^2$
- $g^{(2)}(0)\geq g^{(2)}(\tau)$ for stationary light — the zero-lag correlation is always the maximum
- $g^{(2)}(\tau) = 1 + \dfrac{\langle\Delta I(t)\Delta I(t+\tau)\rangle}{\langle I(t)\rangle^2}$, with $\Delta I=I-\langle I\rangle$ — a field with no intensity fluctuations has $g^{(2)}=1$ for all $\tau$
- Siegert relation, for Gaussian (thermal/chaotic) light only: $g^{(2)}(\tau) = 1+|g^{(1)}(\tau)|^2$
- Sub-Poissonian light ($\Delta n^2<\langle n\rangle$, equivalently $g^{(2)}(0)<1$) cannot arise from any classical field — a purely quantum signature; see [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md)

## Derivation Outline

1. Define the intensity-intensity correlator $G^{(2)}(\tau)=\langle I(t)I(t+\tau)\rangle$, the natural second-order analogue of $G^{(1)}$.
2. Normalize by $\langle I\rangle^2$ to get $g^{(2)}$.
3. Apply the Cauchy–Schwarz inequality to $\langle I^2\rangle$ to establish $g^{(2)}(0)\geq1$ classically.
4. For Gaussian field statistics, use the Gaussian moment theorem to factor the fourth-order field correlator into products of second-order ones, yielding the Siegert relation.

## Physical Intuition

Where $g^{(1)}$ asks "does the wave still remember its own phase after a delay $\tau$?", $g^{(2)}$ asks a completely different question: "if I see a bright flash of light now, am I more or less likely to see another bright flash a time $\tau$ later?" For ordinary chaotic light (like a thermal source), intensity fluctuates in noisy bursts, so seeing one photon makes it *more* likely to see another one nearby in time — this is bunching, and it is why $g^{(2)}(0)>1$ for such sources. A perfectly steady classical beam has no such correlation and sits at exactly $g^{(2)}=1$. But no classical wave, however you shape its noise, can ever make photons *less* likely to arrive close together than chance would predict — that anti-bunching behavior, $g^{(2)}(0)<1$, only happens for light made of individual quantum emitters, like a single atom that must fully re-excite before it can emit again.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [First-Order Coherence Function](First-Order%20Coherence%20Function.md), [Hanbury-Brown and Twiss Experiment](Hanbury-Brown%20and%20Twiss%20Experiment.md), [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md), [Quantum Second-Order Coherence](Quantum%20Second-Order%20Coherence.md)
**Full Derivation:**
