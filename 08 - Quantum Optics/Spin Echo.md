---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

A π-pulse applied midway through a free-precession interval flips every atom's position on the Bloch equator. This puts the atoms that had raced ahead (due to [inhomogeneous broadening](Inhomogeneous%20Broadening.md)) behind, and they steadily catch back up to the ones that had lagged. The result is a burst of recovered signal, the echo, whose amplitude depends only on the truly irreversible (homogeneous) decoherence.

## Key Equation

$$
\text{Echo amplitude} \propto e^{-2\tau/T_2^{(\text{homog})}}
$$

**Derived From:** the pulse sequence $\pi/2 \to$ free precession $\tau \to \pi \to$ free precession $\tau \to$ echo; inhomogeneous dephasing accumulated during the first $\tau$ is exactly time-reversed by the $\pi$-pulse and exactly cancelled during the second $\tau$, so only the irreversible, stochastic contributions accumulated over the total time $2\tau$ survive in the echo amplitude.

## Supporting Formulas

- Pulse sequence: (1) $\pi/2$-pulse about $\hat y$ — all atoms rotate to the equator, in phase; (2) free precession for $\tau$ — atoms fan out, ensemble coherence decays as $e^{-(\Delta\Omega\,\tau)^2/2}$; (3) $\pi$-pulse about $\hat x$ at time $\tau$ — every Bloch vector is flipped, fast atoms now behind, slow ones ahead; (4) free precession for $\tau$ — atoms converge; (5) echo at $t=2\tau$
- What it measures: the true, fundamental $T_2^{(\text{homog})}$ (spontaneous emission + collisions), independent of the apparent, much shorter $T_2^*$ set by inhomogeneous broadening — see [Inhomogeneous Broadening](Inhomogeneous%20Broadening.md) and [T1 and T2 Relaxation](T1%20and%20T2%20Relaxation.md)
- Application: in atomic clocks, the photon echo effectively replaces $T_2^*$ with $T_2^{(\text{homog})}$ as the operative coherence time, unlocking the full intrinsic coherence of the transition — see [Cesium Fountain Clock](Cesium%20Fountain%20Clock.md)

## Derivation Outline

1. Apply a $\pi/2$-pulse to bring all atoms from the ground state to the equator of the Bloch sphere, in phase.
2. Let the ensemble precess freely for time $\tau$; because different atoms have different detunings, they fan out across the equatorial plane and the macroscopic coherence signal decays.
3. Apply a $\pi$-pulse that flips every Bloch vector; atoms that had raced ahead are now placed behind, and vice versa.
4. Let the ensemble precess freely for a second interval $\tau$; since each atom's precession rate is unchanged and deterministic, the flip causes all atoms to re-converge exactly at $t=2\tau$, producing a strong emitted signal — the echo — whose amplitude reflects only whatever coherence was irreversibly lost along the way.

## Physical Intuition

Picture that same group of runners with slightly different, fixed paces, now imagine that exactly halfway through the race everyone is instantly teleported to the mirror-image position on the track — the runners who had pulled ahead are now placed the same distance behind the pack, and the stragglers are now the same distance ahead. Since everyone keeps running at their own unchanged, steady pace, the fast runners (now behind) steadily close the gap on the slow ones (now ahead), and at exactly double the elapsed time, everyone arrives back at the same point simultaneously — a burst of "everyone together" that wasn't there a moment before or after. This trick can undo any dephasing that comes from atoms simply running at different but fixed rates, but it cannot undo dephasing from a genuinely random event — a runner who trips and loses their place unpredictably cannot be un-tripped by any clever choreography. That is why the echo isolates exactly the irreversible, "runner tripped" component of decoherence and discards the reversible, "different fixed paces" component.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Inhomogeneous Broadening](Inhomogeneous%20Broadening.md), [T1 and T2 Relaxation](T1%20and%20T2%20Relaxation.md), [Ramsey Interferometer](Ramsey%20Interferometer.md)
**Full Derivation:**
