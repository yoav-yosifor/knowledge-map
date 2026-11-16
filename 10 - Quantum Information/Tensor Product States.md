---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

The joint Hilbert space of two quantum systems is the tensor product of their individual Hilbert spaces. If each subsystem is prepared independently, the joint state is simply the tensor product of the two individual states. But this structure is exactly what makes [entanglement](Entanglement.md) possible, since not every joint state factorizes this way.

## Key Equation

$$
\mathcal{H}_{AB} = \mathcal{H}_A \otimes \mathcal{H}_B, \qquad |\Psi\rangle = |\psi\rangle_A \otimes |\phi\rangle_B \ \text{(product state case)}
$$

**Derived From:** composing two independent quantum systems — the postulate that joint states live in the tensor-product space, not the (smaller) direct-sum / Cartesian-product space.

## Supporting Formulas

- Computational basis for two qubits: $\{|00\rangle,|01\rangle,|10\rangle,|11\rangle\}$, with $|ij\rangle \equiv |i\rangle_A\otimes|j\rangle_B$
- General two-qubit pure state: $|\Psi\rangle = c_{00}|00\rangle+c_{01}|01\rangle+c_{10}|10\rangle+c_{11}|11\rangle$, $\sum|c_{ij}|^2=1$
- Product density matrix: $\rho_{AB}=\rho_A\otimes\rho_B$

## Derivation Outline

1. Postulate that the joint Hilbert space of two systems is $\mathcal{H}_{AB}=\mathcal{H}_A\otimes\mathcal{H}_B$, not a smaller Cartesian-product-like space.
2. If the two systems are prepared independently, their joint state is simply the product $|\psi\rangle_A\otimes|\phi\rangle_B$.
3. Build the two-qubit computational basis as $|ij\rangle\equiv|i\rangle_A\otimes|j\rangle_B$, giving the general state $\sum c_{ij}|ij\rangle$.
4. Note the tensor-product space also contains superpositions of basis states that do not factorize into any single $|\psi\rangle_A\otimes|\phi\rangle_B$ — these are the entangled states.

## Physical Intuition

When you bring two separate quantum systems together and want to describe them as one combined system, quantum mechanics doesn't just let you list what each one is doing side by side the way you might for two independent classical variables — it demands a much larger space of possibilities, built by combining every basis state of the first system with every basis state of the second. If the two systems really were prepared completely independently of each other, with no correlation whatsoever, then their combined description is simple: you just plug each one's own state into its own slot in this combined space, and the result is the tensor product of the two, a state that still lets you say something definite about each half on its own. But the whole point of building this larger combined space, rather than something smaller, is that it also contains states that cannot be pulled apart this way — states where, no matter how you try to write it, you cannot assign a separate, independent description to each half. Those non-factorizing states are entangled states, and their existence is a direct structural consequence of how quantum systems are required to combine: the joint space is big enough to hold not just every simple, independently-prepared pairing, but every possible superposition of them too, and most of those superpositions simply don't correspond to any two individually well-defined states at all.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Entanglement](Entanglement.md), [Density Matrix](Density%20Matrix.md)
**Full Derivation:**
