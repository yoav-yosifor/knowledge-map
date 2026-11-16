---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The $N$ discrete propagation constants (and mode profiles) of a linear array of $N$ identical, nearest-neighbor-coupled waveguides.

## Starting Point

- Nearest-neighbor coupled-mode equations for the array (identical waveguides, coupling coefficient $\kappa$ between adjacent guides only): $\dfrac{\partial\varepsilon_n}{\partial z}=-i\kappa\varepsilon_{n-1}-i\kappa\varepsilon_{n+1}$, $n=1,2,\dots,N$.
- Boundary condition: $\varepsilon_0=\varepsilon_{N+1}=0$ (no waveguides outside the array).

## Full Derivation

1. **Write the total field as a superposition of the individual waveguide modes with amplitudes $C_n$.**

   $$
   E(x,z)=\sum_{n=1}^N\varepsilon_n(z)E_n(x)e^{-i\beta_0z}=\sum_{n=1}^NC_ne^{-i\Delta z}E_n(x)e^{-i\beta_0z}=\sum_{n=1}^NC_nE_n(x)e^{-i\beta z},\qquad\Delta=\beta-\beta_0
   $$

   $\Delta$ is the shift of the array eigenmode's propagation constant away from the individual waveguide's own propagation constant $\beta_0$.

2. **Substitute into the set of nearest-neighbor coupled differential equations to get a set of difference equations.**

   $$
   \Delta C_n=\kappa C_{n-1}+\kappa C_{n+1}
   $$

   This is the discrete (array-index) analog of the two-waveguide coupled-mode equations — each guide couples only to its immediate left and right neighbors.

3. **Try a plane-wave solution along the array index $n$.**

   $$
   C_n^S=A\cdot e^{-iSn}
   $$

   Substituting into the difference equation and dividing through by the common factor gives the dispersion relation.

4. **Read off the dispersion relation.**

   $$
   \Delta=2\kappa\cos(S)
   $$

   Both $S$ and $-S$ solve this relation, so the general solution is $C_n^S=A\cdot e^{-iSn}+B\cdot e^{iSn}$. Without boundary conditions, any $S$ in $-2\kappa<\Delta<2\kappa$ appears to be allowed.

5. **Apply the boundary condition $C_0=C_{N+1}=0$.**

   $$
   C_n^S=\sin(Sn),\qquad S=\frac{m\pi}{N+1},\qquad m=1,2,\dots,N
   $$

   Requiring the amplitude to vanish just outside both ends of the finite array (as if waveguides "0" and "$N+1$" exist but carry no field) forces the general solution into a sine standing wave and quantizes $S$ into exactly $N$ allowed values.

6. **Substitute back to get the quantized propagation-constant shifts.**

   $$
   \Delta_m=2\kappa\cos\!\left(\frac{m\pi}{N+1}\right),\qquad m=1,2,\dots,N
   $$

   The array of $N$ waveguides therefore has exactly $N$ discrete supermodes, spread over a band of width $4\kappa$ centered on the single-waveguide propagation constant $\beta_0$.

## Result

$$
\Delta_m=2\kappa\cos\!\left(\frac{m\pi}{N+1}\right),\qquad m=1,2,\dots,N
$$

## Where It's Used

**Concept:** [Waveguide Array Supermodes](Waveguide%20Array%20Supermodes.md)

---

## Links

**Related:** [Coupled Waveguide Supermodes Derivation](Coupled%20Waveguide%20Supermodes%20Derivation.md)
