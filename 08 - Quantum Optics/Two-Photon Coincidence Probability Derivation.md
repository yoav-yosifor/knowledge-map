---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

This derives the [quantum second-order coherence function](Quantum%20Second-Order%20Coherence.md) $G^{(2)}$ as the actual, physically measured probability that two photodetectors click simultaneously. In doing so, it resolves the historical puzzle of how two different photons can appear to interfere.

## Starting Point

- Two ideal, point-like detector atoms at positions $\vec r_1,\vec r_2$, each coupled to the field via the RWA dipole interaction $\hat H_j^{(I)}=-\hat d\cdot\hat E^{(+)}(\vec r_j,t)+h.c.$
- First-order time-dependent perturbation theory for the transition probability of each detector
- Completeness of the field's final-state basis, $\sum_{\psi_f^{field}}|\psi_f^{field}\rangle\langle\psi_f^{field}|=\hat I$

## Full Derivation

1. Write the probability that both detectors click as a sum, over all possible final field states, of the squared transition amplitude driven by the combined interaction $\hat H_{int}^{(I)}=\hat H_1^{(I)}+\hat H_2^{(I)}$. This is done because "both detectors fire" is a joint transition of the whole atom-field system, and first-order perturbation theory is the standard tool for computing a transition probability from an interaction Hamiltonian.

2. Expand to first order in each detector's interaction (since each detector atom transitions once), keeping only the cross term where detector 1 absorbs one photon and detector 2 absorbs a different photon, since this term is exactly the piece that carries a genuine two-photon coincidence and not two coincidental single-photon events counted separately. This isolates the physically relevant two-photon absorption process from the full perturbative expansion.

3. Use completeness of the final field states, $\sum_{\psi_f^{field}}|\psi_f^{field}\rangle\langle\psi_f^{field}|=\hat I$, to collapse the sum over unobserved final states into a single expectation value evaluated in the initial field state alone. This step is taken because the experiment never actually measures which specific final field state resulted — only that both detectors clicked — so summing over all of them (via completeness) is the correct way to discard that unwanted information.

4. **Recognize normal ordering.**

   $$
   \left\langle\psi_i^{field}\right|\hat E^{(-)}(\vec r_1,t_1)\hat E^{(-)}(\vec r_2,t_2)\hat E^{(+)}(\vec r_2,t_2)\hat E^{(+)}(\vec r_1,t_1)\left|\psi_i^{field}\right\rangle
   $$

   Because each detector interaction only contains the field operator $\hat E^{(+)}$ (the photon-absorbing, annihilation-type part) acting to the right on the initial state and $\hat E^{(-)}$ (its Hermitian conjugate, from the bra side) acting to the left, the resulting expectation value is automatically normal-ordered, as above. This is the crucial physical insight: normal ordering is not an assumption bolted on afterward, it falls directly out of how a real absorptive photodetector interacts with the field, since a detector can only ever absorb (not emit) a photon to register a click.

5. **Generalize to $G^{(n)}$.**

   $$
   G^{(n)}=\left\langle:\hat I(\vec x_n)\cdots\hat I(\vec x_1):\right\rangle
   $$

   Identifying the normal-ordered four-point correlator from the previous step as $G^{(2)}$, the definition generalizes immediately to an $n$-fold coincidence probability for $n$ simultaneously-clicking detectors, as above. This generalization is done because the same first-order-perturbation argument applies unchanged to any number of detectors, each contributing one more normally-ordered field-operator pair.

## Result

$$
G^{(2)}(\tau) = \int_0^t dt_2\int_0^t dt_1\,\left\langle\psi_i^{field}\right|\hat E^{(-)}(\vec r_1,t_1)\hat E^{(-)}(\vec r_2,t_2)\hat E^{(+)}(\vec r_2,t_2)\hat E^{(+)}(\vec r_1,t_1)\left|\psi_i^{field}\right\rangle \equiv \left\langle:\hat I(\vec x_2)\hat I(\vec x_1):\right\rangle
$$

## Where It's Used

**Concept:** [Quantum Second-Order Coherence](Quantum%20Second-Order%20Coherence.md)

---

## Links

**Related:** [Quantum Second-Order Coherence](Quantum%20Second-Order%20Coherence.md), [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md), [Hanbury-Brown and Twiss Experiment](Hanbury-Brown%20and%20Twiss%20Experiment.md)
