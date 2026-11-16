---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A dielectric slab with a core index higher than both surrounding media ($n_f>n_c$, $n_f>n_s$) traps light by [total internal reflection](../05%20-%20Optics/TIR%20Phase%20Shift.md) into a discrete set of guided modes. Normalizing the geometry and indices into dimensionless parameters $V$, $b$, $a$ collapses every slab waveguide, regardless of its specific dimensions, onto the same universal characteristic-equation curves.

## Key Equation

$$
\tan^{-1}\!\left(\sqrt{\tfrac{b}{1-b}}\right) + \tan^{-1}\!\left(\sqrt{\tfrac{b+a}{1-b}}\right) = V\sqrt{1-b} - \pi N, \quad N=0,1,2,\dots
$$

**Derived From:** substituting the normalized frequency $V=k_0 d\sqrt{n_f^2-n_s^2}$, asymmetry coefficient $a=(n_s^2-n_c^2)/(n_f^2-n_s^2)$, and normalized propagation coefficient $b=(n_{eff}^2-n_s^2)/(n_f^2-n_s^2)$ (with $n_{eff}=\beta/k_0$) into the guided-mode condition — see [TIR Self-Consistency Derivation](TIR%20Self-Consistency%20Derivation.md) and [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md) for the two ways of reaching that condition.

**Which form to use:** the normalized $(V,b,a)$ arctan form above is for finding/plotting modes — one dimensionless curve, branch $N$ explicit, covers every slab regardless of its specific $n_c,n_f,n_s,d$. The raw $\tan(2\theta)$ form below is for working directly with a given slab's physical decay/oscillation constants (e.g. checking a derivation, plugging in real units) — same equation, just not yet normalized.

## Supporting Formulas

- **TE vs. TM — which fields are present:** TE modes have $E_z=0$, built from $(E_y,H_x,H_z)$; TM modes have $H_z=0$, built from $(H_y,E_x,E_z)$ — each polarization keeps only the field component transverse to both the propagation direction and the direction of index variation.
- **TE vs. TM — why the profiles differ slightly:** both share the same piecewise shape (harmonic in the core, exponential decay outside) and the same functional form of characteristic equation, but TE matches $E_y,\partial_xE_y$ at each interface while TM matches $H_y,\tfrac1{n^2}\partial_xH_y$ — that extra $1/n^2$ weighting is the only difference between them, and it's what rescales TM's decay constants below.
- $\tan(2\theta)$ characteristic equations, raw (un-normalized) form, symmetric-slab convention, $\theta=\kappa_f d/2$:
  $$
  \tan(2\theta) = \frac{\kappa_f(\gamma_s+\gamma_c)}{\kappa_f^2-\gamma_s\gamma_c} \ \ \text{(TE)}, \qquad
  \tan(2\theta) = \frac{\kappa_f(\bar\gamma_s+\bar\gamma_c)}{\kappa_f^2-\bar\gamma_s\bar\gamma_c} \ \ \text{(TM)}, \quad \bar\gamma_{s,c}=\Big(\tfrac{n_f}{n_{s,c}}\Big)^2\gamma_{s,c}
  $$
  full derivation, including the raw $\epsilon$-explicit TM form it compresses from: [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md).
- TM characteristic equation, normalized form — the same relation as above, after the $V,b,a$ substitution used to reach the Key Equation: $\tan^{-1}\!\left(\dfrac{n_f^2}{n_s^2}\sqrt{\tfrac{b}{1-b}}\right) + \tan^{-1}\!\left(\dfrac{n_f^2}{n_c^2}\sqrt{\tfrac{b+a}{1-b}}\right) = V\sqrt{1-b} - \pi N$
- **Mode classification by $\beta/k_0$:**

| Regime | $\beta/k_0$ range | Core | Substrate | Cladding |
|---|---|---|---|---|
| Guided | $n_f > \beta/k_0 > n_s$ | harmonic | exponential decay | exponential decay |
| Substrate | $n_s > \beta/k_0 > n_c$ | harmonic | harmonic | exponential decay |
| Radiation | $\beta/k_0 < n_c$ | harmonic | harmonic | harmonic |

