---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Applying the [two-mode squeezing operator](Squeezed%20States.md) to two vacuum modes creates photons in matched pairs split between the two modes. This generates a continuous-variable entangled state whose cross-mode position difference and momentum sum are squeezed together toward zero fluctuation. That is precisely the correlation structure needed to approximate the [EPR](../10%20-%20Quantum%20Information/EPR%20Argument.md) state.

## Key Equation

$$
|0,0\rangle_r = \hat S_{AB}(r)|0\rangle_A|0\rangle_B = \exp\!\left[r\left(\hat a^\dagger\hat b^\dagger-\hat a\hat b\right)\right]|0\rangle_A|0\rangle_B
$$

**Derived From:** generalizing the single-mode [Squeezed States](Squeezed%20States.md) operator to two distinct field modes $A,B$ — the generator $\hat a^\dagger\hat b^\dagger-\hat a\hat b$ creates or destroys photons in the two modes as matched pairs rather than two-at-a-time in a single mode; physically this is the non-degenerate (signal/idler) regime of the [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md).

## Supporting Formulas

- Bogoliubov transform of the annihilation operators: $\hat S_{AB}^\dagger\hat a_A\hat S_{AB}=\cosh r\,\hat a_A+\sinh r\,\hat a_B^\dagger$, $\hat S_{AB}^\dagger\hat a_B\hat S_{AB}=\cosh r\,\hat a_B+\sinh r\,\hat a_A^\dagger$
- Quadrature sum/difference squeezing: $\hat S_{AB}^\dagger(\hat P_A\pm\hat P_B)\hat S_{AB}=e^{\mp r}(\hat P_A\pm\hat P_B)$; the position quadratures scale oppositely, so $\hat X_A-\hat X_B$ is squeezed by $e^{-r}$ while $\hat X_A+\hat X_B$ is anti-squeezed by $e^{+r}$
- Position-quadrature transform: $\hat S_{AB}^\dagger\hat X_A\hat S_{AB}=\cosh r\,\hat X_A+\sinh r\,\hat X_B$, and correspondingly for $\hat X_B$
- As $r\to\infty$, both $\hat X_A-\hat X_B$ and $\hat P_A+\hat P_B$ are squeezed toward zero fluctuation simultaneously, and the state converges to the continuous-variable EPR state — full derivation in [Two-Mode Squeezed Vacuum Derivation](Two-Mode%20Squeezed%20Vacuum%20Derivation.md)

## Derivation Outline

1. Generalize the single-mode squeezing generator to two modes, coupling $A$ and $B$ so that photons are created or destroyed in matched pairs.
2. Read off the Bogoliubov transform of $\hat a_A,\hat a_B$ under conjugation by $\hat S_{AB}(r)$.
3. Combine into quadrature operators and take sum/difference combinations across the two modes.
4. Observe that the sum and difference quadratures scale by inverse exponential factors of $r$ — one cross-mode combination squeezed, the complementary one anti-squeezed.

## Physical Intuition

A single-mode squeezer pulls photons out of the vacuum two at a time into the same mode. A two-mode squeezer instead creates photons in pairs split across two different modes, A and B — every time a photon shows up in A, a partner shows up in B, born together. Because they're always created in step, the difference between A's and B's positions gets quieter and quieter as the squeezing grows, and so does the sum of their momenta, even though each mode individually gets noisier on its own. Push the squeezing parameter to its limit and A's position becomes essentially locked to B's, while their combined momentum becomes essentially fixed too — exactly the pair of simultaneously sharp, complementary properties at the heart of the EPR paradox, produced here by an entirely ordinary piece of nonlinear-optics hardware rather than a thought experiment.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md), [Squeezed States](Squeezed%20States.md), [SPDC Time-Frequency Entanglement](SPDC%20Time-Frequency%20Entanglement.md), [EPR Argument](../10%20-%20Quantum%20Information/EPR%20Argument.md)
**Full Derivation:** [Two-Mode Squeezed Vacuum Derivation](Two-Mode%20Squeezed%20Vacuum%20Derivation.md)
