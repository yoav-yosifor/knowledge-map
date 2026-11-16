---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Coherent states $|\alpha\rangle$ are defined as the eigenstates of the annihilation operator, and they turn out to be the quasi-classical states of light — the closest quantum object to an ideal classical field of fixed complex amplitude $\alpha$. They carry the minimum uncertainty quantum mechanics allows, with [Poissonian](Poisson%20Photocount%20Statistics.md) photon-number statistics, which is why laser light near the quantum limit is well described by them.

## Key Equation

$$
\hat a|\alpha\rangle = \alpha|\alpha\rangle
$$

**Derived From:** requiring a quantum state whose mean electric field looks exactly like a classical oscillating field of complex amplitude $\alpha$; such a state is generated physically from the vacuum by the [Displacement Operator](Displacement%20Operator.md).

## Supporting Formulas

- Fock-basis expansion: $|\alpha\rangle=\displaystyle\sum_{n=0}^\infty\frac{\alpha^n}{\sqrt{n!}}e^{-|\alpha|^2/2}|n\rangle$, giving Poissonian photon statistics $P_n=\dfrac{|\alpha|^{2n}}{n!}e^{-|\alpha|^2}$
- $\langle\alpha|\hat n|\alpha\rangle=|\alpha|^2$, $\Delta n^2=\langle n\rangle$ — exactly the Poissonian statistics found classically for constant-intensity photodetection, see [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md)
- $\Delta X=\Delta P=1/\sqrt2$, saturating $\Delta X\Delta P=\tfrac12$, independent of the measurement angle $\theta$
- Mean field: $\langle\alpha|\hat E(\vec r,t)|\alpha\rangle=\sqrt{\pi\hbar\omega/V}\,\text{Re}\{\alpha\,e^{-i(\omega_kt-\vec k\cdot\vec r)}\}$ — looks exactly like a classical field
- Non-orthogonality: $|\langle\alpha|\beta\rangle|^2=e^{-|\alpha-\beta|^2}$ — distinct coherent states are never exactly orthogonal, only nearly so once $|\alpha-\beta|$ is large
- Free evolution: $|\alpha(t)\rangle=|\alpha\,e^{-i\omega t}\rangle$ — a coherent state stays coherent and simply rotates rigidly in phase space, see [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md)

## Derivation Outline

1. Impose $\hat a|\alpha\rangle=\alpha|\alpha\rangle$ and expand $|\alpha\rangle=\sum_n c_n|n\rangle$ in the Fock basis, giving a recursion $c_{n+1}=\alpha c_n/\sqrt{n+1}$.
2. Solve the recursion and normalize to fix $c_0$, giving the Poissonian Fock-basis coefficients.
3. Compute the mean field, quadrature variances, and photon-number variance directly from $\hat a|\alpha\rangle=\alpha|\alpha\rangle$ and its conjugate.

## Physical Intuition

A coherent state is the quantum state that behaves as much like an ideal classical light wave as quantum mechanics allows. Its defining property — being an eigenstate of the annihilation operator — sounds abstract, but its consequence is intuitive: if you compute the average electric field in this state, you get back exactly the oscillating classical field you'd expect from a laser, complete with a well-defined amplitude and phase. It still carries irreducible quantum noise (equal amounts in both quadratures, at the smallest amount the uncertainty principle allows), and its photon number still fluctuates randomly shot-to-shot in exactly the Poissonian way a classical steady beam does when counted by a detector — but beyond that minimal noise, it is as "classical" as a quantum state of light can be. This is why a well-stabilized laser, even though its light is fundamentally quantum, can be modeled almost perfectly as a classical field: its quantum state is extremely close to a coherent state.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Displacement Operator](Displacement%20Operator.md), [Photon Number States](Photon%20Number%20States.md), [Squeezed States](Squeezed%20States.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md), [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md), [Strong Coherent Field Approximation](Strong%20Coherent%20Field%20Approximation.md)
**Full Derivation:**