- $N$ indexes the tangent-function branch (mode number)
- Number of guided modes at a given $V$ (from the $b=0$ cutoff of each branch $N$): $M_{TE} = \left\lfloor \dfrac{V-\tan^{-1}\sqrt a}{\pi}\right\rfloor + 1$, $\ M_{TM}=\left\lfloor \dfrac{V-\tan^{-1}\!\left[(n_f/n_c)^2\sqrt a\right]}{\pi}\right\rfloor + 1$ — full derivation: [Guided Mode Count Derivation](Guided%20Mode%20Count%20Derivation.md).

## Derivation Outline

1. Require self-consistency of the TIR-guided ray (round-trip phase = $2\pi N$) — ray-optics route. Full derivation: [TIR Self-Consistency Derivation](TIR%20Self-Consistency%20Derivation.md).
2. Equivalently, solve Maxwell's equations directly for the field profile and apply boundary conditions — rigorous route. Full derivation: [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md).
3. Both routes converge on the same characteristic equation; normalizing to $V$, $b$, $a$ makes it geometry-independent (see step 8/9 of the [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md)).
4. For the symmetric slab ($n_1=n_3$), the characteristic equation splits into two independent even/odd mode families via a double-angle-identity reduction. Full derivation: [Symmetric Slab Mode Families](Symmetric%20Slab%20Mode%20Families.md).

## Physical Intuition

<u>Why only discrete angles survive</u>

- Picture a ray bouncing inside the slab by total internal reflection. Most launch angles cancel themselves out over repeated bounces — the wave crest from one crossing lands out of step with the next.
- Only angles whose round-trip phase lines back up with itself survive; those are the guided modes. Everything else never forms a standing pattern.
- Same selection principle as a standing wave on a string or a bound state in a quantum well: only self-consistent patterns survive, which is why the modes are discrete and countable, not a continuum.

<u>What the normalized parameters mean</u>

- Normalized frequency (thickness, wavelength, index contrast combined) is roughly "how much room" there is for resonant angles to fit — bigger it is, the more guided modes exist.
- Normalized propagation coefficient says how tightly a given mode is held: near its max, the mode barely notices it's confined; near zero, it's barely hanging on, about to leak into the substrate.
- Asymmetry between the two outer materials sets a penalty: a symmetric slab guides its first mode at any thickness, but an asymmetric one needs enough size/contrast before even the lowest mode stops leaking away.

<u>What the mode profile looks like</u>

- Inside the core, the mode looks like a segment of a standing wave — the mode number counts how many times it crosses zero: the fundamental mode is a single hump with no crossings, the next has one, and so on, exactly like harmonics on a string.
- Outside the core, the field doesn't stop at the boundary — it fades away smoothly (an evanescent tail) rather than being sharply cut off, still carrying some of the mode's energy just outside the guiding layer.
- That tail reaches farther into whichever outer material is weaker at confining it (the higher-index side, since it's closer to matching the core) — so for an asymmetric slab, the same mode decays more slowly into the substrate than into the cladding.
- Higher-order modes ride closer to cutoff, so more of their energy sits in the tails and less in the core — right up until the tail stops decaying altogether and the mode stops being guided.
- TE and TM profiles for the same mode number look almost identical — they diverge only in how far the tails reach, since that's the one place their boundary conditions differ.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Goos-Hänschen Shift](Goos-Hänschen%20Shift.md), [TIR Phase Shift](../05%20-%20Optics/TIR%20Phase%20Shift.md)
**Full Derivation:** [TIR Self-Consistency Derivation](TIR%20Self-Consistency%20Derivation.md) (ray-optics), [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md) (rigorous, from Maxwell's equations), [Guided Mode Count Derivation](Guided%20Mode%20Count%20Derivation.md) (number of guided modes from the $V,b,a$ cutoff), [Symmetric Slab Mode Families](Symmetric%20Slab%20Mode%20Families.md) (even/odd mode-family split for $n_1=n_3$)
