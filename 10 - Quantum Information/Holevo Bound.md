---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The Holevo bound caps how much classical information can actually be extracted from an ensemble of quantum states by [measurement](Quantum%20Measurement.md). No matter how clever the measurement, the accessible classical information can never exceed the Holevo quantity. For a $d$-dimensional system, that means it can never exceed $\log d$ bits.

## Key Equation

$$
\chi = S(\rho) - \sum_x p_x S(\rho_x), \qquad \rho=\sum_x p_x \rho_x, \qquad I(X:Y) \le \chi
$$

**Derived From:** Alice encodes classical value $x$ (probability $p_x$) into quantum state $\rho_x$ and sends it; Bob measures and obtains classical outcome $Y$. $\chi$ is the gap between the entropy of the ensemble average $\rho$ and the average entropy of the individual code states — it upper-bounds the classical mutual information $I(X:Y)$ Bob can extract, optimized over all possible measurements.

## Supporting Formulas

- Pure-state encoding: all $\rho_x$ pure $\Rightarrow S(\rho_x)=0 \Rightarrow \chi = S(\rho)$
- Commuting (classical-like) encoding: bound achieved by measuring in the common eigenbasis
- Non-commuting encoding: no single measurement optimally distinguishes all states — some encoded information is fundamentally inaccessible
- Dimensional limit: $\chi \le \log d$; for $n$ qubits, $\chi \le n$ bits — $n$ qubits cannot transmit more than $n$ accessible classical bits per use without extra resources
- [Superdense Coding](Superdense%20Coding.md) surpasses "1 qubit → 1 bit" using pre-shared entanglement as an additional resource, without violating Holevo (the resource model has changed)

## Derivation Outline

1. Alice encodes classical value $x$ (probability $p_x$) into quantum state $\rho_x$; the ensemble average is $\rho=\sum_x p_x\rho_x$.
2. Define $\chi=S(\rho)-\sum_x p_x S(\rho_x)$, the entropy gap between the ensemble average and the average individual state.
3. Bob measures and obtains outcome $Y$; for any measurement, $I(X:Y)\le\chi$.
4. If the $\rho_x$ commute, the bound is achieved by measuring in the common eigenbasis; if not, some encoded information is fundamentally inaccessible.
5. For a $d$-dimensional system, $\chi\le\log d$, so $n$ qubits carry at most $n$ accessible classical bits per use without extra resources (e.g. shared entanglement, as in superdense coding).

## Physical Intuition

Imagine Alice trying to smuggle a classical message into Bob's hands by encoding it into quantum states rather than sending the classical bits directly — you might hope that because a quantum state can be built out of a continuum of possible directions, she could pack in an enormous amount of information per particle. The Holevo bound says: not so fast. However cleverly Alice chooses her code states, and however cleverly Bob designs his measurement, the amount of the original message he can actually recover is capped by a single number that only depends on how distinguishable, on average, her code states are from each other — and if those code states don't all commute with one another, meaning they can't all be perfectly told apart by any single measurement, some of what Alice tried to encode is not just hard to extract, it is gone for good, lost to the fact that measurement forces a choice of basis. The bound tightens to its simplest form when the code states are literally the same as classical labels: then there's no penalty and Bob recovers everything. This is why a single qubit, no matter how you dress it up, cannot be made to carry more than one reliable classical bit of information per use — that ceiling can only be lifted by bringing in an entirely different resource, like a shared entangled pair, which changes what's being asked of the qubit rather than breaking the bound itself.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Von Neumann Entropy](Von%20Neumann%20Entropy.md), [Superdense Coding](Superdense%20Coding.md), [Quantum Measurement](Quantum%20Measurement.md)
**Full Derivation:**
