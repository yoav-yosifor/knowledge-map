---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

In a [Lambda three-level system](Three-Level%20Atom%20Configurations.md), a particular superposition of the two ground states has exactly zero excited-state amplitude by construction. That means it is completely decoupled from both laser fields: an atom prepared in this "dark state" cannot absorb or scatter light at all. This is the basis of coherent population trapping and, when the fields are varied slowly, of loss-free population transfer ([STIRAP](STIRAP.md)).

## Key Equation

$$
|D\rangle = \frac{\Omega_2^*\,|1\rangle - \Omega_1^*\,|2\rangle}{\sqrt{|\Omega_1|^2+|\Omega_2|^2}}
$$

**Derived From:** diagonalizing the Lambda-system RWA Hamiltonian at two-photon resonance ($\Delta_1=\Delta_2=0$), where the characteristic polynomial factors as $-\lambda(\lambda^2-|\Omega_1|^2-|\Omega_2|^2)=0$, giving one zero eigenvalue $\lambda_0=0$ in addition to the two bright eigenvalues $\lambda_\pm=\pm\tfrac{\hbar}{2}\sqrt{|\Omega_1|^2+|\Omega_2|^2}$ — see [Three-Level Atom Configurations](Three-Level%20Atom%20Configurations.md).

## Supporting Formulas

- Decoupling condition: $H_\text{AL}|D\rangle=0$ — the dark state is annihilated by the light-atom coupling because the coupling Hamiltonian only ever connects ground states to the excited state, and the dark state's excited-state component is exactly zero
- Bright states (the other two eigenstates) do contain excited-state amplitude and undergo Rabi oscillations at the combined generalized Rabi frequency $\sqrt{|\Omega_1|^2+|\Omega_2|^2}$
- Limiting cases: $\Omega_1=0,\Omega_2\neq0 \Rightarrow |D\rangle=|1\rangle$; $\Omega_1\neq0,\Omega_2=0 \Rightarrow |D\rangle=|2\rangle$; $\Omega_1=\Omega_2 \Rightarrow |D\rangle=(|1\rangle-|2\rangle)/\sqrt2$ — these limits are what let the dark state rotate continuously from $|1\rangle$ to $|2\rangle$ as the two Rabi frequencies are varied, the mechanism exploited in [STIRAP](STIRAP.md)
- Coherent population trapping (CPT): at two-photon resonance the dark state is a steady-state solution of the full open-system (Lindblad) dynamics — population accumulates in $|D\rangle$ and stays there, immune to the excited state's decay

## Derivation Outline

1. Set both single-photon detunings to zero (two-photon/Raman resonance) in the Lambda RWA Hamiltonian.
2. Solve the characteristic equation for the eigenvalues; one root is exactly zero regardless of the values of $\Omega_1,\Omega_2$.
3. Solve the eigenvector equation for this zero eigenvalue; because the Hamiltonian only connects the excited state to the two ground states, the zero-eigenvalue eigenvector is forced to have zero excited-state component, leaving only a superposition of the two ground states.

## Physical Intuition

Even though both lasers are shining on the atom and both are, individually, perfectly capable of driving a transition, there exists one very particular combination of the two ground states for which the two possible excitation pathways — via laser 1 or via laser 2 — destructively interfere and exactly cancel. An atom sitting in that special combination is, in effect, invisible to both lasers at once, even though neither laser has been turned off and both are resonant. This is not a coincidence of weak coupling; it is an exact structural feature of having two paths that can interfere. Because the dark state contains no excited-state population, it also completely sidesteps the "leaky bucket" problem of spontaneous decay — there's no amplitude in the leaky state to lose. If the relative strengths of the two lasers are then changed slowly enough, the identity of "which combination of ground states currently forms the dark state" smoothly rotates, and an atom that starts out riding the dark state can be steered from one ground state fully into the other while never once populating the lossy excited state along the way.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Three-Level Atom Configurations](Three-Level%20Atom%20Configurations.md), [STIRAP](STIRAP.md), [Adiabatic Approximation](Adiabatic%20Approximation.md)
**Full Derivation:**
