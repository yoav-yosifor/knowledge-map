---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The coincidence-detection probability of two photons at a balanced [beamsplitter](Quantum%20Beamsplitter.md), worked out in three cases: for distinguishable photons, for perfectly indistinguishable photons at zero delay, and for [wavepacket](Single-Photon%20Wave%20Packet.md) photons at a general relative delay $\tau$. This general result is the [Hong-Ou-Mandel dip](Hong-Ou-Mandel%20Effect.md).

## Starting Point

- Balanced beamsplitter scattering matrix, $t=1/\sqrt2$, $r=i/\sqrt2$, from [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md) and [Quantum Beamsplitter](Quantum%20Beamsplitter.md)
- Coincidence rate as a normal-ordered intensity correlator, $G^{(2)}=\langle:\hat I_a\hat I_b:\rangle$, from [Quantum Second-Order Coherence](Quantum%20Second-Order%20Coherence.md)
- Single-photon wavepacket creation operator $\hat a^\dagger[\phi;t]=\int dt\,\phi(t)\hat a^\dagger(t)$ with $\int dt\,|\phi(t)|^2=1$, from [Single-Photon Wave Packet](Single-Photon%20Wave%20Packet.md), and continuum commutator $[\hat a(t),\hat a^\dagger(t')]=\delta(t-t')$

## Full Derivation

1. **Distinguishable photons.**

   $$
   |\psi_{in}\rangle=\hat a_{in}^{(H)\dagger}\hat b_{in}^{(V)\dagger}|0\rangle
   $$

   Send a horizontally polarized photon into port $a$ and a vertically polarized photon into port $b$, and propagate each creation operator through the beamsplitter scattering matrix separately for each polarization. This is done first because polarization acts as an unambiguous "which-path" tag: since the two photons remain distinguishable throughout, this case establishes the ordinary, non-interfering baseline to compare the quantum effect against.

2. Expand the resulting output state into its four two-photon components and compute the coincidence rate by acting with the annihilation operators for each cross combination on the output state, giving:

   $$
   G^{(2)}(0)=\tfrac14+\tfrac14=\tfrac12
   $$

   This reproduces the classical 50% coincidence probability, confirming that distinguishable photons show no two-photon interference at all — the two contributing amplitudes never overlap because the polarization labels keep them apart.

3. **Indistinguishable photons at zero delay.** Drop the polarization labels, $|\psi_{in}\rangle=|1\rangle_a\otimes|1\rangle_b$, and again propagate through the beamsplitter; the two cross-term contributions to the "one photon in each output" amplitude now carry coefficients $r^2$ and $(t^*)^2$ that sum to exactly zero for the balanced beamsplitter:

   $$
   r^2+(t^*)^2=0
   $$

   This cancellation is the heart of the effect: because the photons are now genuinely identical, the two histories ("both transmitted" and "both reflected") cannot be told apart even in principle, and quantum mechanics adds their amplitudes rather than their probabilities — and those amplitudes happen to cancel exactly.

4. Simplify the surviving output state and confirm the coincidence rate vanishes:

   $$
   |\psi_{out}\rangle=\tfrac{i}{\sqrt2}(|2,0\rangle+|0,2\rangle), \qquad \hat a_{out}\hat b_{out}|\psi_{out}\rangle=0 \ \Rightarrow\ G^{(2)}(0)=0
   $$

   This step nails down the headline result: perfectly indistinguishable photons always leave together from the same output port, and the two detectors can never click in coincidence.

5. **Finite delay.** Replace the idealized single-mode photons with finite-duration wavepackets, $|1_\phi\rangle=\int dt\,\phi(t)\hat a^\dagger(t)|0\rangle$, and give the two input wavepackets a relative delay $\tau$:

   $$
   |\psi_{in}\rangle=\hat a_{in}^\dagger[\phi_a;t]\,\hat b_{in}^\dagger[\phi_b;t-\tau]|0\rangle
   $$

   A meaningful notion of "delay" requires photons localized in time, which is exactly why the idealized single-mode treatment above must be replaced by the wavepacket formalism here.

6. Propagate each wavepacket creation operator through the beamsplitter and expand the resulting product into the four combinations of which port each wavepacket ends up in, exactly mirroring the algebra of step 3 but now carried by wavepacket (rather than single-mode) operators. This step generalizes the zero-delay algebra to the case where the two wavepackets need not perfectly overlap.

7. Act on the output state with the detection operators $\hat a_{out}(t_a)\hat b_{out}(t_b)$ and integrate over the detection times; the "both photons in the same detector" terms vanish exactly as before (annihilating the vacuum), leaving only the two surviving cross terms, evaluated via the continuum commutator:

   $$
   [\hat a_{out}(t_a),\hat a_{out}^\dagger[\phi;t]]=\phi(t_a-t)
   $$

   This isolates the interference term that depends on the wavepacket overlap, the delay-dependent generalization of the perfect cancellation found at $\tau=0$.

8. Integrate the squared magnitude of the surviving amplitude over the detection times to obtain the overlap integral between the two wavepacket envelopes:

   $$
   G^{(2)}(0;\tau)=\frac12\left(1-\left|\int dt\,\phi_a(t)\phi_b^*(t-\tau)\right|^2\right)
   $$

   This is the central result: the coincidence rate depends entirely on how well the two photon wavepackets overlap, i.e. on their degree of indistinguishability, smoothly interpolating between the perfect-overlap ($\tau=0$) and no-overlap (large $\tau$) limits already found.

9. Repeat the same propagation in the frequency domain, where a time delay $\tau$ becomes a linear phase $e^{-i\omega\tau}$, obtaining the equivalent form:

   $$
   G^{(2)}(0;\tau)=\frac12\left(1-\left|\int d\omega\,\phi_a^*(\omega)\phi_b(\omega)e^{-i\omega\tau}\right|^2\right)
   $$

   This alternative derivation is included to confirm the dip's width is set by the spectral overlap of the two photons — the Fourier-dual statement of the temporal-overlap result.

10. Evaluate the overlap integral for Gaussian wavepackets and specialize to identical wavepackets ($\omega_{a0}=\omega_{b0}$, $\sigma_a=\sigma_b\equiv\sigma$), collapsing the general result to the characteristic Hong-Ou-Mandel dip:

    $$
    G^{(2)}(0;\tau)=\frac12\left(1-e^{-\sigma^2\tau^2/2}\right)
    $$

    This final step gives the concrete, experimentally recognizable shape of the dip — a smooth Gaussian well dropping from the classical $1/2$ baseline to exactly $0$ at zero delay, with a width fixed by the inverse spectral bandwidth of the photons.

## Result

$$
G^{(2)}(0;\tau) = \frac{1}{2}\left(1-\left|\int dt\,\phi_a(t)\phi_b^*(t-\tau)\right|^2\right), \qquad \text{Gaussian case: } G^{(2)}(0;\tau)=\frac12\left(1-e^{-\sigma^2\tau^2/2}\right)
$$

## Where It's Used

**Concept:** [Hong-Ou-Mandel Effect](Hong-Ou-Mandel%20Effect.md)

---

## Links

**Related:** [Hong-Ou-Mandel Effect](Hong-Ou-Mandel%20Effect.md), [Quantum Beamsplitter](Quantum%20Beamsplitter.md), [Single-Photon Wave Packet](Single-Photon%20Wave%20Packet.md), [Quantum Second-Order Coherence](Quantum%20Second-Order%20Coherence.md)
