---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The 3-qubit bit-flip code protects one logical qubit against a single [bit-flip error](Bit-Flip%20Channel.md) by encoding it redundantly across three physical qubits. The error is then detected through parity (stabilizer) measurements, which reveal which qubit flipped without ever learning the encoded amplitudes.

## Key Equation

$$
|0_L\rangle = |000\rangle, \quad |1_L\rangle = |111\rangle, \qquad a|0\rangle+b|1\rangle \to a|000\rangle+b|111\rangle
$$

**Derived From:** repetition encoding across three qubits, chosen so that a single [Bit-Flip Channel](Bit-Flip%20Channel.md) error on any one qubit can be identified and undone without collapsing $a,b$.

## Supporting Formulas

- Syndrome measurement: stabilizers $Z_1Z_2, Z_2Z_3$ commute and, without collapsing the logical state, uniquely identify: no error, or an error on qubit 1, 2, or 3
- Recovery: apply $X$ to the erroneous qubit to restore the encoded state exactly
- Success condition: $p < \tfrac12$ (error probability per qubit)

## Derivation Outline

1. Encode the logical qubit redundantly: $a|0\rangle+b|1\rangle \to a|000\rangle+b|111\rangle$
2. Measure the stabilizers $Z_1Z_2$ and $Z_2Z_3$ — this reveals the error location, not $a,b$
3. Apply the corresponding $X$ correction to recover the original encoded state

## Physical Intuition

Think of the classical trick of writing a message three times and taking a majority vote to catch a typo — the bit-flip code is the quantum version of that idea, adapted to survive a constraint classical error correction never has to worry about: you're not allowed to look at the message to check it, because looking would destroy the very superposition you're trying to protect. The fix is to spread the logical zero and one across three physical qubits in lockstep, so that a single accidental flip on any one of them leaves the other two still agreeing with each other. Instead of reading out each qubit directly, you only ask indirect yes/no questions like "do qubits one and two agree" and "do qubits two and three agree" — these parity checks can be answered without ever revealing what the actual encoded amplitudes are, so the fragile quantum information underneath stays completely untouched. The pattern of answers to those two questions acts like a fingerprint that points unambiguously at which single qubit, if any, got flipped, and once you know that, undoing a bit flip is trivial — you just flip it back. The whole scheme only works, of course, if flips are rare enough that you can trust "one flip" is far more likely than "two," which is exactly the regime real physical qubits are built to sit in.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Bit-Flip Channel](Bit-Flip%20Channel.md), [Phase-Flip Code](Phase-Flip%20Code.md), [Shor Code](Shor%20Code.md), [No-Cloning Theorem](No-Cloning%20Theorem.md)
**Full Derivation:**
