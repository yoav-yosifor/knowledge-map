---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

When a totally-internally-reflected wave's evanescent tail reaches a second, higher-index medium separated from the first by only a thin low-index gap, part of the wave "hops" across the gap and re-emerges as a propagating wave in that second medium — reducing the reflection below unity even though the incidence angle exceeds the critical angle. This is similar to tunneling in quantum mechanics.

## Key Equation

$$
\theta_1>\theta_{cr}=\sin^{-1}\!\left(\frac{n_2}{n_1}\right)
$$

**Derived From:** stated directly in the source as the ordinary TIR condition at the $n_1$–$n_2$ interface (from Snell's law). Frustrated TIR occurs when a third, higher-index layer $n_3$ is placed close enough beyond the low-index gap that $\theta_1<\sin^{-1}(n_3/n_1)$ (which requires $n_3>n_2$), allowing part of the light to be transmitted into $n_3$ instead of being fully reflected.

## Supporting Formulas

- Requires $n_3>n_2$ for the second threshold angle $\sin^{-1}(n_3/n_1)$ to exist above the first.
- Transmission and reflection depend on the separation $h$ between the two high-index media — larger $h$ means more evanescent decay before reaching the second medium, so less tunneling and reflection closer to $1$.

## Derivation Outline

1. A wave undergoes ordinary TIR at an interface where $\theta_1>\theta_{cr}=\sin^{-1}(n_2/n_1)$, producing an evanescent field beyond the interface.
2. If a third medium of higher index $n_3>n_2$ is placed close enough that $\theta_1<\sin^{-1}(n_3/n_1)$, the evanescent tail can couple into a propagating wave inside $n_3$ before it fully decays.
3. Some of the incident power is therefore transmitted through the low-index gap instead of being fully reflected — the transmission/reflection split is set by the gap thickness $h$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [TIR Phase Shift](../05%20-%20Optics/TIR%20Phase%20Shift.md), [Goos-Hänschen Shift](Goos-Hänschen%20Shift.md), [Leaky Waveguide Modes](Leaky%20Waveguide%20Modes.md)
**Full Derivation:**
