---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Any pure [qubit](Qubit.md) state maps to a unique point on the surface of a sphere, called the Bloch sphere. The states $|0\rangle$ and $|1\rangle$ sit at the poles, and the polar and azimuthal angles encode the population balance and relative phase between them. [Mixed states](Pure%20vs%20Mixed%20States.md) extend this picture further, corresponding to points inside the sphere described by the Bloch vector.

## Key Equation

$$
|\psi\rangle = \cos\!\left(\tfrac{\theta}{2}\right)|0\rangle + e^{i\phi}\sin\!\left(\tfrac{\theta}{2}\right)|1\rangle
$$

**Derived From:** the general qubit state $\alpha|0\rangle+\beta|1\rangle$ with global phase removed and normalization imposed — the remaining two real parameters $(\theta,\phi)$ are exactly spherical coordinates.

## Supporting Formulas

- Bloch vector (density matrix form): $\rho = \tfrac{1}{2}(I + \vec r \cdot \vec\sigma)$, with $\vec\sigma = (X,Y,Z)$
- $|\vec r| = 1 \Leftrightarrow$ pure state (surface); $|\vec r| < 1 \Leftrightarrow$ mixed state (interior)
- Eigenvalues of $\rho$: $\lambda_\pm = \tfrac12(1 \pm |\vec r|)$
- The eigenstates of the Pauli matrices lie along the $x$, $y$, $z$ axes of the sphere

## Derivation Outline

1. Start from the general qubit state $\alpha|0\rangle+\beta|1\rangle$ (two complex amplitudes).
2. Remove the unobservable global phase, leaving three real parameters.
3. Impose normalization $|\alpha|^2+|\beta|^2=1$, leaving exactly two real parameters.
4. Identify those two parameters as spherical angles $(\theta,\phi)$ — pure states become points on the unit sphere.
5. Extend to mixed states via $\rho=\tfrac12(I+\vec r\cdot\vec\sigma)$: $|\vec r|<1$ gives interior points, with eigenvalues $\lambda_\pm=\tfrac12(1\pm|\vec r|)$.

## Physical Intuition

Every pure state of a single qubit can be drawn as an arrow from the center of a ball out to a point on its surface — 0 and 1 sit at the north and south poles, and every other point on the surface is some specific balance of the two plus a specific relative phase between them, so the whole family of qubit states becomes something you can literally point at. States that are maximally uncertain about their own identity — a fully mixed state, a classical 50/50 coin flip with no coherence at all — sit exactly at the center of the ball, as far as possible from any pole. States that are somewhere between a clean superposition and total classical ignorance live at intermediate radius: the shorter the arrow, the more the state behaves like a probabilistic mixture rather than a genuine coherent superposition. This picture is more than decoration — it means every single-qubit operation, however it's built out of gates, is literally just a rotation of this ball, so questions like "do these two gates commute" become questions about whether two rotation axes commute, which is often easier to see geometrically than to work out algebraically.

## Isomorphisms

- Single-qubit unitaries (Bloch-sphere rotations) are the same compact SU(2) rotation group as linear optics' photon-number-conserving transformations (phase shifters and beamsplitters) — see [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md) and the [Isomorphism Log](../00%20-%20Index/Isomorphism%20Log.md).

## Open Questions

- [ ]

---

## Links

**Related:** [Qubit](Qubit.md), [Pure vs Mixed States](Pure%20vs%20Mixed%20States.md), [Density Matrix](Density%20Matrix.md)
**Full Derivation:**
