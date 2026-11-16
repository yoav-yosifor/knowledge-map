---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

That the [Einstein A and B coefficients](Einstein%20Coefficients.md) follow directly from quantum perturbation theory applied to a single atom coupled to the quantized field, with no assumption of thermal equilibrium required. Specifically, this derives the asymmetric $(n+1)$-vs-$n$ scaling of emission versus absorption rates.

## Starting Point

- Fermi's golden rule: transition rate $\Gamma \sim |M|^2\,\delta(E_f-E_i)$, with matrix element $M=\langle f|H_\text{int}|i\rangle$
- Single-photon interaction Hamiltonian: $H_\text{int} = H_I^\dagger\hat a^\dagger + H_I\hat a$, built from photon creation/annihilation operators
- Definition $M_0 \equiv \langle g|H_I^\dagger|e\rangle$

## Full Derivation

1. **Set up the emission process.**

   $$
   |e;n\rangle \ \longrightarrow\ |g;n+1\rangle
   $$

   Take the initial state as an excited atom with $n$ photons present, and the final state as the de-excited atom with one additional photon. This step is done because emission is, by definition, the process where the atom loses energy and the field gains a photon — writing the initial and final states explicitly is what lets Fermi's golden rule be applied.

2. **Evaluate the emission matrix element.** Acting with $H_I^\dagger\hat a^\dagger$ on $|e;n\rangle$ and using the raising-operator property $\hat a^\dagger|n\rangle=\sqrt{n+1}|n+1\rangle$ gives:

   $$
   M_{2\to1}=\sqrt{n+1}\,M_0^\dagger
   $$

   This step is done because the $\sqrt{n+1}$ factor is exactly where the field's quantum statistics enters the atomic transition rate — it is not put in by hand, it falls out of how the photon creation operator acts on a number state.

3. **Square to get the emission rate.** Since Fermi's golden rule gives a rate proportional to $|M|^2$, this gives:

   $$
   W_\text{em}\propto|M_0|^2(n+1)
   $$

   This step is done to show explicitly that the emission rate splits into two additive contributions: an $n$-independent piece (spontaneous emission, present even with zero photons) and an $n$-proportional piece (stimulated emission).

4. **Set up the absorption process.**

   $$
   |g;n\rangle \ \longrightarrow\ |e;n-1\rangle
   $$

   Take the initial state as a ground-state atom with $n$ photons, and the final state as the excited atom with one fewer photon. This mirrors step 1 for the reverse process.

5. **Evaluate the absorption matrix element and rate.** Acting with $H_I\hat a$ and using the lowering-operator property $\hat a|n\rangle=\sqrt n|n-1\rangle$ gives:

   $$
   M_{1\to2}=\sqrt n\,M_0, \qquad W_\text{abs}\propto|M_0|^2\,n
   $$

   This step is done to show that absorption, unlike emission, has no photon-independent term at all — it is impossible to absorb a photon that isn't there, so the rate vanishes exactly when $n=0$, in contrast to emission which survives even in the vacuum.

6. **Convert photon number to energy density and match Einstein's phenomenology.**

   $$
   u(\omega)=\frac{\hbar\omega^3}{\pi^2c^3}\,n(\omega)
   $$

   Using this to convert mean photon number to the classical energy density, the quantum rates $W_\text{em}\propto(n+1)$ and $W_\text{abs}\propto n$ reproduce exactly the phenomenological forms $A(\langle n\rangle+1)$ and $A\langle n\rangle$ that Einstein's rate equations require, without ever assuming the atoms are in thermal equilibrium with the field. This final step is done because it confirms that $A$ and $B$ are genuinely intrinsic properties of the atom (and the vacuum), not artifacts of the equilibrium argument used to first discover their ratio.

## Result

$$
W_\text{em} \propto |M_0|^2(n+1), \qquad W_\text{abs} \propto |M_0|^2\,n \qquad\Longrightarrow\qquad B_{21}=B_{12}=B,\ \ \frac{A}{B}=\frac{\hbar\omega^3}{\pi^2c^3}
$$

## Where It's Used

**Concept:** [Einstein Coefficients](Einstein%20Coefficients.md)

---

## Links

**Related:** [Plancks Law](Plancks%20Law.md), [Einstein Coefficients](Einstein%20Coefficients.md)
