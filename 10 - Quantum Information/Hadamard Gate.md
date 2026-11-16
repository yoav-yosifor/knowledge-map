---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

The Hadamard gate is the fundamental single-qubit gate that maps computational basis states into equal superpositions — physically analogous to a 50-50 [beam splitter](Beam%20Splitter%20Transformation.md) in a Mach-Zehnder interferometer.

## Key Equation

$$
H = \frac{1}{\sqrt2}\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}
$$

**Derived From:** a [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md) chosen so that it maps $|0\rangle,|1\rangle$ to equal-weight superpositions and squares to the identity.

## Supporting Formulas

- $H^2 = I$ — applying it twice restores the original state
- Photonic realization: implemented by a physical [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), $|0\rangle \to (|0\rangle+|1\rangle)/\sqrt2$

## Derivation Outline

1. Require a unitary that maps $|0\rangle$ and $|1\rangle$ each to equal-weight superpositions of $|0\rangle,|1\rangle$.
2. Require the operation to be its own inverse: $H^2=I$.
3. Solving these constraints gives $H=\tfrac{1}{\sqrt2}\begin{pmatrix}1&1\\1&-1\end{pmatrix}$.
4. Photonically, realize $H$ as a 50-50 beam-splitter transformation: $|0\rangle\to(|0\rangle+|1\rangle)/\sqrt2$.

## Physical Intuition

Think of a beam of light hitting a half-silvered mirror: it doesn't choose to go one way or the other, it splits into an equal-weight combination of both paths, and that's exactly the job the Hadamard gate does for a qubit sitting in a definite state — it takes something that's completely decided ("this qubit is a zero") and turns it into something completely undecided, an equal mixture of possibilities held together with a definite phase relationship rather than a fifty-fifty coin flip. The reason it's built to square to the identity is the same reason running a beam of light through two identical half-silvered mirrors in a row can bring it right back to where it started, or send it somewhere else entirely, depending on how the two paths recombine — apply the gate twice and the two superpositions interfere with each other in just the right way to undo the first step exactly. That reversibility isn't a coincidence, it's a requirement: any legitimate quantum gate has to be undoable, and the Hadamard gate is the simplest one whose whole purpose is to convert perfectly certain information into perfectly balanced uncertainty and back again. That's also why it shows up constantly at the start of quantum algorithms — it's the standard way of putting a qubit into an equal superposition so that later steps have both possibilities to interfere with.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Unitary Quantum Gate](Unitary%20Quantum%20Gate.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md)
**Full Derivation:**
