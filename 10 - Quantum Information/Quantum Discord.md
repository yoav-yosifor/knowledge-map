---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Quantum discord captures nonclassical correlations that go beyond [entanglement](Entanglement.md). It's defined as the gap between the total correlations in a state and the correlations that measurement can classically access. That gap can be nonzero even for separable (unentangled) states.

## Key Equation

$$
\delta(A\to B) = I(A:B) - J(A\to B), \qquad J(A\to B) = S(\rho_B) - \sum_a p_a\, S(\rho_{B|a})
$$

**Derived From:** [Quantum Mutual Information](Quantum%20Mutual%20Information.md) minus a measurement-based classical correlation $J(A\to B)$, maximized over all measurements on $A$ — in classical information theory these two definitions of mutual information coincide, but measurement disturbance makes them diverge quantum mechanically.

## Supporting Formulas

- Entanglement $\Rightarrow$ nonzero discord; nonzero discord can exist without entanglement

## Derivation Outline

1. Take the total correlations between $A$ and $B$ as the [Quantum Mutual Information](Quantum%20Mutual%20Information.md) $I(A:B)$.
2. Define the measurement-based classical correlation $J(A\to B)=S(\rho_B)-\sum_a p_a S(\rho_{B|a})$, maximized over all measurements on $A$.
3. Classically these two expressions for mutual information coincide; measurement disturbance makes them diverge quantum mechanically.
4. Define discord as the leftover: $\delta(A\to B)=I(A:B)-J(A\to B)$.
5. Since separable states can still have $J<I$, discord can be nonzero even without entanglement.

## Physical Intuition

Classically, there are two equivalent ways to ask how correlated two variables are: compare their combined uncertainty to their individual uncertainties, or ask how much learning one variable's value narrows down the other. In ordinary probability theory these two questions always give the same number. Quantum mechanically they don't, and that mismatch is exactly what quantum discord measures. The reason they split apart is that "learning" a quantum subsystem's value requires actually measuring it, and measurement is not a passive read-out — it disturbs the system, and different choices of measurement basis disturb it differently and extract different amounts of correlation. Quantum discord asks you to find the best possible measurement, the one that disturbs least and extracts the most classical-looking correlation, and then it counts whatever correlation is left over as genuinely quantum. What makes this surprising is that you don't need entanglement to have some of this left-over correlation — two particles can be completely unentangled, in the sense that their joint state factorizes into no entangled piece whatsoever, and still be correlated in a way that no measurement can fully extract without disturbing the state. So discord is a strictly broader net than entanglement: every entangled state has nonzero discord, but plenty of separable, unentangled states have nonzero discord too, revealing a layer of "quantumness" that lives outside of entanglement altogether.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quantum Mutual Information](Quantum%20Mutual%20Information.md), [Entanglement](Entanglement.md)
**Full Derivation:**
