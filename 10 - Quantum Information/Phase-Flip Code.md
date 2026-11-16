---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Phase-flip errors (a $Z$ rather than $X$ error) become ordinary bit-flip errors once you rotate into the Hadamard basis. So the phase-flip code is just the [Bit-Flip Code](Bit-Flip%20Code.md) conjugated by [Hadamard gates](Hadamard%20Gate.md).

## Key Equation

$$
|+\rangle = \frac{|0\rangle+|1\rangle}{\sqrt2}, \qquad |-\rangle = \frac{|0\rangle-|1\rangle}{\sqrt2}, \qquad |+\rangle \leftrightarrow |-\rangle \ \text{under a phase flip}
$$

**Derived From:** applying [Hadamard Gate](Hadamard%20Gate.md) to map the $Z$-error problem onto an $X$-error problem, then reusing the [Bit-Flip Code](Bit-Flip%20Code.md) machinery.

## Supporting Formulas

- Procedure: rotate to the Hadamard basis → apply the bit-flip code → rotate back

## Derivation Outline

1. Note a phase-flip ($Z$) error swaps $|+\rangle\leftrightarrow|-\rangle$ while leaving $|0\rangle,|1\rangle$ untouched — invisible in the computational basis.
2. Apply [Hadamard Gate](Hadamard%20Gate.md)s to rotate into the $|+\rangle,|-\rangle$ basis, where this same error now acts as an ordinary bit flip.
3. Encode and correct using the standard [Bit-Flip Code](Bit-Flip%20Code.md) machinery in this rotated basis.
4. Rotate back with Hadamard gates to return to the original basis, having corrected the phase flip.

## Physical Intuition

A phase-flip error is a strange kind of mistake because it doesn't touch the zero-or-one label of a qubit at all — a zero stays a zero and a one stays a one — it only flips the relative sign between the two halves of a superposition, which is invisible if you only ever check the qubit in its usual zero-one basis. But that same sign flip looks like a completely ordinary bit flip if you first change your point of view: switch to describing the qubit in terms of its plus and minus superposition states instead of zero and one, and a phase error swaps "plus" into "minus" exactly the same way an ordinary bit-flip error swaps zero into one. Since the Hadamard gate is precisely the tool that converts back and forth between these two ways of describing a qubit, you can protect against phase errors with zero new machinery: rotate the qubit into the plus-minus description with a Hadamard gate, run the exact same bit-flip error-correcting code you'd already built for ordinary bit flips, then rotate back. It's the same protection, just viewed through a different lens — proof that phase errors and bit errors aren't two separate problems requiring two separate inventions, they're the same problem in two different bases.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Bit-Flip Code](Bit-Flip%20Code.md), [Hadamard Gate](Hadamard%20Gate.md), [Shor Code](Shor%20Code.md)
**Full Derivation:**
