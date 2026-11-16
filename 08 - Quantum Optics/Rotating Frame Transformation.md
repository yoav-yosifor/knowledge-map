---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

A rotating-frame transformation is an **exact** change of representation, not an approximation: it re-describes the state relative to a basis that itself rotates in time, stripping out whatever fast, shared phase evolution is common to the whole relevant subspace so that only the physically meaningful *relative* dynamics — detuning, coupling, relative phase — remain visible. It is usually the necessary first step before applying the [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), which only discards terms once they've been sorted into slow and fast by this transformation.

## Key Equation

$$
\hat H_\text{rot} = U\hat H U^\dagger + i\hbar\dot U U^\dagger
$$

**Derived From:** demanding that the transformed state $|\psi_\text{rot}(t)\rangle=U(t)|\psi(t)\rangle$ obey its own Schrödinger equation $i\hbar\partial_t|\psi_\text{rot}\rangle=\hat H_\text{rot}|\psi_\text{rot}\rangle$; substituting $|\psi\rangle=U^\dagger|\psi_\text{rot}\rangle$ into the original equation $i\hbar\partial_t|\psi\rangle=\hat H|\psi\rangle$ and applying the product rule to $\partial_t(U^\dagger|\psi_\text{rot}\rangle)$ produces an extra "frame-drag" term $i\hbar\dot U U^\dagger$ on top of the naively-rotated Hamiltonian $U\hat HU^\dagger$ — exactly analogous to the fictitious centrifugal/Coriolis terms that appear when writing Newton's second law in a rotating classical reference frame.

## Supporting Formulas

- **Global-phase removal:** if $\hat H=\hat H'+C(t)I$ with $C$ common to the *entire relevant Hilbert space* and $C$ constant, then $e^{-i\hat Ht/\hbar}=e^{-iCt/\hbar}e^{-i\hat H't/\hbar}$, so the state only picks up an overall phase $e^{-iCt/\hbar}$ — this changes neither probabilities $|\langle a|\psi(t)\rangle|^2$ nor expectation values $\langle\psi(t)|\hat O|\psi(t)\rangle$, so $\hat H\to\hat H-CI$ is safe and equivalent to choosing a different zero of energy.
- **Worked block example (Jaynes-Cummings subspace $\{|e,n\rangle,|g,n+1\rangle\}$):** $\hat H_n=\hbar(n+1)\omega_L I+\hbar\begin{pmatrix}-\Delta & g\sqrt{n+1}\\g\sqrt{n+1} & 0\end{pmatrix}$, with $\Delta=\omega_L-\omega_a$. The $\hbar(n+1)\omega_LI$ piece is common to both states in the block, so it is a global phase and drops out, leaving $\hat H_n^{(\text{rot})}=\hbar\begin{pmatrix}-\Delta & g\sqrt{n+1}\\g\sqrt{n+1} & 0\end{pmatrix}$ — detuning, coupling, and relative phase survive; only the shared carrier phase is removed. See [RWA Rotating-Frame Derivation](RWA%20Rotating-Frame%20Derivation.md) for the equivalent single-atom worked case.
- **Block caveat:** dropping $C_nI$ is only safe *within one fixed block*. If the physical state is a superposition across blocks with different constants, $|\psi\rangle=\alpha|\psi_n\rangle+\beta|\psi_m\rangle$ with $C_n\neq C_m$, the two blocks pick up different phases $e^{-iC_nt/\hbar}\neq e^{-iC_mt/\hbar}$; their difference is a genuine *relative* phase and is physical. In that situation, terms cannot simply be deleted block by block — a proper unitary rotating-frame transformation must be used instead.

## Derivation Outline

1. Define the rotating-frame state $|\psi_\text{rot}(t)\rangle=U(t)|\psi(t)\rangle$ for a time-dependent unitary $U(t)$ chosen to track the system's known fast oscillation (e.g. $U=e^{i\omega_Lt|e\rangle\langle e|}$ to rotate at the laser frequency).
2. Substitute into the Schrödinger equation and use the product rule to isolate the extra frame-drag term $i\hbar\dot UU^\dagger$, arriving at the general transformation law above.
3. Apply it to a Hamiltonian containing a term $C(t)I$ shared across the whole relevant subspace: show algebraically that it produces only a global phase factor and can be dropped without changing any observable prediction.
4. Confirm what survives: relative energy differences (the detuning $\Delta$), couplings ($g\sqrt{n+1}$, Rabi frequencies), and relative phases between different basis states all remain fully present in $\hat H_\text{rot}$ — only the fast carrier phase shared by the whole subspace has been removed.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [RWA Rotating-Frame Derivation](RWA%20Rotating-Frame%20Derivation.md), [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md)
**Full Derivation:** [RWA Rotating-Frame Derivation](RWA%20Rotating-Frame%20Derivation.md)
