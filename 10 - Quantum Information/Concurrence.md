---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

Concurrence is a closed-form, necessary-and-sufficient entanglement measure for two-qubit states, ranging from 0 (separable) to 1 (maximally entangled, e.g. a [Bell state](Bell%20States.md)).

## Key Equation

$$
C(\rho) = \max\{0,\ \sqrt{\lambda_1}-\sqrt{\lambda_2}-\sqrt{\lambda_3}-\sqrt{\lambda_4}\}
$$

**Derived From:** $\lambda_1\ge\lambda_2\ge\lambda_3\ge\lambda_4$, the eigenvalues of $R=\rho\,(\sigma_y\otimes\sigma_y)\,\rho^*\,(\sigma_y\otimes\sigma_y)$, where $\rho^*$ is the complex conjugate of $\rho$ in the computational basis.

## Supporting Formulas

- $C(\rho)=0 \Leftrightarrow$ separable; $C(\rho)>0 \Leftrightarrow$ entangled; $C(\rho)=1 \Leftrightarrow$ maximally entangled (e.g. [Bell States](Bell%20States.md))

## Derivation Outline

1. Form the spin-flipped state $\rho^*(\sigma_y\otimes\sigma_y)$ and combine with $\rho(\sigma_y\otimes\sigma_y)$ to build $R$.
2. Find the eigenvalues of $R$, ordered $\lambda_1\ge\lambda_2\ge\lambda_3\ge\lambda_4$.
3. Combine their square roots: $\sqrt{\lambda_1}-\sqrt{\lambda_2}-\sqrt{\lambda_3}-\sqrt{\lambda_4}$.
4. Take the max with 0 to define $C(\rho)\in[0,1]$.
5. Read off separability from the value: $C=0$ separable, $C=1$ maximally entangled (e.g. a Bell state).

## Physical Intuition

For a general, possibly noisy two-qubit state, it isn't always obvious just by looking whether entanglement is present at all, let alone how much — concurrence is the tool that turns that question into a single number you can actually compute. Feed in the state, turn the crank on a specific recipe involving the state's own mirror image under a particular symmetry operation, and out comes a number between zero and one that behaves exactly the way an entanglement measure should: zero means the state is completely separable and could have been prepared by two parties who never shared anything but classical instructions, one means it's as entangled as a Bell state can possibly be, and anything in between tells you how much of that resource survives. What makes concurrence special compared to many other entanglement diagnostics is that it's both necessary and sufficient for two-qubit states — there's no gap between "concurrence says entangled" and "actually entangled," unlike cruder tests that can only rule entanglement in or out but not both. That completeness, combined with having an explicit formula rather than requiring an open-ended search or optimization, is exactly why concurrence is the go-to measure whenever the system in question is small enough — two qubits — for it to apply.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [PPT Criterion](PPT%20Criterion.md), [Entanglement Detection](Entanglement%20Detection.md), [Bell States](Bell%20States.md)
**Full Derivation:**
