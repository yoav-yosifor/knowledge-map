---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

The quantum-operator treatment of a beamsplitter: a unitary two-mode scattering element. It must inject [vacuum fluctuations](Vacuum%20Fluctuations.md) into any unused port to keep the field operators canonical. It behaves like a particle-splitter for [single photons](Photon%20Number%20States.md) but like a classical wave-divider for [coherent states](Coherent%20States.md).

## Prerequisite Concepts

- [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md) — the base real-rotation transformation this generalizes to complex transmission/reflection amplitudes
- [Vacuum Fluctuations](Vacuum%20Fluctuations.md) — what necessarily enters the unused port to preserve unitarity
- [Photon Number States](Photon%20Number%20States.md) — describes the particle-like single-photon input case
- [Coherent States](Coherent%20States.md) and [Displacement Operator](Displacement%20Operator.md) — describe the wave-like coherent-state input case
- [Beamsplitter Loss Model](Beamsplitter%20Loss%20Model.md) — the same vacuum-injection argument applied to modeling optical loss and detector inefficiency
- [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md) — used to quantify the perfect anti-correlation a single photon produces at the two outputs

## Regimes and Parameters

- General complex scattering matrix $\begin{bmatrix}t&r\\r&t\end{bmatrix}$; unitarity forces $|t|^2+|r|^2=1$ and a fixed relative phase $\phi_r-\phi_t=\pm\pi/2$ between reflection and transmission — a convenient choice is $t=\sqrt T$, $r=i\sqrt{1-T}$
- Attenuating a single mode by bare rescaling, $\hat a^{out}=\sqrt T\hat a^{in}$, breaks the canonical commutator $[\hat a^{out},\hat a^{\dagger out}]=T\leq1$; only mixing in a second, vacuum-populated mode through the full two-port unitary restores $[\hat a^{out},\hat a^{\dagger out}]=1$ — full derivation for the general-loss version of this argument in [Beamsplitter Loss Derivation](Beamsplitter%20Loss%20Derivation.md)
- Single-photon input ($|1\rangle_a\otimes|0\rangle_b$): output is $t|1\rangle_a|0\rangle_b+r|0\rangle_a|1\rangle_b$ — the photon goes entirely to one port or the other, never splits, giving perfect anti-correlation $g^{(2)}(0)=0$ between the two detectors
- Coherent-state input ($|\alpha\rangle_a\otimes|0\rangle_b$): output is $|t\alpha\rangle_a\otimes|r\alpha\rangle_b$ — the amplitude simply divides between the ports, exactly the classical expectation; a linear beamsplitter can never instead produce the "whole amplitude in superposition" cat-like state $r|\alpha\rangle_a|0\rangle_b+t|0\rangle_a|\alpha\rangle_b$
- Detector inefficiency $\eta$ modeled as an ideal detector preceded by a fictitious beamsplitter of transmission $\eta$ mixing the signal with vacuum: the mean count is attenuated, $\langle\hat n\rangle=\eta\langle\hat n_{in}\rangle$, but the full counting statistics undergo binomial thinning, $P_m(\eta)=\sum_{n=m}^\infty p_n\binom{n}{m}\eta^m(1-\eta)^{n-m}$ — each of $n$ incoming photons is independently detected with probability $\eta$
- General linear optics (any combination of beamsplitters, phase shifters, mirrors, etalons — described by a unitary mode matrix $u_{kk'}$) always maps a coherent state to another coherent state, $\alpha_k^{(out)}=\sum_{k'}u_{kk'}\alpha_{k'}^{(in)}$ — genuinely non-classical light can only be produced by an inherently non-linear process

## Physical Intuition

A beamsplitter looks, classically, like a simple partial mirror: some light goes through, some reflects. Quantum mechanically it has to do something subtler to stay consistent — if you tried to model "losing" half the light by just shrinking the field operator, you would also be illegally shrinking its irreducible quantum noise, which the uncertainty principle forbids. The fix is that the "missing" port isn't really empty: vacuum fluctuations leak in through it, and that leakage is exactly what keeps the bookkeeping consistent. This single requirement then explains two very different-looking behaviors depending on what you send in. A lone photon is indivisible — it cannot be shared between two paths, so it commits entirely to one output or the other, and the two detectors downstream can never click together. A coherent state, by contrast, behaves like the classical wave it approximates — its amplitude genuinely splits between both outputs, each remaining a well-behaved, classical-looking beam. The same vacuum-leakage idea also explains why a real, imperfect photon detector looks mathematically identical to a perfect detector preceded by a lossy beamsplitter: each photon independently "survives" or is "lost" with some fixed probability, exactly like a coin flip repeated once per photon. And zooming out, no matter how many beamsplitters and phase shifters you chain together, if you start with a classical (coherent) state you can only ever get another classical state out — turning classical light into something genuinely quantum requires leaving the world of simple linear optics altogether.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Beamsplitter Loss Model](Beamsplitter%20Loss%20Model.md), [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md), [Hong-Ou-Mandel Effect](Hong-Ou-Mandel%20Effect.md)
**Concepts Used:** [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Photon Number States](Photon%20Number%20States.md), [Coherent States](Coherent%20States.md)
