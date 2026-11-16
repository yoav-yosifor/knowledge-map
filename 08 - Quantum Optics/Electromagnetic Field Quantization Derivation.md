---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The electromagnetic Hamiltonian as a sum of independent [quantum harmonic oscillators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md), one per field mode, starting from Maxwell's equations in free space.

## Starting Point

- Maxwell's equations in free space, $\rho=0,\ \vec J=0$
- $\vec B=\nabla\times\vec A$, $\vec E=-\nabla\phi-\partial_t\vec A$
- Vector identity $\nabla\times(\nabla\times\vec A)=\nabla(\nabla\cdot\vec A)-\nabla^2\vec A$

## Full Derivation

1. **Substitute the potentials.**

   $$
   \vec B=\nabla\times\vec A, \qquad \vec E=-\nabla\phi-\partial_t\vec A
   $$

   Substituting these into the remaining Maxwell equations gives coupled equations of motion for $\vec A$ and $\phi$. Because $\nabla\cdot\vec B=0$ is automatically satisfied by $\vec B=\nabla\times\vec A$, working with the potentials reduces the original four coupled field equations to two, and opens up the freedom to choose a convenient gauge.

2. **Note the gauge freedom.**

   $$
   \vec A'=\vec A+\nabla\chi, \qquad \phi'=\phi-\partial_t\chi
   $$

   This leaves the physical fields $\vec E,\vec B$ unchanged; choose $\chi$ so that $\nabla^2\chi=-\nabla\cdot\vec A$, fixing the Coulomb gauge $\nabla\cdot\vec A=0$. The potentials themselves are not unique, so this freedom is used deliberately to pick the gauge that makes the remaining equations as simple as possible — the Coulomb gauge removes the purely longitudinal part of $\vec A$.

3. With no free charges or currents and the Coulomb gauge imposed, the coupled equations decouple into a pure wave equation for $\vec A$ and Laplace's equation for $\phi'$, whose only solution in free space with no static charges is $\phi'=0$. Once there is nothing to source a scalar potential, all of the field's dynamics is carried entirely by the vector potential.

4. **Expand in plane-wave modes.**

   $$
   \partial_t^2 A_{\vec k,\lambda}=-\omega_k^2 A_{\vec k,\lambda}, \qquad \omega_k=c|\vec k|
   $$

   Expanding $\vec A$ in plane-wave eigenmodes labeled by $(\vec k,\lambda)$, with two transverse polarizations enforced by the Coulomb gauge, and substituting back shows each mode amplitude obeys this equation — a harmonic-oscillator equation. Because the wave equation is linear, any solution can be built from a sum of independent plane waves, and substituting a single plane wave back in shows each one behaves exactly like a mechanical oscillator with its own frequency, already visible at the purely classical level.

5. **Compute the mode energy.**

   $$
   U=\sum_{\vec k,\lambda}\frac12\varepsilon_0V\omega_k^2\left(A_{\vec k,\lambda}A^*_{\vec k,\lambda}+A^*_{\vec k,\lambda}A_{\vec k,\lambda}\right)
   $$

   Computing $\vec E,\vec B$ from $\vec A$ for each mode and integrating $U=\frac12\int(E^2+B^2)\,d\vec r$ over the quantization volume, cross-mode terms vanish by orthogonality, leaving the expression above. Writing the energy symmetrically in $A$ and $A^*$ anticipates that these will become non-commuting operators, so the classical expression is deliberately kept free of any assumption about operator ordering.

6. **Promote to operators.**

   $$
   \hat H_\text{EM}=\sum_{\vec k,\lambda}\hbar\omega_k\left(\hat n_{\vec k,\lambda}+\tfrac12\right)
   $$

   Promoting the classical amplitudes to operators, $A_{\vec k,\lambda}\to\hat a_{\vec k,\lambda}$, $A^*_{\vec k,\lambda}\to\hat a^\dagger_{\vec k,\lambda}$, and imposing $[\hat a,\hat a^\dagger]=1$, using $\hat a\hat a^\dagger=\hat a^\dagger\hat a+1$ turns the symmetrized energy into the Hamiltonian above. This final replacement is the quantization step itself — every earlier step was purely classical bookkeeping needed to reach a Hamiltonian that looks exactly like a mechanical harmonic oscillator, so the same operator-promotion recipe used for a single oscillator can now be applied independently, mode by mode.

## Result

$$
\hat H_\text{EM} = \sum_{\vec k,\lambda}\varepsilon_0 V\omega_k^2\left(\hat n_{\vec k,\lambda}+\frac12\right) \;\;\longrightarrow\;\; \sum_{\vec k,\lambda}\hbar\omega_k\left(\hat n_{\vec k,\lambda}+\frac12\right)
$$

## Where It's Used

**Concept:** [Electromagnetic Field Quantization](Electromagnetic%20Field%20Quantization.md)

---

## Links

**Related:** [Harmonic Oscillator Ladder Operators](../06%20-%20Quantum%20Mechanics%201/Harmonic%20Oscillator%20Ladder%20Operators.md), [Quadrature Operators](Quadrature%20Operators.md)
