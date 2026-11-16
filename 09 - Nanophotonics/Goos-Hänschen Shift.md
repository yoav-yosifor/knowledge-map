---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

The [phase shift picked up on total internal reflection](../05%20-%20Optics/TIR%20Phase%20Shift.md) can be pictured as if the ray had reflected from a virtual mirror, displaced beyond the real interface into the cladding or substrate. The effective bounce depth is therefore larger than the physical slab thickness.

## Key Equation

$$
d_{eff} = d + x_c + x_s
$$

**Derived From:** modeling each TIR bounce as reflection from a mirror shifted by $x_{s,c}$ into the adjacent medium; the source states $d_{eff}$ as the sum of the real thickness $d$ and the two virtual penetration depths $x_c$ (cladding side) and $x_s$ (substrate side), without deriving the mirror picture from the phase shift itself.

## Supporting Formulas

- $x_{s,c}$ are fixed by the TIR phase: $-2n_f k_0\cdot x_{s,c}\cos\theta_f + \pi = 2\phi_{TIR}$

## Derivation Outline

1. Picture each TIR bounce as reflecting off a virtual mirror displaced into the cladding/substrate rather than at the real interface.
2. Require the extra path length to that virtual mirror and back to reproduce the actual TIR phase shift, $2\phi_{TIR}$.
3. Solve $-2n_fk_0x_{s,c}\cos\theta_f+\pi=2\phi_{TIR}$ for the virtual penetration depth $x_{s,c}$.
4. Add the two penetration depths to the real thickness to get $d_{eff}=d+x_c+x_s$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [TIR Phase Shift](../05%20-%20Optics/TIR%20Phase%20Shift.md), [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md)
**Full Derivation:**
