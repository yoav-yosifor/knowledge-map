---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The Jaynes-Cummings interaction Hamiltonian $\hat H_{AF}=\hbar g(\hat a\hat\sigma_++\hat a^\dagger\hat\sigma_-)$ — a two-level atom coupled to a single quantized cavity mode — starting from the dipole interaction with the fully quantized multimode field, then applying the [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md) and restricting to one mode.

## Starting Point

- Two-level atom, ground $|g\rangle$ (energy $0$) and excited $|e\rangle$ (energy $\hbar\omega_a$): $\hat H_A=\hbar\omega_a\hat\sigma_+\hat\sigma_-$, with $\hat\sigma_+=|e\rangle\langle g|$, $\hat\sigma_-=|g\rangle\langle e|$ — see [Atomic Hamiltonian](Atomic%20Hamiltonian.md).
- Quantized multimode field: $\hat H_F=\sum_{k,\lambda}\hbar\omega_k\left(\hat a_{k,\lambda}^\dagger\hat a_{k,\lambda}+\tfrac12\right)$, $[\hat a_{k,\lambda},\hat a_{k,\lambda}^\dagger]=1$ — see [Electromagnetic Field Quantization](Electromagnetic%20Field%20Quantization.md).
- Dipole interaction energy $\hat H_\text{int}=-\hat{\vec d}\cdot\hat{\vec E}(\vec R)$, evaluated at the atom's fixed position $\vec R$ (dipole approximation) — see [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md).
- Dipole operator restricted to the two atomic levels: $\hat{\vec d}=d_{eg}(\hat\sigma_++\hat\sigma_-)$, using $d_{ee}=d_{gg}=0$ (parity) and $d_{ge}=d_{eg}^*$ (Hermiticity), $d_{eg}$ taken real — see [Transition Dipole Moment](Transition%20Dipole%20Moment.md).
- Quantized field operator at the atom's position, summed over modes: $\hat{\vec E}(\vec R)=\sum_{k,\lambda}E_{k,\lambda}(\vec R)\left(\hat a_{k,\lambda}+\hat a_{k,\lambda}^\dagger\right)$, where $E_{k,\lambda}(\vec R)$ folds in the per-photon field amplitude $\sqrt{2\pi\hbar\omega_k}$ and the mode's polarization/spatial profile $u_{k,\lambda}(\vec R)$ — see [Electric Field Operator](Electric%20Field%20Operator.md).

## Full Derivation

1. **Restrict the dipole coupling to two levels and insert the field expansion.** Substituting $\hat{\vec d}=d_{eg}(\hat\sigma_++\hat\sigma_-)$ and the field operator into $\hat H_\text{int}=-\hat{\vec d}\cdot\hat{\vec E}(\vec R)$:
   $$
   \hat H_\text{int}=-d_{eg}(\hat\sigma_++\hat\sigma_-)\cdot\sum_{k,\lambda}E_{k,\lambda}(\vec R)\left(\hat a_{k,\lambda}+\hat a_{k,\lambda}^\dagger\right)
   $$
   This is pure substitution — no approximation yet.

2. **Define the single-photon coupling constant per mode.** Collecting the atom-independent factors into $\hbar g_{k,\lambda}\equiv-d_{eg}\cdot E_{k,\lambda}(\vec R)=-\sqrt{2\pi\hbar\omega_k}\,d_{eg}\cdot u_{k,\lambda}(\vec R)$ (the interaction energy of the atom with a single quantum of that mode) gives the multimode interaction Hamiltonian in its standard pre-RWA form:
   $$
   \hat H_{AF}=\sum_{k,\lambda}\left(\hbar g_{k,\lambda}\hat a_{k,\lambda}+\hbar g_{k,\lambda}^*\hat a_{k,\lambda}^\dagger\right)\left(\hat\sigma_++\hat\sigma_-\right)
   $$

3. **Expand the product into four terms per mode.**
   $$
   \hat H_{AF}=\sum_{k,\lambda}\hbar g_{k,\lambda}\,\hat a_{k,\lambda}\hat\sigma_+ \;+\; \hbar g_{k,\lambda}\,\hat a_{k,\lambda}\hat\sigma_- \;+\; \hbar g_{k,\lambda}^*\,\hat a_{k,\lambda}^\dagger\hat\sigma_+ \;+\; \hbar g_{k,\lambda}^*\,\hat a_{k,\lambda}^\dagger\hat\sigma_-
   $$
   Each term pairs a field ladder operator with an atomic ladder operator; nothing has been dropped yet.

