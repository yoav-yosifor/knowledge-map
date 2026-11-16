---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

A beam splitter mixes two optical modes via a [unitary](../10%20-%20Quantum%20Information/Unitary%20Quantum%20Gate.md) rotation — a reversible, information-preserving transformation — acting jointly on the two modes. In photonic [dual-rail encoding](../10%20-%20Quantum%20Information/Dual-Rail%20Encoding.md), where a qubit is represented by which of two modes a photon occupies, this is exactly how the [Hadamard Gate](../10%20-%20Quantum%20Information/Hadamard%20Gate.md) and other single-qubit rotations are physically built.

## Key Equation

$$
a_{\text{out}} = a_{\text{in}}\cos\theta + b_{\text{in}}\sin\theta, \qquad b_{\text{out}} = -a_{\text{in}}\sin\theta + b_{\text{in}}\cos\theta
$$

$$
\begin{pmatrix} a_{\text{out}} \\ b_{\text{out}} \end{pmatrix}
=
\begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix}
\begin{pmatrix} a_{\text{in}} \\ b_{\text{in}} \end{pmatrix}
$$

**Derived From:** a linear, energy-conserving (unitary) mixing of two mode operators — see [Unitary Quantum Gate](../10%20-%20Quantum%20Information/Unitary%20Quantum%20Gate.md) for the general unitarity condition this transformation satisfies.

## Supporting Formulas

- At $\theta=45°$: implements the [Hadamard Gate](../10%20-%20Quantum%20Information/Hadamard%20Gate.md)
- The matrix is exactly the classical rotation matrix $R(\theta)$ — the same object as a coordinate rotation, acting here on mode operators instead of coordinates

## Derivation Outline

1. Posit the most general linear relation between the input and output mode operators of a two-mode device.
2. Require the transformation to be unitary — preserving total photon number and the commutation relations — which restricts it to a rotation-matrix form.
3. Parametrize the rotation by a single mixing angle $\theta$.
4. Read off the beamsplitter relations for $a_{\text{out}}$ and $b_{\text{out}}$ directly from that rotation matrix.

## Physical Intuition

*Explain it without equations.*
*Write this AFTER the Feynman test — speak it out loud first, then write.*
*No LaTeX allowed here.*

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Hadamard Gate](../10%20-%20Quantum%20Information/Hadamard%20Gate.md), [Dual-Rail Encoding](../10%20-%20Quantum%20Information/Dual-Rail%20Encoding.md), [Unitary Quantum Gate](../10%20-%20Quantum%20Information/Unitary%20Quantum%20Gate.md), [Quantum Beamsplitter](Quantum%20Beamsplitter.md), [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md)
**Full Derivation:**
