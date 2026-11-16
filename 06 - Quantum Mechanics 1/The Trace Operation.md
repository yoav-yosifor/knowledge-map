---
tags:
  - quantum-mechanics-1
  - concept
  - technique
---
---
## Core Idea

The trace is a basis-independent linear map from operators to numbers — summing an operator's diagonal elements in any complete orthonormal basis always gives the same result, which makes it the natural tool for extracting physical, basis-free predictions (expectation values, purity) from an operator.

## Key Equation

$$
\text{tr}\,\hat{O} = \sum_i \langle i|\hat{O}|i\rangle
$$

**Derived From:** choosing any complete orthonormal basis $\{|i\rangle\}$ and summing the diagonal matrix elements of $\hat{O}$ in that basis; the value is the same for every choice of basis.

## Supporting Formulas

- Linearity: $\text{tr}(aA+bB) = a\,\text{tr}\,A + b\,\text{tr}\,B$ — the trace distributes over sums and scalar multiples
- Cyclic property: $\text{tr}(ABCD) = \text{tr}(BCDA) = \text{tr}(CDAB) = \text{tr}(DABC)$ — operators inside a trace may be cyclically permuted (this does **not** mean they commute; only cyclic reorderings are allowed)
- Expectation value: $\langle\hat{O}\rangle = \text{tr}(\hat{O}\rho)$ — see [Density Matrix](../10%20-%20Quantum%20Information/Density%20Matrix.md)

## Derivation Outline

1. Fix any complete orthonormal basis $\{|i\rangle\}$.
2. Define $\text{tr}\,\hat{O}$ as the sum of diagonal elements $\langle i|\hat{O}|i\rangle$ in that basis.
3. Show the sum is unchanged under a change of basis — this is what makes the trace a well-defined, basis-independent number rather than a basis-dependent bookkeeping quantity.

## Physical Intuition

A matrix element like $\langle i|\hat O|j\rangle$ depends on which basis you happened to write it in — rotate the basis and every individual number changes. The trace is the one number you can build from those elements that survives any such rotation, because it is really summing over probabilities weighted by outcomes rather than over basis-specific bookkeeping. That is exactly why it is the right tool to combine with an operator to get something physically meaningful (an expectation value, a purity): a physical prediction cannot depend on which arbitrary basis a physicist chose to write the state down in, and the trace guarantees that.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Density Matrix](../10%20-%20Quantum%20Information/Density%20Matrix.md), [Completeness Relation](Completeness%20Relation.md)
**Full Derivation:**