4. **Move to the interaction picture with respect to $\hat H_0=\hat H_A+\hat H_F$.** Under $\hat H_0$, each operator rotates at its own free frequency: $\hat\sigma_+(t)=\hat\sigma_+e^{i\omega_a t}$, $\hat\sigma_-(t)=\hat\sigma_-e^{-i\omega_a t}$, $\hat a_{k,\lambda}(t)=\hat a_{k,\lambda}e^{-i\omega_k t}$, $\hat a_{k,\lambda}^\dagger(t)=\hat a_{k,\lambda}^\dagger e^{i\omega_k t}$. Substituting into the four terms above:
   $$
   \hat a_{k,\lambda}\hat\sigma_+\to e^{i(\omega_a-\omega_k)t},\quad
   \hat a_{k,\lambda}^\dagger\hat\sigma_-\to e^{-i(\omega_a-\omega_k)t},\quad
   \hat a_{k,\lambda}\hat\sigma_-\to e^{-i(\omega_a+\omega_k)t},\quad
   \hat a_{k,\lambda}^\dagger\hat\sigma_+\to e^{i(\omega_a+\omega_k)t}
   $$

5. **Identify co-rotating versus counter-rotating terms.** Near resonance, $\omega_k\approx\omega_a$, so $\hat a_{k,\lambda}\hat\sigma_+$ and $\hat a_{k,\lambda}^\dagger\hat\sigma_-$ oscillate slowly, at the detuning $\omega_a-\omega_k$ — these are *co-rotating*, and each conserves the total excitation number (a photon is destroyed exactly as the atom is excited, or created exactly as the atom relaxes). The remaining two terms, $\hat a_{k,\lambda}^\dagger\hat\sigma_+$ and $\hat a_{k,\lambda}\hat\sigma_-$, oscillate fast, at $\approx\omega_a+\omega_k$ — these are *counter-rotating*: they would simultaneously create a photon and excite the atom (or destroy a photon and de-excite the atom), manufacturing or erasing energy from nowhere at the bare level. This is exactly the same co-/counter-rotating split as in the [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md) for a classical drive, applied here mode by mode to a quantized field.

6. **Apply the RWA: drop the counter-rotating terms.** Over any timescale relevant to the atom-field dynamics, the fast terms time-average to zero, leaving only the energy-conserving processes:
   $$
   \hat H_{AF}=\sum_{k,\lambda}\left(\hbar g_{k,\lambda}\hat a_{k,\lambda}\hat\sigma_++\hbar g_{k,\lambda}^*\hat a_{k,\lambda}^\dagger\hat\sigma_-\right)
   $$
   (written back in the Schrödinger picture, having discarded only the counter-rotating operator products — no picture-dependent step remains).

7. **Restrict to a single cavity mode.** Inside a cavity, only one mode $(k_0,\lambda_0)$ sits near resonance with the atomic transition and is appreciably coupled to it; every other mode is far detuned (and, for a real cavity, the boundary conditions forbid a continuum of propagating modes in the first place). Dropping the sum and keeping only that mode — relabeling $\hat a_{k_0,\lambda_0}\to\hat a$ and $g_{k_0,\lambda_0}\to g$ (real, by absorbing any residual phase into the definition of $|e\rangle$) — collapses the multimode sum to a single term:
   $$
   \hat H_{AF}=\hbar g\left(\hat a\,\hat\sigma_++\hat a^\dagger\,\hat\sigma_-\right)
   $$

## Result

$$
\hat H_{AF} = \hbar g\left(\hat a\,\hat\sigma_++\hat a^\dagger\,\hat\sigma_-\right)
$$

Together with the free atomic and field pieces, the complete Jaynes-Cummings Hamiltonian is

$$
\hat H_\text{JC} = \hbar\omega_c\,\hat a^\dagger\hat a + \hbar\omega_a\,\hat\sigma_+\hat\sigma_- + \hbar g\left(\hat a\,\hat\sigma_++\hat a^\dagger\,\hat\sigma_-\right)
$$

where $\omega_c$ is the cavity mode frequency (the zero-point $\tfrac12\hbar\omega_c$ dropped as a constant offset).

## Where It's Used

**Concept:** [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md)

---

## Links

**Related:** [Dipole Interaction Hamiltonian](Dipole%20Interaction%20Hamiltonian.md), [Rotating Wave Approximation](Rotating%20Wave%20Approximation.md), [Electromagnetic Field Quantization](Electromagnetic%20Field%20Quantization.md), [Electric Field Operator](Electric%20Field%20Operator.md), [Transition Dipole Moment](Transition%20Dipole%20Moment.md), [Atomic Hamiltonian](Atomic%20Hamiltonian.md)
