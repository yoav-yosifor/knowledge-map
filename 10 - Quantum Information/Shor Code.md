---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The Shor code protects a logical qubit against any single-qubit error: bit-flip, phase-flip, or both. It works by nesting the [Bit-Flip Code](Bit-Flip%20Code.md) inside the [Phase-Flip Code](Phase-Flip%20Code.md) — first protecting against phase flips, then protecting each resulting qubit against bit flips. This uses 9 physical qubits in total.

## Key Equation

$$
|0_L\rangle = \frac{(|000\rangle+|111\rangle)^{\otimes3}}{2\sqrt2}, \qquad
|1_L\rangle = \frac{(|000\rangle-|111\rangle)^{\otimes3}}{2\sqrt2}
$$

**Derived From:** encoding each of the three blocks of a phase-flip code using the bit-flip code, nesting the two three-qubit codes.

## Supporting Formulas

- Any single-qubit error decomposes as $E = \alpha I + \beta X + \gamma Y + \delta Z$; since $Y=iXZ$, bit and phase errors are correctable independently
- Syndrome measurement collapses the error into a discrete Pauli error, which is then corrected

## Derivation Outline

1. Protect against phase flips first (outer code)
2. Protect each resulting qubit against bit flips (inner code)
3. Any single-qubit error, expanded in the Pauli basis, reduces to independently correctable bit and phase components

## Physical Intuition

A single qubit can go wrong in only a handful of independent ways: it can flip like a classical bit, it can suffer a purely quantum kind of damage that scrambles its phase without touching which basis state it's in, it can suffer both at once, or nothing happens at all. Ordinary error-correcting codes handle bit flips well, using redundancy across several copies to vote out a wrong answer, but phase damage is invisible to that kind of code because it doesn't show up as a flipped value in the bit-flip basis at all — it only shows up if you look in the complementary basis. The Shor code's trick is to protect against phase damage first, by spreading one logical qubit's information across three blocks in a way that makes phase errors on any single block detectable and correctable, and then, because each of those three blocks is still just an ordinary qubit vulnerable to bit flips, to protect each one again using the simpler bit-flip method underneath. Because any possible single-qubit error can always be broken down into some combination of a bit flip, a phase flip, or both together, having independent machinery to catch each piece separately is enough to catch every possible single-qubit error, however it's combined. The cost of this two-layer protection is that one logical qubit now needs nine physical qubits to carry it — three blocks of three — and a syndrome measurement step to figure out, without ever looking at the encoded information itself, exactly which of the possible errors occurred so it can be undone.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Bit-Flip Code](Bit-Flip%20Code.md), [Phase-Flip Code](Phase-Flip%20Code.md)
**Full Derivation:**
