---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Superposition is not classical uncertainty about some hidden value. It is a direct consequence of the linearity of quantum dynamics: if two states are physically allowed, so is any linear combination of them. The system genuinely occupies that single combined state, not secretly one or the other.

## Key Equation

$$
|\psi\rangle = \alpha |0\rangle + \beta |1\rangle,
\qquad
|\alpha|^2 + |\beta|^2 = 1
$$

**Derived From:** linearity of the Schrödinger equation — if $|0\rangle$ and $|1\rangle$ are both valid solutions, any complex linear combination is too; normalization then fixes $|\alpha|^2+|\beta|^2=1$.

## Supporting Formulas

- Information is stored in the amplitudes $\alpha,\beta$ themselves, not just in eventual measurement outcomes —
- Relative phase between $\alpha$ and $\beta$ is physically meaningful and computationally used —

## Derivation Outline

1. Take two valid solutions $|0\rangle,|1\rangle$ of the Schrödinger equation for a given system.
2. Linearity of the Schrödinger equation means any complex combination $\alpha|0\rangle+\beta|1\rangle$ is also a valid solution.
3. Normalize: $|\alpha|^2+|\beta|^2=1$, fixing total probability.
4. The system genuinely occupies this combined state — not classical ignorance about which of $|0\rangle,|1\rangle$ it is — with information carried in the amplitudes and their relative phase.

## Physical Intuition

A superposition is not the system secretly being in $|0\rangle$ or $|1\rangle$ and us just not knowing which — it is a single, well-defined quantum state in its own right. Computation works by reshaping these amplitudes before the final measurement, not by the system "trying" both values at once.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Qubit](Qubit.md), [Interference](Interference.md)
**Full Derivation:**
