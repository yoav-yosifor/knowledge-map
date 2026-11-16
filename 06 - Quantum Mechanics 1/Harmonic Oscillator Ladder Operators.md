---
tags:
  - quantum-mechanics-1
  - concept
---
---
## Core Idea

The raising and lowering (ladder) operators of the quantum harmonic oscillator step between its evenly-spaced energy eigenstates one quantum at a time, turning the problem of solving a differential equation into pure algebra on the number operator.

## Key Equation

$$
\hat a|n\rangle = \sqrt{n}\,|n-1\rangle, \qquad \hat a^\dagger|n\rangle = \sqrt{n+1}\,|n+1\rangle
$$

**Derived From:** the commutators $[\hat N,\hat a^\dagger]=\hat a^\dagger$ and $[\hat N,\hat a]=-\hat a$, which show that $\hat a|n\rangle$ is itself an eigenstate of $\hat N=\hat a^\dagger\hat a$ with eigenvalue lowered by one; normalizing that state fixes the $\sqrt n$ coefficient (and analogously for $\hat a^\dagger$).

## Supporting Formulas

- $\hat H=\hbar\omega\bigl(\hat N+\tfrac12\bigr)$, $\hat N|n\rangle=n|n\rangle$, $\hat H|n\rangle=\hbar\omega\bigl(n+\tfrac12\bigr)|n\rangle$
- $|n\rangle = \dfrac{(\hat a^\dagger)^n}{\sqrt{n!}}|0\rangle$ — every number state built from the vacuum by repeated raising
- $[\hat a,\hat a^\dagger]=1$ — the single bosonic commutation relation from which everything above follows

## Derivation Outline

1. Write the Hamiltonian in terms of the number operator, $\hat H=\hbar\omega(\hat N+\tfrac12)$, $\hat N=\hat a^\dagger\hat a$.
2. Use $[\hat N,\hat a]=-\hat a$ to show $\hat N(\hat a|n\rangle)=(n-1)(\hat a|n\rangle)$ — so $\hat a|n\rangle$ is an eigenstate of $\hat N$ with eigenvalue $n-1$.
3. Normalize $\hat a|n\rangle$ to fix its coefficient at $\sqrt n$ (and, by the analogous argument with $[\hat N,\hat a^\dagger]=\hat a^\dagger$, fix $\hat a^\dagger|n\rangle$'s coefficient at $\sqrt{n+1}$).
4. Build up every $|n\rangle$ from the vacuum $|0\rangle$ by repeated application of $\hat a^\dagger$.

## Physical Intuition

Solving the harmonic oscillator's Schrödinger equation directly, as a differential equation, is possible but clumsy. The ladder-operator trick sidesteps that entirely: instead of asking "what wavefunction has energy $E_n$," it asks "given one eigenstate, is there a simple operation that produces the next one?" The answer is yes — $\hat a^\dagger$ always adds exactly one quantum of energy and $\hat a$ always removes exactly one, never anything in between, which is only possible because the oscillator's spectrum is perfectly evenly spaced. This turns an analysis problem into pure bookkeeping: start at the bottom rung $|0\rangle$ (which $\hat a$ cannot lower any further) and climb the ladder by repeated application of $\hat a^\dagger$, with the $\sqrt n$ and $\sqrt{n+1}$ factors simply tracking the correct normalization at each rung.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Electromagnetic Field Quantization](Electromagnetic%20Field%20Quantization.md), [Photon Number States](Photon%20Number%20States.md)
**Full Derivation:**
