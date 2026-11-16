---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A slab waveguide's transverse-resonance (round-trip phase-closure) condition can be satisfied by a ray at an angle below the critical angle ($\theta_f<\theta_{cr}$) — such a wave is not confined by true total internal reflection and gradually leaks power out of the guide as it propagates, rather than staying permanently trapped like a guided mode.

## Key Equation

$$
-n_fk_0d\cos\theta_f+\phi_c+\phi_s=\pi N
$$

**Derived From:** stated directly in the source as the general transverse-resonance condition for a ray in the slab — the same closure requirement used for guided modes (see [TIR Self-Consistency Derivation](TIR%20Self-Consistency%20Derivation.md)), but here evaluated without requiring $\theta_f>\theta_{cr}$.

## Supporting Formulas

- Guided waves require **two** conditions at once: total internal reflection ($\theta_f>\theta_{cr}$) *and* transverse resonance. Leaky waves satisfy resonance without TIR.
- Below the critical angle, the interface reflection coefficient $r=e^{i2\phi_c}$ is no longer unimodular (per [TIR Phase Shift](../05%20-%20Optics/TIR%20Phase%20Shift.md)), so each bounce loses some power even as the resonance condition is met.
- A leaky wave can still propagate a substantial length along the slab before leaking out, since the per-bounce loss can be small even though $|r|<1$.

## Derivation Outline

1. Require the same transverse-resonance (round-trip phase-closure) condition used to find guided modes, without assuming the ray angle exceeds the critical angle.
2. Note that below the critical angle the interface reflection coefficient is no longer unimodular, so each bounce loses some power even as the resonance condition is satisfied.
3. Conclude the wave still forms a resonant transverse pattern (a "leaky mode") but radiates away as it travels along the slab, rather than remaining perfectly confined.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md), [TIR Self-Consistency Derivation](TIR%20Self-Consistency%20Derivation.md), [TIR Phase Shift](../05%20-%20Optics/TIR%20Phase%20Shift.md)
**Full Derivation:**
