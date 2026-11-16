---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The three real numbers describing a driven two-level atom obey equations of motion that are exactly the equations of gyroscopic precession. The [Bloch vector](Optical%20Bloch%20Vector.md) precesses around an effective "Rabi vector" built from the detuning and the drive strength, just like a magnetic spin precesses around a magnetic field. Decay terms are then added by hand to capture spontaneous emission and dephasing.

## Key Equation

$$
\dot{\vec\sigma} = \vec\Omega \times \vec\sigma, \qquad \vec\Omega = (\Omega_0,\,0,\,-\Delta)
$$

**Derived From:** taking the von Neumann equation $\dot\rho = \tfrac{1}{i\hbar}[H,\rho]$ for the two-level density matrix in the RWA rotating frame, writing the coherence as $\rho'_{12}=u+iv$ and the population difference as $w=\rho_{22}-\rho_{11}$, and separating the resulting complex equation into its three real components — see [Density Matrix](../10%20-%20Quantum%20Information/Density%20Matrix.md) and [Von Neumann Equation](../10%20-%20Quantum%20Information/Von%20Neumann%20Equation.md).

## Supporting Formulas

- Component form: $\dot w = \Omega_0 v$, $\dot u = \Delta v$, $\dot v = -\Delta u - \Omega_0 w$
- With decay added (the full Optical Bloch Equations): $\dot w = \Omega_0 v - (w+1)/T_1$, $\dot u = \Delta v - u/T_2$, $\dot v = -\Delta u - \Omega_0 w - v/T_2$ — see [T1 and T2 Relaxation](T1%20and%20T2%20Relaxation.md)
- Generalized Rabi frequency = precession rate: $\Omega=|\vec\Omega|=\sqrt{\Omega_0^2+\Delta^2}$
- Steady state under continuous driving: see [Saturation Parameter](Saturation%20Parameter.md)
- Pre-rotating-frame density matrix equations (before RWA) oscillate at both $\omega_L$ and $\omega_A$ — moving to the rotating frame and applying the RWA is what strips this fast oscillation and produces the clean precession form above; see [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md)

## Derivation Outline

1. Write the density matrix equations of motion directly from the Hamiltonian, before any approximation — these oscillate rapidly at the optical frequency.
2. Move to the frame rotating at the laser frequency and apply the RWA, discarding counter-rotating terms, to obtain slowly-varying equations for the populations and the rotating-frame coherence.
3. Repackage the coherence's real and imaginary parts and the population difference into the three-component Bloch vector $(u,v,w)$; the resulting three coupled real equations are exactly the cross product of $\vec\sigma$ with a fixed vector $\vec\Omega$.

## Physical Intuition

The same mathematics that describes a spinning top precessing around gravity, or a magnetic moment precessing around a magnetic field, describes a driven two-level atom precessing around an effective field built from the detuning and the Rabi frequency. On resonance, that effective field points purely along the coupling direction, and the Bloch vector sweeps cleanly from the ground state, through an equal superposition, to the fully excited state and back — a Rabi flop. Detune the laser, and the effective field tilts, so the vector now precesses around a tilted axis on a cone that never quite reaches full excitation — faster oscillation, but capped amplitude. This geometric picture is exactly what lets a slow sweep of the detuning smoothly drag the Bloch vector from one pole of the sphere to the other (adiabatic rapid passage), the same way a compass needle tracks a slowly rotating magnet: rotate too fast and the needle — like the Bloch vector — falls behind and loses track.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Optical Bloch Vector](Optical%20Bloch%20Vector.md), [T1 and T2 Relaxation](T1%20and%20T2%20Relaxation.md), [Adiabatic Rapid Passage](Adiabatic%20Rapid%20Passage.md), [Von Neumann Equation](../10%20-%20Quantum%20Information/Von%20Neumann%20Equation.md)
**Full Derivation:**
