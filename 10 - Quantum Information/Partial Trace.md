---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

The partial trace removes an unobserved subsystem from a joint [density matrix](Density%20Matrix.md), while preserving all measurement statistics on the remaining subsystem. It's the standard way to compute the reduced state of one part of an [entangled](Entanglement.md) system.

## Key Equation

$$
\rho_A = \mathrm{Tr}_B(\rho_{AB}) = \sum_b (I_A\otimes\langle b|)\,\rho_{AB}\,(I_A\otimes|b\rangle)
$$

**Derived From:** requiring $\rho_A$ to reproduce exactly the measurement statistics of any observable acting only on subsystem $A$, summed over an orthonormal basis $\{|b\rangle\}$ of subsystem $B$.

## Supporting Formulas

- Component-wise rule: $(\rho_A)_{i,i'} = \sum_j (\rho_{AB})_{(i,j),(i',j)}$ — sum over the indices of the subsystem removed
- Block-matrix rule: reshape $\rho_{AB}$ into blocks $\begin{pmatrix}B_{00}&B_{01}\\B_{10}&B_{11}\end{pmatrix}$; tracing out $B$ gives $\rho_A = B_{00}+B_{11}$
- Pure-state shortcut: with $|v_b\rangle = (I_A\otimes\langle b|)|\psi_{AB}\rangle$, $\rho_A = \sum_b |v_b\rangle\langle v_b|$
- Sanity checks on the result: Hermitian, trace 1, non-negative eigenvalues

## Derivation Outline

1. Require $\rho_A$ to reproduce the correct expectation value for any observable $O_A$ acting only on subsystem $A$.
2. Write that observable on the joint system as $O_A\otimes I_B$, so $\langle O_A\rangle=\mathrm{Tr}\big(\rho_{AB}(O_A\otimes I_B)\big)$.
3. Sum over an orthonormal basis $\{|b\rangle\}$ of $B$ to eliminate its degrees of freedom, giving $\rho_A=\sum_b(I_A\otimes\langle b|)\rho_{AB}(I_A\otimes|b\rangle)$.
4. Read off the equivalent component-wise or block-matrix rules for computing this sum in practice.
5. Check the result is Hermitian, trace 1, and positive — confirming it's a valid density matrix.

## Physical Intuition

If two qubits are entangled and you only have access to one of them, you can't write down "the state of my qubit" as a clean, definite state on its own — its fate is tangled up with a partner you can't see. But you still need some way to predict what any experiment on your qubit alone will show, and that's all the partial trace does: it's the recipe for averaging away the part of the system you don't have, in exactly the way that keeps every prediction about the part you do have correct. It's bookkeeping, not physics — nothing is "happening" to the qubit you traced out, you're just being honest that you don't know its outcome and folding that ignorance into a probability-weighted description of the qubit you kept. The reason a maximally entangled pair looks maximally random once you trace out its partner is precisely because all the information was stored in the correlation between the two, and tracing out one half throws away access to that correlation entirely.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Density Matrix](Density%20Matrix.md), [Entanglement](Entanglement.md), [Schmidt Decomposition](Schmidt%20Decomposition.md), [Entanglement Entropy](Entanglement%20Entropy.md), [Decoherence](Decoherence.md)
**Full Derivation:**
