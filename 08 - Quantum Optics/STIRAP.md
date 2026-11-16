---
tags:
  - quantum-optics
  - system
  - device
---
---
## Overview

STIRAP (Stimulated Raman Adiabatic Passage) is a pulse sequence that transfers population completely from one ground state to another in a [Lambda three-level atom](Three-Level%20Atom%20Configurations.md), without ever populating the lossy excited state. It does this by counter-intuitively turning on the "second" laser before the "first." That order [adiabatically](Adiabatic%20Approximation.md) rotates the [dark state](Dark%20State.md) from the initial ground state to the final one.

## Prerequisite Concepts

- [Dark State](Dark%20State.md) — the zero-excited-state superposition that STIRAP adiabatically rotates from $|1\rangle$ to $|2\rangle$
- [Three-Level Atom Configurations](Three-Level%20Atom%20Configurations.md) — the Lambda-system Hamiltonian and its two driving fields $\Omega_1,\Omega_2$
- [Adiabatic Approximation](Adiabatic%20Approximation.md) — the slow-driving condition that keeps the atom locked to the dark state throughout the pulse sequence

## Regimes and Parameters

- **Intuitive pulse order** ($\Omega_1$ first, then $\Omega_2$): fails — with $\Omega_2=0$ initially there is no dark state to hide in, so the atom is driven straight into the lossy excited state $|3\rangle$
- **Counter-intuitive pulse order** ($\Omega_2$ first, then $\Omega_1$, overlapping): succeeds — at $\Omega_1=0,\Omega_2\neq0$ the dark state already coincides with $|1\rangle$, so the atom starts inside the dark state before $|1\rangle\leftrightarrow|3\rangle$ coupling ever turns on; as the pulses evolve the dark state rotates smoothly toward $|2\rangle$
- **Adiabatic condition:** $\left|\frac{d}{dt}\arctan(\Omega_1/\Omega_2)\right| \ll \sqrt{|\Omega_1|^2+|\Omega_2|^2}$ — the dark-state mixing angle must rotate more slowly than the dressed-state splitting; requires smooth, long, overlapping pulses and no gap between them
- **Result:** $P_{|1\rangle\to|2\rangle}=100\%$ with excited-state population $|b_3|^2\to0$ throughout — spontaneous emission from $|3\rangle$ never gets a chance to act because the state is never populated

## Physical Intuition

The ordinary way to move population from state 1 to state 3 to state 2 is to push it through the excited state — but the excited state is a "leaky bucket": every moment population spends there, some of it randomly leaks out via spontaneous emission, capping the achievable transfer efficiency no matter how carefully the pulses are timed. STIRAP sidesteps the leaky bucket entirely by never actually putting population in it. The trick is backwards from what intuition suggests: turn on the laser that couples to the *target* state before the laser that couples to the *starting* state. Doing this means that, right from the very first instant, there already exists a special combination of the two ground states — the dark state — that is completely blind to both lasers, and it happens to coincide exactly with where the atom starts. As the two laser intensities are then swapped smoothly over time, that same dark state morphs continuously into the target ground state, and if the morphing is slow enough (adiabatic) the atom is dragged along inside it the whole way, arriving at the target state having never sat, even briefly, in the leaky excited state.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Dark State](Dark%20State.md), [Adiabatic Rapid Passage](Adiabatic%20Rapid%20Passage.md)
**Concepts Used:** [Adiabatic Approximation](Adiabatic%20Approximation.md), [Three-Level Atom Configurations](Three-Level%20Atom%20Configurations.md), [Rabi Oscillations](Rabi%20Oscillations.md)
