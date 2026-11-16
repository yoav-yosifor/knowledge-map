---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

Transposing only one subsystem of a bipartite density matrix (the partial transpose) and checking whether the result stays positive semidefinite gives a practical test for [entanglement](Entanglement.md). A negative eigenvalue after partial transpose always proves entanglement. For the smallest bipartite dimensions, this test is complete — it catches every entangled state.

## Key Equation

$$
(\rho_{AB}^{T_B})_{ij,i'j'} = (\rho_{AB})_{ij',i'j}
$$

**Derived From:** transposing only the indices belonging to subsystem $B$ in the matrix elements of $\rho_{AB}$ written in a product basis, leaving subsystem $A$'s indices untouched.

## Supporting Formulas

- If $\rho_{AB}^{T_B}$ has a negative eigenvalue $\Rightarrow$ entangled; if $\rho_{AB}^{T_B}\ge0$, the state is called PPT
- For $2\times2$ and $2\times3$ systems: PPT is necessary **and** sufficient for separability
- For $3\times3$ and larger: PPT is necessary but not sufficient — PPT entangled ("bound entangled") states exist
- Negativity, quantifying the violation: $\mathcal{N}(\rho) = \sum_{\lambda_i<0} |\lambda_i(\rho^{T_B})|$; logarithmic negativity $E_{\mathcal N} = \log_2\|\rho^{T_B}\|_1$
- Beyond PPT, converging numerical tests exist: DPS and NPA semidefinite-programming hierarchies

## Derivation Outline

1. Write $\rho_{AB}$ in a product basis with matrix elements indexed by $(i,j),(i',j')$.
2. Transpose only the $B$-indices, leaving $A$ untouched: $(\rho_{AB}^{T_B})_{ij,i'j'}=(\rho_{AB})_{ij',i'j}$.
3. Require the result stay positive semidefinite, the same sanity check every valid density matrix must pass.
4. Any state built from local pieces (separable) stays positive under this partial transpose, so PPT holds for all separable states.
5. A negative eigenvalue of $\rho^{T_B}$ therefore proves entanglement; only in $2\times2$/$2\times3$ is PPT also sufficient, while larger systems admit PPT bound-entangled states.

## Physical Intuition

Every legitimate density matrix has to come out positive semidefinite — that's just the statement that all measurement probabilities it predicts have to be non-negative, a basic sanity requirement of any physical state. The clever trick behind the PPT test is to take a state shared between two parties and transpose only one party's half of it, leaving the other party's half completely alone, and then ask whether the resulting matrix still passes that same positivity sanity check. If a state was built purely from local operations and classical communication — no real entanglement — this partial flip can never break positivity, because you can always trace the operation back to a state that was some honest mixture of independent, transposition-friendly pieces on each side. So if you do the partial transpose and discover a negative eigenvalue popping out, that's an unambiguous, ironclad signature that no such honest local recipe could have produced the state — it must be entangled. What makes this test only a practical stepping stone rather than the final word is that the logic only runs in one direction for larger systems: for the two smallest possible bipartite sizes, passing this test also guarantees separability, so the test is perfectly complete there, but for bigger systems there turn out to be strange "bound entangled" states that sail through the positivity check completely undetected while still being genuinely entangled underneath.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement Detection](Entanglement%20Detection.md), [Concurrence](Concurrence.md), [Entanglement](Entanglement.md)
**Full Derivation:**
