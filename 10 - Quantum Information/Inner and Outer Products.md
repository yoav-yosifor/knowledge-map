---
tags:
  - quantum-information
  - concept
  - technique
---
---
## Core Idea

The inner product of two kets is a complex scalar that measures their overlap. The outer product, by contrast, is an operator. A special case matters a great deal: a state's outer product with itself, $|\psi\rangle\langle\psi|$, is simultaneously a projector and the [density matrix](Density%20Matrix.md) of a pure state.

## Key Equation

$$
\langle\phi|\psi\rangle \ \text{(inner product, scalar)} \qquad\qquad |\psi\rangle\langle\phi| \ \text{(outer product, operator)}
$$

**Derived From:** basic Dirac notation — pairing a bra with a ket contracts to a scalar; pairing a ket with a bra leaves a rank-1 operator.

## Supporting Formulas

- $|\psi\rangle\langle\psi|$ is both a projector ($P^2=P$) and the pure-state density matrix

## Derivation Outline

1. Pair a bra $\langle\phi|$ with a ket $|\psi\rangle$, contracting to the scalar inner product $\langle\phi|\psi\rangle$ — an overlap measure.
2. Pair a ket $|\psi\rangle$ with a bra $\langle\phi|$ instead, leaving the rank-1 outer-product operator $|\psi\rangle\langle\phi|$.
3. Special case $\phi=\psi$: the operator $|\psi\rangle\langle\psi|$ satisfies $P^2=P$, so it is a projector onto $|\psi\rangle$.
4. That same operator is exactly the density matrix of the pure state $|\psi\rangle$.

## Physical Intuition

These two products answer two completely different questions even though they're built from the same two ingredients. Pairing a bra with a ket and contracting them down to a single number answers "how much does one state look like another" — a number close to its maximum size means the two states are nearly the same, and a number of zero means they're as different as two quantum states can be, completely distinguishable in principle. Pairing them the other way around, ket first, leaves you with something that isn't a number at all but a machine: an operator that takes any input state and pushes it toward the direction of one of the two original states. The special case where you build this machine out of a single state paired with itself is worth pausing on: this particular operator does nothing more than project anything you feed it onto that one state's direction, and applying it twice does exactly the same thing as applying it once, which is the hallmark of a projection. That same operator is also exactly how you write down the density matrix of a system that's in that one definite state with total certainty — there's no coincidence here, a pure state's density matrix really is nothing more than "project onto this direction," and the entire machinery of density matrices for uncertain or mixed states is built by averaging together many of these simple projector building blocks.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Quantum Measurement](Quantum%20Measurement.md), [Density Matrix](Density%20Matrix.md)
**Full Derivation:**
