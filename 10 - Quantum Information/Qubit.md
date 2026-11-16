---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

A qubit generalizes the classical bit using quantum mechanics. Instead of a definite 0 or 1, it is any isolated two-level quantum system that can exist in a coherent [superposition](Superposition.md) of its two basis states. A global phase on that state is physically irrelevant — only the relative amplitude and phase between the two basis states affect measurement outcomes.

## Key Equation

$$
|\psi\rangle = \alpha |0\rangle + \beta |1\rangle, \qquad |\alpha|^2 + |\beta|^2 = 1
$$

**Derived From:** [Superposition](Superposition.md) applied to any two-level system, with normalization fixing the total probability to 1.

## Supporting Formulas

- A global phase $e^{i\gamma}$ on the whole state is physically irrelevant — only relative amplitude and relative phase matter
- A pure qubit state has exactly two real degrees of freedom, geometrically the [Bloch Sphere](Bloch%20Sphere.md)
- Physical realizations: spin-½ systems, photon polarization, path/time-bin encoding, superconducting circuits — the discussion is platform-independent

## Derivation Outline

1. Take a two-level quantum system and apply the [Superposition](Superposition.md) principle: $|\psi\rangle=\alpha|0\rangle+\beta|1\rangle$.
2. Normalize total probability to 1: $|\alpha|^2+|\beta|^2=1$.
3. Note a global phase $e^{i\gamma}$ on the whole state is unobservable — only relative amplitude and phase matter.
4. Geometrize the two remaining real degrees of freedom as points on the [Bloch Sphere](Bloch%20Sphere.md).

## Physical Intuition

A classical bit is a light switch: up or down, nothing in between, and asking which it is right now always has a definite answer even before you check. A qubit is more like a compass needle that's allowed to point anywhere, not just north or south — it can lean partway toward 0 and partway toward 1 at the same time, and the direction it's leaning, not just how far toward each pole, is real physical information that measurements are sensitive to. What makes this more than just "a bit with some uncertainty" is that the two amplitudes can interfere with each other, cancel or reinforce, which ordinary classical odds never do. The one thing that genuinely doesn't matter is spinning the whole needle by a common overall phase with nothing to compare it against — that's like relabeling clockwise as counterclockwise for the entire system at once, which changes no prediction at all. That's exactly why only the relative size and relative phase between the two amplitudes carries physical meaning, never the overall phase alone.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Superposition](Superposition.md), [Bloch Sphere](Bloch%20Sphere.md), [Quantization](Quantization.md)
**Full Derivation:**
