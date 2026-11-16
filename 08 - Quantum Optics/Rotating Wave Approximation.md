---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

The Rotating Wave Approximation drops the part of the laser-atom coupling that describes energy-non-conserving processes, such as exciting the atom while also emitting a photon, or vice versa. That part oscillates so fast it averages to zero. What's left is a clean, time-independent Hamiltonian that governs [Rabi oscillations](Rabi%20Oscillations.md).

## Key Equation

$$
H_\text{RWA} = \hbar\Delta\,|e\rangle\langle e| + \frac{\hbar\Omega_0}{2}(\sigma_++\sigma_-) = \hbar\begin{pmatrix}0 & \Omega_0/2\\\Omega_0/2 & \Delta\end{pmatrix}
$$

**Derived From:** transforming the full lab-frame Hamiltonian $H=H_0+V(t)$ into the frame rotating at the laser frequency $\omega_L$, then discarding the terms that oscillate at $2\omega_L$ — see [RWA Rotating-Frame Derivation](RWA%20Rotating-Frame%20Derivation.md) for the full derivation.

## Supporting Formulas

- Detuning: $\Delta \equiv \omega_a-\omega_L$ — appears naturally on the diagonal as the residue of the atom's own energy minus the frame's rotation rate
- Validity condition: $\Omega_0/\omega_L \ll 1$ — satisfied by many orders of magnitude for ordinary optical driving ($\Omega_0\sim$ MHz–GHz, $\omega_L\sim$ hundreds of THz)
- Generalized Rabi frequency and eigenvalues: $\Omega=\sqrt{\Omega_0^2+\Delta^2}$, $\lambda_\pm = \tfrac{\hbar}{2}(\Delta\pm\Omega)$ — see [Dressed States](Dressed%20States.md)
- Equivalent physical picture: $H_\text{RWA}$ is identical in form to a spin-$\tfrac12$ particle in a static effective magnetic field $(\Omega_0,0,-\Delta)$ — the Bloch vector precesses around this vector, see [Optical Bloch Equations](Optical%20Bloch%20Equations.md)
- Correction beyond RWA: the [Bloch-Siegert Shift](Bloch-Siegert%20Shift.md), of order $(\Omega_0/\omega_L)^2$
- **Time-averaging bound (why the fast terms are actually negligible, not just "fast"):** for a term rotating at $\Omega$, $\left|\dfrac1T\displaystyle\int_0^T e^{i\Omega t}\,dt\right|=\left|\dfrac{e^{i\Omega T}-1}{i\Omega T}\right|\le\dfrac{2}{|\Omega|T}\xrightarrow[|\Omega|T\gg1]{}0$. More generally, if the fast phase multiplies a slowly-varying envelope $f(t)$, integrating $\int_0^Tf(t)e^{i\Omega t}dt$ by parts gives a result of order $1/\Omega$. So any term whose frequency $\Omega$ vastly exceeds the system's own dynamical rate ($\Omega_0$ or $\Delta$ here) contributes an accumulated effect suppressed by that same ratio — this is the precise statement standing behind "the counter-rotating terms average to zero."
- **Quantized-field (Jaynes-Cummings) version of the same approximation:** once the classical drive is replaced by a quantized mode, $\hat H_\text{int}\propto(\hat a+\hat a^\dagger)(\hat\sigma_++\hat\sigma_-)$ expands into four terms; in the interaction picture $\hat a(t)=\hat a\,e^{-i\omega_Lt}$, $\hat a^\dagger(t)=\hat a^\dagger e^{+i\omega_Lt}$, $\hat\sigma_-(t)=\hat\sigma_-e^{-i\omega_at}$, $\hat\sigma_+(t)=\hat\sigma_+e^{+i\omega_at}$, so $\hat a\hat\sigma_++\hat a^\dagger\hat\sigma_-$ rotate at the slow detuning $\pm\Delta$ while $\hat a\hat\sigma_-+\hat a^\dagger\hat\sigma_+$ rotate at $\approx\pm2\omega_a$; discarding the latter gives the [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md) $\hat H_\text{JC}=\hbar g(\hat a\hat\sigma_++\hat a^\dagger\hat\sigma_-)$ at resonance. The validity condition generalizes to $|\Delta|,\,g\ll\omega_{eg}$ — same structure as $\Omega_0/\omega_L\ll1$ above, with the coupling rate ($g$ or $\Omega_0$) playing the role of the dynamical rate that must stay far below the optical frequency.

## Derivation Outline

1. Expand the cosine driving term into four exponentials using Euler's formula; two are co-rotating (energy-conserving near resonance) and two are counter-rotating (would require gaining or losing $\approx2\hbar\omega_L$ from nowhere).
2. Move to a frame rotating at the laser frequency $\omega_L$; the co-rotating terms become constant, while the counter-rotating terms are pushed to oscillate at $2\omega_L$.
3. Argue (by direct time-averaging, or by the time–energy uncertainty relation) that the $2\omega_L$ terms contribute a negligible, rapidly self-cancelling correction on the timescale of any real Rabi dynamics, and discard them — made precise by the time-averaging bound in Supporting Formulas above.
4. What remains is a time-independent Hamiltonian with the detuning on the diagonal and half the peak Rabi frequency on the off-diagonal.

## Physical Intuition

Think of pushing a child on a swing. Pushing in sync with the swing's natural rhythm builds up amplitude — that's the resonant, co-rotating term. Pushing back and forth a million times faster than the swing's rhythm, in essentially random alignment with its motion, averages to nothing — that's the counter-rotating term. The counter-rotating terms in the full Hamiltonian describe genuinely energy-non-conserving events (the atom absorbs energy from a laser photon that is simultaneously being created, an impossible bookkeeping trick), and such virtual events can only persist for the fleeting time allowed by the uncertainty principle before they must vanish again — far too short to leave any lasting trace on the much slower Rabi dynamics. Dropping them turns an intractable, rapidly oscillating problem into a static one that behaves exactly like a compass needle in a fixed magnetic field.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [RWA Rotating-Frame Derivation](RWA%20Rotating-Frame%20Derivation.md), [Rotating Frame Transformation](Rotating%20Frame%20Transformation.md), [Bloch-Siegert Shift](Bloch-Siegert%20Shift.md), [Rabi Oscillations](Rabi%20Oscillations.md), [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md)
**Full Derivation:** [RWA Rotating-Frame Derivation](RWA%20Rotating-Frame%20Derivation.md)
