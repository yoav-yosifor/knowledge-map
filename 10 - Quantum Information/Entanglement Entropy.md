---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

For a bipartite pure state, the [von Neumann entropy](Von%20Neumann%20Entropy.md) of either reduced subsystem quantifies how much information is stored non-locally, in the correlations between the two parts. It is zero for product states and reaches its maximum, $\log d$, for maximally [entangled](Entanglement.md) states.

## Key Equation

$$
S_{\text{ent}} = S(\rho_A) = S(\rho_B), \qquad \rho_A = \mathrm{Tr}_B(|\Psi\rangle\langle\Psi|)
$$

**Derived From:** [Von Neumann Entropy](Von%20Neumann%20Entropy.md) applied to the reduced state obtained via [Partial Trace](Partial%20Trace.md); equals $S(\rho_A)$ or $S(\rho_B)$ interchangeably because both share the same nonzero eigenvalues (the squared [Schmidt Decomposition](Schmidt%20Decomposition.md) coefficients).

## Supporting Formulas

- Bell state example: $|\Phi^+\rangle=(|00\rangle+|11\rangle)/\sqrt2 \Rightarrow \rho_A=I/2 \Rightarrow S=\log2$

## Derivation Outline

1. Take a bipartite pure state $|\Psi\rangle$ and compute the reduced state $\rho_A=\mathrm{Tr}_B(|\Psi\rangle\langle\Psi|)$.
2. Apply the von Neumann entropy $S(\rho)$ to $\rho_A$.
3. Note $\rho_A$ and $\rho_B$ share the same nonzero eigenvalues (squared Schmidt coefficients), so $S(\rho_A)=S(\rho_B)$.
4. Product states give $S=0$; maximally entangled states give $S=\log d$.
5. Example: for the Bell state $|\Phi^+\rangle$, $\rho_A=I/2 \Rightarrow S=\log2$.

## Physical Intuition

Take a pair of qubits in some definite, perfectly known joint state, and ask a more local question: how much do I know about just my half, ignoring the other qubit entirely? If the two qubits were never entangled, the answer is "everything" — my half has its own definite state, and looking at it tells the full story. But if the pair is entangled, my half, considered alone, looks like a genuinely mixed, uncertain state, even though the pair together is perfectly pure and perfectly known. Entanglement entropy is just the ordinary measure of that local uncertainty, applied to one half of an entangled pair, and the striking thing is that its value doesn't depend on any actual ignorance about the world — the full joint state is completely specified — it's purely a bookkeeping consequence of information having been pushed out of each individual qubit and into the correlations between them. The more of that redistribution has happened, the larger the local uncertainty, until you hit the maximum possible entropy exactly when the pair is maximally entangled, at which point either qubit alone looks as uncertain as a fair coin flip. In this sense entanglement entropy is doing double duty: it measures your ignorance about a subsystem, but for a globally pure state that ignorance is entirely a measure of how strongly entangled the two parts are with each other.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Von Neumann Entropy](Von%20Neumann%20Entropy.md), [Schmidt Decomposition](Schmidt%20Decomposition.md), [Partial Trace](Partial%20Trace.md), [Entanglement](Entanglement.md)
**Full Derivation:**
