---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The discrete guided-mode condition for a [slab waveguide](Slab%20Waveguide%20Modes.md), obtained from requiring that a ray bouncing back and forth by [total internal reflection](../05%20-%20Optics/TIR%20Phase%20Shift.md) accumulates a total round-trip phase equal to an integer multiple of $2\pi$.

## Starting Point

- A ray of core index $n_f$ propagates at angle $\theta_f$ inside a slab of thickness $d$ (core $|x|<d/2$), bouncing between the substrate interface ($x=-d/2$) and cladding interface ($x=d/2$) by total internal reflection — the same symmetric-slab convention used in [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md).
- Each bounce imprints a [TIR phase shift](../05%20-%20Optics/TIR%20Phase%20Shift.md): $\phi_s$ at the substrate interface, $\phi_c$ at the cladding interface.

## Full Derivation

1. **Write the field at the substrate interface ($x=-d/2$).**

   $$
   E(x=-d/2) \propto e^{-i k_0 n_f\left(-\tfrac d2\cos\theta_f + z\sin\theta_f\right)}
   $$

   This is just the propagating-wave phase along $z$ for a ray tilted at $\theta_f$, evaluated at the lower boundary.

2. **Write the field at the cladding interface ($x=d/2$).**

   $$
   E(x=d/2) \propto e^{-i k_0 n_f\left(\tfrac d2\cos\theta_f + z\sin\theta_f\right)} = E(x=-d/2)\,e^{-i k_0 n_f d\cos\theta_f}
   $$

   Crossing the slab from $x=-d/2$ to $x=d/2$ adds a phase set by the ray's $x$-component of the wavevector, $k_0 n_f\cos\theta_f$, over the full core thickness $d$ — the same one-way distance as before, since it's set by the slab's thickness, not by where the origin sits.

3. **Identify the one-way phase accumulation across the slab.**

   $$
   \Delta\varphi = -k_0 n_f d\cos\theta_f
   $$

   This is the phase picked up crossing the core once, before any reflection is included.

4. **Close the round trip: down, reflect, across, reflect again, and demand the total returns to a multiple of $2\pi$.**

   $$
   -2n_f k_0 d\cos\theta_f + 2\phi_c + 2\phi_s = 2\pi N, \qquad N=1,2,3,\dots
   $$

   The factor of 2 on the propagation term comes from traversing the slab twice (down and back) in one round trip; the $2\phi_c$ and $2\phi_s$ terms are the phase shifts from the two TIR bounces. Only angles $\theta_f$ satisfying this closure condition interfere constructively on every round trip, so only these angles correspond to a self-consistent, physically guided mode.

## Result

$$
-2n_f k_0 d\cos\theta_f + 2\phi_c + 2\phi_s = 2\pi N, \qquad N=1,2,3,\dots
$$

## Where It's Used

**Concept:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md)

---

## Links

**Related:** [TIR Phase Shift](../05%20-%20Optics/TIR%20Phase%20Shift.md), [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md) (alternate, rigorous route to the same condition)
