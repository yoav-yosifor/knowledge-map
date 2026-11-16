---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The three independent real numbers in a two-level atom's density matrix package into a Bloch vector $(u,v,w)$ whose components have distinct physical jobs. $w$ is how much population sits in the excited versus ground state. $u$ and $v$ are the two field quadratures of the atom's response: $u$ shifts the light's phase without absorbing energy (dispersion), while $v$ actually exchanges energy with the field (absorption or gain).

## Key Equation

$$
u \equiv 2\,\text{Re}(\rho_{ge}), \qquad v \equiv 2\,\text{Im}(\rho_{ge}), \qquad w \equiv \rho_{ee}-\rho_{gg}
$$

**Derived From:** the two-level density matrix $\rho=\begin{pmatrix}\rho_{ee}&\rho_{eg}\\\rho_{ge}&\rho_{gg}\end{pmatrix}$, which has four entries but only three independent real numbers once $\text{tr}\,\rho=1$ is imposed; $u,v,w$ are exactly that independent triple, reconstructed as $\rho=\tfrac12\begin{pmatrix}1+w & u-iv\\u+iv & 1-w\end{pmatrix}$.

## Supporting Formulas

- Pure-state (Bloch-sphere) condition: $u^2+v^2+w^2=1$; decoherence shrinks the vector inside the sphere, $u^2+v^2+w^2<1$, with full decoherence driving $u,v\to0$
- Coherence in polar form: $\rho_{ge}=|\rho_{ge}|e^{i\phi}$, so $u=2|\rho_{ge}|\cos\phi$, $v=2|\rho_{ge}|\sin\phi$ — nonzero $(u,v)$ signals a genuine quantum superposition, not a classical mixture
- Macroscopic polarization from an ensemble: $P(t)=N\langle\hat d\rangle = N\,\text{tr}(\hat d\rho) = Nd_{eg}\,u$ — the field only ever sees the ensemble-averaged $u$, not any single atom's amplitudes
- $u$ (Q-quadrature, in phase with the field): contributes zero net energy transfer; $\chi'\propto u\propto \Delta/(\Delta^2+1/T_2^2)$ — the dispersive lineshape, and $n\approx1+\tfrac12\chi'\propto u$ the refractive index
- $v$ (P-quadrature, in phase with $\dot E$): $\dot W\propto E_0\omega_L v$; $v>0$ means absorption, $v<0$ means stimulated emission/gain; $\chi''\propto v\propto (1/T_2)/(\Delta^2+1/T_2^2)$ — the Lorentzian absorption lineshape, and $\alpha\propto\chi''\propto v$ the absorption coefficient

## Derivation Outline

1. Write the ensemble-averaged density matrix of a two-level atom and identify its three independent real degrees of freedom (populations minus the trace constraint, plus the complex coherence).
2. Package those three numbers into $(u,v,w)$ so the geometry of the density matrix becomes a vector inside (or on) a unit sphere.
3. Relate $u$ and $v$ to the macroscopic polarization the field actually experiences, by taking the ensemble average and projecting the polarization onto the two quadratures of the driving field, $\cos(\omega_L t)$ and $\sin(\omega_L t)$.
4. Show that only the quadrature in phase with $\dot E$ (i.e. $v$) can transfer energy, by time-averaging the instantaneous power $\dot W = E(t)\dot P(t)$ over one field cycle.

## Physical Intuition

Picture the atom's dipole as a tiny oscillating antenna. It can oscillate perfectly in step with the driving field — like a mass on a spring pushed exactly at the right moments to keep its motion synchronized — in which case it never gains or loses net energy to the driver; it just shifts the field's phase as it passes through the medium. That in-step response is $u$, and macroscopically it is exactly what a refractive index is. Or the dipole's oscillation can lag the field by a quarter cycle, in which case, cycle after cycle, it is either steadily pulling energy out of the field (absorption) or steadily pumping energy into it (stimulated emission, if the atom is inverted) — that out-of-step response is $v$. Because any real experiment involves many atoms with slightly different histories and phases, the field only ever "feels" the ensemble average of these quadratures, not any one atom's instantaneous behavior — which is why the macroscopic polarization, and the observable refractive index and absorption of a medium, are built entirely from averaged $u$ and $v$.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Bloch Sphere](../10%20-%20Quantum%20Information/Bloch%20Sphere.md), [Optical Bloch Equations](Optical%20Bloch%20Equations.md), [Rabi Oscillations](Rabi%20Oscillations.md)
**Full Derivation:**
