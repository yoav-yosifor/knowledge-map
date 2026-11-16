---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The exact rotating-frame Hamiltonian for a laser-driven two-level atom. It shows precisely how the detuning appears on the diagonal, and how the coupling splits into a constant (resonant) part and a rapidly oscillating (counter-rotating) part that the [RWA](Rotating%20Wave%20Approximation.md) discards.

## Starting Point

- Bare atom Hamiltonian: $H_0=\hbar\omega_a|e\rangle\langle e|$ (ground state energy set to zero)
- Dipole interaction: $V(t)=\hbar\Omega_0\cos(\omega_L t)(\sigma_++\sigma_-)$, with $\sigma_+=|e\rangle\langle g|$, $\sigma_-=|g\rangle\langle e|$, and peak Rabi frequency $\Omega_0=dE_0/\hbar$ — see [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md)
- Schrödinger equation $i\hbar\,\partial_t|\psi\rangle = H|\psi\rangle$ with $H=H_0+V(t)$

## Full Derivation

1. **Expand the cosine.**

   $$
   \cos(\omega_L t)=\tfrac12\left(e^{i\omega_L t}+e^{-i\omega_L t}\right)
   $$

   This splits $V(t)$ into four terms: $\sigma_+e^{-i\omega_L t}$, $\sigma_-e^{+i\omega_L t}$ (co-rotating) and $\sigma_+e^{+i\omega_L t}$, $\sigma_-e^{-i\omega_L t}$ (counter-rotating). This is done because the four terms behave completely differently once we track energy bookkeeping: the first pair excites the atom while a photon is absorbed (or de-excites it while one is emitted) — both conserve energy near resonance — while the second pair would require creating or destroying $\approx2\hbar\omega_L$ of energy from nothing.

2. **Define the rotating-frame unitary.**

   $$
   U(t)=e^{i\omega_L t\,|e\rangle\langle e|}={\rm diag}(1,\,e^{i\omega_L t})
   $$

   This factors the trivial optical-frequency phase out of the excited-state amplitude via $b_e\equiv e^{i\omega_L t}c_e$. This is done because $c_e(t)$ winds at $\omega_a\sim10^{14}$ Hz even with no interesting physics happening — that fast phase must be stripped away before the slow Rabi dynamics ($\sim10^6$–$10^9$ Hz) can be seen or solved for numerically.

3. **Compute the frame drag.**

   $$
   -i\hbar\,U\dot U^\dagger = -\hbar\omega_L|e\rangle\langle e|
   $$

   This is the extra term generated purely by the frame itself. This is done because transforming into a moving (rotating) coordinate system always introduces a fictitious contribution to the Hamiltonian, exactly as switching to a rotating reference frame in classical mechanics introduces a centrifugal term — here it subtracts the laser frequency from the excited-state energy.

4. **Add the transformed bare Hamiltonian.**

   $$
   UH_0U^\dagger=\hbar\omega_a|e\rangle\langle e|
   $$

   Since $H_0$ is diagonal in the same basis as $U$, it is unaffected by the transformation. Combined with the frame drag, this gives

   $$
   \hbar(\omega_a-\omega_L)|e\rangle\langle e| = \hbar\Delta\,|e\rangle\langle e|
   $$

   This step is done to show that the detuning is not inserted by hand — it is the leftover mismatch between what the real atom wants to do ($\omega_a$) and what the chosen frame automatically removes ($\omega_L$).

5. **Transform the ladder operators.**

   $$
   U\sigma_+U^\dagger=e^{i\omega_L t}\sigma_+, \qquad U\sigma_-U^\dagger=e^{-i\omega_L t}\sigma_-
   $$

   Direct matrix multiplication gives these. This is done because the interaction term must be transformed the same way as everything else in the Hamiltonian, and these are the building blocks needed to see how each of the four cosine-expansion terms behaves in the new frame.

6. **Transform the interaction and multiply out the phases.**

   $$
   e^{+i\omega_L t}\!\cdot\! e^{-i\omega_L t}=1, \qquad e^{-i\omega_L t}\!\cdot\! e^{+i\omega_L t}=1, \qquad e^{\pm i\omega_L t}\!\cdot\! e^{\pm i\omega_L t}=e^{\pm2i\omega_L t}
   $$

   Applying $U\cdots U^\dagger$ to each of the four terms from step 1 and multiplying the resulting phase factors: the two co-rotating terms pick up the first two products above — they become constants — while the two counter-rotating terms pick up the third, doubling their oscillation frequency instead of cancelling. This step is done because it is the mechanical heart of the RWA: the frame transformation was specifically chosen so the physically relevant (co-rotating) terms freeze while the unphysical (counter-rotating) terms get pushed to an even faster, more obviously negligible frequency.

7. **Assemble and truncate.**

   $$
   H_\text{rot}=\hbar\Delta|e\rangle\langle e| + \frac{\hbar\Omega_0}{2}(\sigma_++\sigma_-) + \frac{\hbar\Omega_0}{2}\left(\sigma_+e^{2i\omega_L t}+\sigma_-e^{-2i\omega_L t}\right)
   $$

   Collecting everything gives the Hamiltonian above. Dropping the last, fast-oscillating piece — justified because its accumulated effect on the amplitudes is bounded by $\Omega_0/\omega_L\ll1$ relative to the surviving term — leaves the time-independent RWA Hamiltonian. This final step is done because a Hamiltonian that no longer depends on time can be diagonalized once and solved exactly, rather than requiring a numerical integration that resolves $10^{14}$ Hz oscillations just to see $10^6$–$10^9$ Hz dynamics.

## Result

$$
H_\text{RWA} = \hbar\begin{pmatrix}0 & \Omega_0/2\\\Omega_0/2 & \Delta\end{pmatrix}
$$

## Where It's Used

**Concept:** [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md)

---

## Links

**Related:** [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Rabi Oscillations](Rabi%20Oscillations.md), [Bloch-Siegert Shift](Bloch-Siegert%20Shift.md), [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [Rotating Frame Transformation](Rotating%20Frame%20Transformation.md)
