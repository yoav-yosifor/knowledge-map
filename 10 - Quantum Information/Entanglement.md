---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Entanglement is a correlation structure that arises from the tensor-product structure of composite quantum systems. The joint state can be pure and completely known, even while neither subsystem has an independent description of its own. These correlations are genuinely quantum: they cannot be reproduced by classical shared randomness.

## Key Equation

$$
|\Psi\rangle_{AB} \neq |\psi\rangle_A \otimes |\phi\rangle_B \quad \text{for any choice of } |\psi\rangle_A, |\phi\rangle_B
$$

**Derived From:** a bipartite pure state is called separable if it factorizes as a single tensor product; entangled means no such factorization exists. See [Bell States](Bell%20States.md) for the canonical examples and [Schmidt Decomposition](Schmidt%20Decomposition.md) for the exact test.

## Supporting Formulas

- Bell states — the maximally entangled two-qubit states, see [Bell States](Bell%20States.md)
- Entanglement is detected/quantified by several criteria depending on system size — see [Entanglement Detection](Entanglement%20Detection.md)
- Reduced state of either subsystem of a maximally entangled pair is maximally mixed: $\rho_A = \rho_B = I/2$ — see [Partial Trace](Partial%20Trace.md)

## Derivation Outline

1. Define a bipartite state as separable if it factorizes: $|\Psi\rangle_{AB}=|\psi\rangle_A\otimes|\phi\rangle_B$.
2. Entangled means no such factorization exists for any choice of $|\psi\rangle_A,|\phi\rangle_B$.
3. Test this via the Schmidt Decomposition: more than one nonzero Schmidt coefficient means entangled.
4. Example: Bell states have two equal Schmidt coefficients, giving maximally mixed reduced states $\rho_A=\rho_B=I/2$.
5. Quantify or detect the degree of entanglement with criteria appropriate to system size.

## Physical Intuition

The more precisely the joint state of an entangled pair is known, the less information is available about either subsystem individually — entanglement redistributes information out of local degrees of freedom and into non-local correlations. Consider the Bell state $|\Phi^+\rangle = (|00\rangle+|11\rangle)/\sqrt2$: it is globally pure and completely specified, yet either qubit alone is described by the maximally mixed state $I/2$, with no phase information and no preference between $|0\rangle$ and $|1\rangle$. The joint system shows perfect correlations between outcomes, but each subsystem alone looks like pure noise — that apparent local randomness is missing information about correlations, not intrinsic noise. Entanglement is not communication — it is correlation structure.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Bell States](Bell%20States.md), [Partial Trace](Partial%20Trace.md), [Entanglement Detection](Entanglement%20Detection.md), [EPR Argument](EPR%20Argument.md)
**Full Derivation:**
