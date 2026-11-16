---
tags:
  - quantum-mechanics-1
  - concept
  - technique
---
---
## Core Idea

For any complete orthogonal basis, the sum of that basis's projection operators equals the identity operator — which means any operator or state can be rebuilt, with no information lost, by "inserting" this sum into it.

## Key Equation

$$
\sum_n |n\rangle\langle n| = \hat{I}
$$

**Derived From:** completeness of the basis $\{|n\rangle\}$ — every physical state can be expanded in it, so projecting onto every basis state and summing the projections reconstructs the identity exactly.

## Supporting Formulas

- Expanding a state: $|\psi\rangle = \hat I|\psi\rangle = \sum_n |n\rangle\langle n|\psi\rangle = \sum_n c_n|n\rangle$, with $c_n=\langle n|\psi\rangle$ the probability amplitude for outcome $n$
- Spectral decomposition of an operator: inserting $\hat I$ into $\hat H = \hat H \hat I$ and using $\hat H|i\rangle = E_i|i\rangle$ gives $\hat H = \sum_j E_j\,|j\rangle\langle j|$ — any operator is rebuilt from its eigenvalues and eigenprojectors
- Each term $E_j|j\rangle\langle j|$ is a projection operator $\hat P_j$ scaled by the eigenvalue

## Derivation Outline

1. Start from a Hermitian operator's eigenvalue equation $\hat H|i\rangle = E_i|i\rangle$, valid for every basis state $|i\rangle$.
2. Multiply $\hat H$ on the right by the identity written as $\sum_i|i\rangle\langle i|$ — this is legal for any complete basis because the identity does nothing to whatever it multiplies.
3. Distribute $\hat H$ through the sum: $\hat H|i\rangle$ becomes $E_i|i\rangle$ term by term, so the whole operator collapses into $\sum_i E_i|i\rangle\langle i|$ — the spectral decomposition falls out automatically, it is not an extra assumption.

## Result

$$
\hat{H} = \sum_j E_j\,|j\rangle\langle j|
$$

## Physical Intuition

Completeness is the statement that a chosen set of measurement outcomes exhausts every possibility — there is nowhere else for the system to be. Because of that, "asking every possible question and adding up the answers" (projecting onto every basis state and summing) reproduces the original object with nothing missing and nothing double-counted. Inserting the identity this way is a bookkeeping trick that costs nothing physically — it just re-expresses an operator or a state in a chosen language of basis states — but it is the single mechanical step that turns an abstract operator into an explicit, calculable sum over energies and projectors.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [The Trace Operation](The%20Trace%20Operation.md)
**Full Derivation:**
