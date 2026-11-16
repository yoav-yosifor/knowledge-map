---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Quantum measurement is modeled as projection onto an eigenbasis of an observable. Outcomes are intrinsically probabilistic, and the act of measuring changes the state. The choice of measurement basis even determines what information is accessible at all. This is why quantum circuits postpone measurement until the very end.

## Key Equation

$$
p(k) = \langle\psi|P_k|\psi\rangle \qquad \text{(state vector form, Born rule)}
\qquad\qquad
p(k) = \mathrm{Tr}(P_k\,\rho) \qquad \text{(density matrix form, works in all cases)}
$$

**Derived From:** the projection postulate — $P_k = |k\rangle\langle k|$ projects onto outcome $k$; the Born rule gives the probability of that outcome as the expectation value of $P_k$.

## Supporting Formulas

- Projection operators satisfy $P^2 = P$, are Hermitian but not unitary — measurement is irreversible where unitary evolution is not
- Post-measurement state (state vector): $|\psi_k\rangle = \dfrac{P_k|\psi\rangle}{\sqrt{p(k)}}$
- Post-measurement state (density matrix): $\rho_k = \dfrac{P_k\,\rho\,P_k}{p(k)}$, reducing to the vector rule when $\rho=|\psi\rangle\langle\psi|$
- The special case $|\psi\rangle\langle\psi|$ is simultaneously a projector and the density matrix of a pure state

## Derivation Outline

1. Posit a projection operator $P_k=|k\rangle\langle k|$ for each possible measurement outcome $k$.
2. Apply the Born rule: $p(k)=\langle\psi|P_k|\psi\rangle$ (or $\mathrm{Tr}(P_k\rho)$ for mixed states).
3. Collapse to the post-measurement state: $|\psi_k\rangle=P_k|\psi\rangle/\sqrt{p(k)}$ (or $\rho_k=P_k\rho P_k/p(k)$).
4. Note $P_k$ is Hermitian and idempotent but not unitary ⇒ measurement is irreversible, unlike unitary evolution.
5. Since measurement destroys coherence, quantum circuits defer it to the very end.

## Physical Intuition

Measurement ends coherent processing: once you measure, quantum information becomes classical information, and premature measurement destroys interference. This is exactly why quantum algorithms are built to delay all measurement to the end of the circuit.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Density Matrix](Density%20Matrix.md), [Qubit](Qubit.md)
**Full Derivation:**
