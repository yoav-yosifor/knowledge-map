---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Decoherence is the loss of quantum coherence: the disappearance of interference terms between amplitudes. It happens when a system becomes entangled with its environment. The result is that a [pure state turns into a mixed state](Pure%20vs%20Mixed%20States.md), with no measurement required.

## Key Equation

$$
\rho_{\text{sys}} = \mathrm{Tr}_{\text{env}}(\rho_{\text{sys+env}})
$$

**Derived From:** the system entangles with the environment, $|\Psi\rangle = |\psi\rangle\otimes|e_0\rangle \to \sum_i \psi_i|i\rangle\otimes|e_i\rangle$; tracing out the environment (see [Partial Trace](Partial%20Trace.md)) leaves the system in a mixed state.

## Supporting Formulas

- After tracing out the environment: $\rho_{\text{sys}} = \sum_i |\psi_i|^2 |i\rangle\langle i|$ — off-diagonal (coherence) terms vanish
- Information has leaked into correlations with the environment, not been destroyed
- See [Einselection](Einselection.md) for why a specific basis emerges

## Derivation Outline

1. System starts in a superposition $|\psi\rangle=\sum_i\psi_i|i\rangle$, environment in a fixed reference state $|e_0\rangle$.
2. Interaction correlates them: $|\psi\rangle\otimes|e_0\rangle \to \sum_i\psi_i|i\rangle\otimes|e_i\rangle$.
3. Take the partial trace over the environment: $\rho_{\text{sys}}=\mathrm{Tr}_{\text{env}}(\rho_{\text{sys+env}})$.
4. If the environmental branches $|e_i\rangle$ are distinguishable, off-diagonal (coherence) terms vanish, leaving $\rho_{\text{sys}}=\sum_i|\psi_i|^2|i\rangle\langle i|$.
5. The pure state has become mixed with no measurement performed — the interference terms are now hidden in system-environment correlations.

## Physical Intuition

A superposition is fragile in a very specific sense: it only shows its quantum character — interference, the ability for two paths to cancel or reinforce — as long as nothing else in the universe has "noticed" which path was taken. The moment a qubit interacts with its environment (a stray photon, a phonon in the crystal it sits in, anything at all) in a way that depends on the qubit's state, the environment has effectively recorded which-path information, whether or not any human ever reads that record. From that point on, the interference terms that made the superposition special are still there in principle, but they're now spread out across correlations with an environment nobody has access to — and once you average over an environment you can't see, those interference terms wash out completely, leaving something that looks and behaves just like a classical, already-decided coin flip. Nobody had to measure anything for this to happen: decoherence is the environment measuring the system whether you wanted it to or not, and it's the practical reason building a quantum computer means fighting an unrelenting battle against stray interactions with the outside world.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Einselection](Einselection.md), [Pure vs Mixed States](Pure%20vs%20Mixed%20States.md), [Kraus Operator Representation](Kraus%20Operator%20Representation.md)
**Full Derivation:**
