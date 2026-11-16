---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The photon-number operator generates rotations of the quadrature axes in phase space. This sweeps the reference phase rather than the physical field itself. That same operator also generates the free time evolution that rigidly rotates a [coherent state](Coherent%20States.md)'s amplitude around the origin.

## Key Equation

$$
\hat R(\theta) = e^{-i\theta\hat a^\dagger\hat a}, \qquad \hat R^\dagger(\theta)\,\hat a\,\hat R(\theta) = e^{-i\theta}\hat a
$$

**Derived From:** the Baker–Campbell–Hausdorff conjugation series applied to the commutator $[\hat n,\hat a]=-\hat a$, whose nested commutators just alternate sign at every step, resumming exactly into a pure phase factor.

## Supporting Formulas

- $\hat X_\theta \equiv \hat R^\dagger(\theta)\hat X\hat R(\theta) = \hat X\cos\theta+\hat P\sin\theta$; $\hat P_\theta=-\hat X\sin\theta+\hat P\cos\theta$; $\hat P_\theta=\hat X_{\theta+\pi/2}$
- $[\hat X_\theta,\hat P_\theta]=i$ — the rotated quadratures remain canonically conjugate at every angle
- Free evolution under $\hat H=\hbar\omega\hat a^\dagger\hat a$ is exactly this rotation: $|\alpha(t)\rangle=|\alpha\,e^{-i\omega t}\rangle$, see [Coherent States](Coherent%20States.md)

## Derivation Outline

1. Write the BCH conjugation series for $\hat R^\dagger\hat a\hat R$ using the single commutator $[\hat n,\hat a]=-\hat a$.
2. Note every nested commutator in the series is just $(-1)^n\hat a$, so the whole series resums to $e^{-i\theta}\hat a$.
3. Substitute this transformed $\hat a$ (and its conjugate) into $\hat X,\hat P$ to obtain the rotated quadratures directly.

## Physical Intuition

The $X$ and $P$ axes of phase space aren't fixed by nature — they're fixed by an arbitrary choice of reference phase, the same way "north" on a map is a convention rather than a physical direction. The rotation operator is simply the tool that changes that reference: it spins the whole $(X,P)$ picture around the origin by an angle $\theta$ without moving or reshaping the physical state at all, exactly the way rotating a map doesn't move the city on it. What makes this genuinely useful, rather than just bookkeeping, is that ordinary free time evolution of a light field *is* exactly this kind of rotation: a coherent state with a fixed amplitude just spins steadily around the origin of phase space as time passes, at a rate set by the mode frequency, without ever spreading out or changing shape.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quadrature Operators](Quadrature%20Operators.md), [Coherent States](Coherent%20States.md), [Displacement Operator](Displacement%20Operator.md), [Baker-Campbell-Hausdorff Formula](../06%20-%20Quantum%20Mechanics%201/Baker-Campbell-Hausdorff%20Formula.md)
**Full Derivation:**
