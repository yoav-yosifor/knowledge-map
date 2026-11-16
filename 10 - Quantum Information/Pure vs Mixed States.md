---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

A pure state is complete knowledge of a quantum system's state vector — nothing about it is unknown. A mixed state is different: it describes classical uncertainty over which pure state the system is actually in, or it arises when the system has become entangled with an unmeasured environment ([decoherence](Decoherence.md)). Either way, mixed states generally show reduced or absent interference.

## Key Equation

$$
\rho = \sum_j p_j |\psi_j\rangle\langle\psi_j|, \qquad p_j \ge 0,\ \sum_j p_j = 1
$$

**Derived From:** [Density Matrix](Density%20Matrix.md) definition — a pure state is the special case of a single term, $\rho=|\psi\rangle\langle\psi|$.

## Supporting Formulas

- Purity $\gamma \equiv \mathrm{Tr}(\rho^2)$: pure $\Leftrightarrow \gamma=1$; maximally mixed ($\rho=I/d$) $\Leftrightarrow \gamma=1/d$; always $1/d \le \gamma \le 1$
- On the [Bloch Sphere](Bloch%20Sphere.md): pure states are on the surface, mixed states are inside

## Derivation Outline

1. Start from the general [Density Matrix](Density%20Matrix.md) $\rho=\sum_j p_j|\psi_j\rangle\langle\psi_j|$.
2. A pure state is the special case of a single term (one $p_j=1$, rest 0): $\rho=|\psi\rangle\langle\psi|$.
3. Compute purity $\gamma=\mathrm{Tr}(\rho^2)$: equals 1 for pure states, $1/d$ for maximally mixed $\rho=I/d$, and lies between for general mixtures.
4. Map $\gamma$ onto the [Bloch Sphere](Bloch%20Sphere.md): pure states sit on the surface, mixed states shrink inward.

## Physical Intuition

Think of a pure state as the most complete description quantum mechanics allows you to give a system: if you know the exact recipe of amplitudes, there's nothing extra hiding underneath, and the system still carries its full capacity to interfere with itself. A mixed state, by contrast, is what you write down when you're missing part of the story — either because you only know the odds that the system was prepared this way or that way, or because it once interacted with something else you can no longer keep track of, so its fate got tangled up with an environment you don't have access to. Once that happens, the delicate cross-terms that produce interference get washed out, because they'd have to interfere consistently across every possibility in the mixture, and generically they don't. That's why a mixed state looks and behaves more like an ordinary classical coin flip than a genuine quantum superposition. Geometrically, this is the difference between standing exactly on the surface of the Bloch sphere, where every state is as pure and as interference-capable as it can be, and sitting somewhere inside it, where the vector has shrunk because it represents an average over several such surface points rather than any single one of them.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Density Matrix](Density%20Matrix.md), [Bloch Sphere](Bloch%20Sphere.md), [Decoherence](Decoherence.md)
**Full Derivation:**
