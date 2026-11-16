---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

If the fields driving a quantum system change slowly enough compared to the energy gaps between its instantaneous eigenstates, the system stays locked onto whichever eigenstate
it started in. It continuously morphs along with that eigenstate rather than jumping out of it. This lets you trade the fixed "bare" atomic basis for a moving "adiabatic" basis of dressed states that track the changing fields.

## Key Equation

$$
|\langle k|\dot{k}'\rangle| \ll \frac{|E_k - E_{k'}|}{\hbar}
$$

**Derived From:** comparing the non-adiabatic coupling strength $\langle k|\dot k'\rangle$ — how fast the instantaneous eigenstates $|k(t)\rangle$ rotate as the Hamiltonian changes — to the dressed-state level spacing $|E_k-E_{k'}|/\hbar$; the approximation holds whenever the rotation is much slower than the gap it would have to cross.

## Supporting Formulas

- Instantaneous eigenvalue equation defining the adiabatic basis: $H(t)|k(t)\rangle = E_k(t)|k(t)\rangle$
- Decoupled equation of motion after the approximation: $i\hbar\,\dot c_{k'} = E_{k'}(t)\,c_{k'}$, solved exactly by a phase-only evolution $c_{k'}(t)=c_{k'}(0)\exp\!\big(-\tfrac{i}{\hbar}\int_0^t E_{k'}dt'\big)$ — see [Adiabatic Basis Decoupling](Adiabatic%20Basis%20Decoupling.md) for the full derivation
- Dressed-state gap set by the generalized Rabi frequency: $\Omega_\text{eff}=\sqrt{\Omega_1^2+\Omega_2^2}$; stronger driving fields widen the gap and make the adiabatic condition easier to satisfy
- Laboratory criteria: smooth, long pulses (abrupt turn-ons inject high-frequency Fourier components that violate the condition); strong coupling fields (wide gap); no accidental level degeneracies (an avoided, not exact, crossing — a true crossing sends $\langle k|\dot k'\rangle\to\infty$)

## Derivation Outline

1. Expand the state in the time-dependent (adiabatic) eigenbasis and substitute into the Schrödinger equation.
2. Project onto each basis bra to isolate the amplitude equations, using exact orthogonality of distinct eigenstates and the (exact, gauge-fixable) vanishing of an eigenstate's overlap with its own time derivative.
3. Identify the one remaining term — the non-adiabatic coupling between different eigenstates — as the sole source of inter-state transitions, and argue it vanishes when the driving changes slowly enough.

## Physical Intuition

Energy levels in quantum mechanics are discrete, not continuous — to jump between them, the system needs a sudden, specific "kick" equal to the gap. If the driving fields change smoothly and gradually enough, they never deliver anything like that kick; the electron, pictured as a standing wave of probability, simply has time to reshape its interference pattern continuously as the fields evolve, with no shock ever forcing it across the gap. Push the fields too fast, on the other hand, and the standing wave shatters into a chaotic mixture of eigenstates, exactly as a sudden jolt would scatter a standing wave on a string. The deep reason slow driving avoids the jolt is that a rate of change is, in quantum mechanics, the same thing as an energy — a slowly changing field has almost no high-frequency content, so it simply cannot supply the discrete packet of energy needed to bridge the gap. That is also why strong driving fields help: they widen the gap between dressed states, making it that much harder for any given rate of change to compete with it.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Adiabatic Basis Decoupling](Adiabatic%20Basis%20Decoupling.md), [Dark State](Dark%20State.md), [STIRAP](STIRAP.md), [Adiabatic Rapid Passage](Adiabatic%20Rapid%20Passage.md)
**Full Derivation:** [Adiabatic Basis Decoupling](Adiabatic%20Basis%20Decoupling.md)
