---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

A quantum gate is a unitary matrix acting on [qubit](Qubit.md) states. Unitarity is exactly what makes quantum evolution reversible and coherence-preserving — in contrast to classical logic gates, whose update rule is generally irreversible and can lose information.

## Key Equation

$$
U^\dagger U = I
$$

**Derived From:** the requirement that quantum evolution preserve the normalization $\langle\psi|\psi\rangle=1$ of every state it acts on.

## Supporting Formulas

- All eigenvalues have unit magnitude: $\lambda = e^{i\theta}$
- Eigenvectors can be chosen orthonormal
- Inner products are preserved: $\langle\psi|\phi\rangle = \langle U\psi|U\phi\rangle$
- Evolution is reversible: $U^{-1}=U^\dagger$
- For a single qubit, unitaries correspond (up to global phase) to rotations of the [Bloch Sphere](Bloch%20Sphere.md)
- Multi-qubit gates are unitary matrices of dimension $2^n\times 2^n$ for $n$ qubits

## Derivation Outline

1. Require any allowed quantum evolution to preserve the normalization $\langle\psi|\psi\rangle=1$ of every state it acts on.
2. Preserving all inner products, $\langle\psi|\phi\rangle=\langle U\psi|U\phi\rangle$, is exactly the condition $U^\dagger U=I$.
3. From $U^\dagger U=I$: $U$ is invertible with $U^{-1}=U^\dagger$, its eigenvalues have unit magnitude $e^{i\theta}$, and its eigenvectors can be chosen orthonormal.
4. So evolution is reversible and information-preserving — unlike classical logic gates, which can be lossy (many-to-one).

## Physical Intuition

Think of a classical logic gate like an AND gate: feed it two 1s and you get a single 1 out, but you can no longer tell what the two inputs were — information about them has been thrown away, and that's fine, because a classical bit doesn't mind being erased. A quantum gate isn't allowed to do that. It has to be a genuine one-to-one relabeling of the space of possible states, never crushing two different states down onto the same output, because if it did there would be no way to run the gate backwards and recover what you started with — and staying runnable backwards is exactly what quantum mechanics demands. That is the entire content of "unitary": not some exotic property, just the statement that the gate never discards information, so every input possibility stays distinguishable in the output, and there is always another gate that undoes it. It's why a quantum computer can't just wire up ordinary AND/OR gates and call it done — those gates are inherently lossy about information in a way quantum evolution structurally forbids.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Hadamard Gate](Hadamard%20Gate.md), [CNOT Gate](CNOT%20Gate.md), [Qubit](Qubit.md)
**Full Derivation:**
