---
tags:
  - quantum-mechanics-1
  - concept
  - technique
---
---
## Core Idea

The Baker–Campbell–Hausdorff (BCH) formula lets you combine or reorder exponentials of non-commuting operators. Its truncated forms turn otherwise-intractable operator exponentials — like [displacement](Displacement%20Operator.md), [rotation](Phase-Space%20Rotation%20Operator.md), and [squeezing](Squeezed%20States.md) transformations — into simple, closed-form actions on ladder operators.

## Key Equation

$$
e^{\hat A+\hat B} = e^{\hat A}\,e^{\hat B}\,e^{-\frac12[\hat A,\hat B]}, \qquad \text{valid when } [\hat A,[\hat A,\hat B]]=[\hat B,[\hat A,\hat B]]=0
$$

**Derived From:** truncating the general BCH expansion $e^{\hat A}e^{\hat B}=\exp\bigl(\hat A+\hat B+\tfrac12[\hat A,\hat B]+\tfrac1{12}[\hat A,[\hat A,\hat B]]-\tfrac1{12}[\hat B,[\hat A,\hat B]]+\cdots\bigr)$ to its first term whenever all higher nested commutators vanish — which happens automatically whenever $[\hat A,\hat B]$ is itself a c-number (an ordinary number rather than an operator).

## Supporting Formulas

- Conjugation form: $e^{-\hat A}\hat B e^{\hat A}=\displaystyle\sum_n\frac{[\hat A,\hat B]^{(n)}}{n!}$, with $[\hat A,\hat B]^{(n)}\equiv[\hat A,[\hat A,\hat B]^{(n-1)}]$ ($n$ nested commutators, $[\hat A,\hat B]^{(0)}\equiv\hat B$)
- If the nested-commutator series alternates sign at every step while staying proportional to the same operator, it resums into a trigonometric factor — the signature of a rotation-type transformation
- If the series never closes but instead keeps alternating between two different operators, it resums into hyperbolic functions — the signature of a squeezing-type (Bogoliubov) transformation

## Derivation Outline

1. Start from the general BCH series for $e^{\hat A}e^{\hat B}$, an infinite sum of nested commutators.
2. Note every commutator nested inside $[\hat A,[\hat A,\hat B]]$ or deeper vanishes whenever $[\hat A,\hat B]$ is a plain number rather than an operator.
3. All terms beyond the first two drop out, leaving just $\hat A+\hat B+\tfrac12[\hat A,\hat B]$ in the exponent.
4. Re-exponentiate this truncated sum to get the closed form $e^{\hat A}e^{\hat B}e^{-\frac12[\hat A,\hat B]}$.

## Physical Intuition

Ordinary numbers satisfy $e^ae^b=e^{a+b}$, but operators generally don't, because $\hat A$ and $\hat B$ don't commute — the order in which you apply them matters. The BCH formula is the precise correction factor needed to fix this: it tells you exactly how much "extra" you pick up from reordering two operator exponentials, and that extra piece is built entirely out of commutators of $\hat A$ and $\hat B$. The truncated version used throughout quantum optics is a special case that becomes enormously powerful: whenever the commutator of the two operators is just a plain number (rather than yet another operator), the correction collapses to a single multiplicative factor and the whole infinite series terminates. This is exactly what happens for the generators of displacement, rotation, and squeezing transformations on a field mode, which is why the same technique — write the conjugation series, notice it resums into something simple (a phase, or hyperbolic functions) — appears again and again across those derivations.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Displacement Operator](Displacement%20Operator.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md), [Squeezed States](Squeezed%20States.md)
**Full Derivation:**
