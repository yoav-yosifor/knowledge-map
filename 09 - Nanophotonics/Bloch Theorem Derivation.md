---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

In a 1D periodic structure the field takes the form of a plane wave $e^{-iKx}$ times a function with the period of the structure (1D proof from the lecture).

## Starting Point

- Periodic permittivity as a Fourier series:
  $$
  \varepsilon_r(x)=\varepsilon_r(x+\Lambda)\ \Rightarrow\ \varepsilon_r(x)=\sum_{n=-\infty}^{\infty}\varepsilon_ne^{-i\frac{2\pi}{\Lambda}nx}
  $$
- The field satisfies the wave equation $\nabla^2E+\varepsilon_r(x)k_0^2E=0$.
- The field as a Fourier integral: $E(x)=\int A(k)e^{-ikx}dk$.

## Full Derivation

1. **Substitute $E$ into the wave equation.**

   $$
   -\int k^2A(k)e^{-ikx}dk+k_0^2\int\sum_{m=-\infty}^{\infty}\varepsilon_me^{-i\frac{2\pi}{\Lambda}mx}A(k)e^{-ikx}dk=0
   $$

   The second derivative acts on $e^{-ikx}$ and gives $-k^2$; the permittivity multiplies the field, so each Fourier component of $\varepsilon_r$ multiplies the whole integrand. This is done to turn the differential equation into an equation on the amplitudes $A(k)$.

2. **Define a shifted wavenumber for the second term.**

   $$
   k'_m=k+\frac{2\pi}{\Lambda}m,\qquad dk'_m=dk
   $$

   (The slide writes $\tfrac{2\pi}{\lambda}m$; the surrounding equations require $\Lambda$, so it is transcribed as $\Lambda$ — likely a slide typo.) Then $e^{-i\frac{2\pi}{\Lambda}mx}e^{-ikx}=e^{-ik'_mx}$, so every term in the sum carries the same kind of exponential as the first term.

   $$
   -\int k^2A(k)e^{-ikx}dk+k_0^2\sum_{m=-\infty}^{\infty}\int\varepsilon_mA\!\left(k'_m-\frac{2\pi}{\Lambda}m\right)e^{-ik'_mx}dk'_m=0
   $$

3. **Relabel the dummy variable.**

   $$
   \int dk\left[k^2A(k)-k_0^2\sum_{m=-\infty}^{\infty}\varepsilon_mA\!\left(k-\frac{2\pi}{\Lambda}m\right)\right]e^{-ikx}=0
   $$

   Each integral in the sum runs over all of $k$-space and $k'_m$ is only a dummy variable, so it can be renamed $k$. This is done so that all terms share one integral and one exponential and can be combined.

4. **Require every Fourier component to vanish.**

   $$
   \forall k:\quad k^2A(k)-k_0^2\sum_{m=-\infty}^{\infty}\varepsilon_mA\!\left(k-\frac{2\pi}{\Lambda}m\right)=0
   $$

   A Fourier transform equals zero only if all its components are zero. This gives an infinite set of equations, one per $k$.

5. **Separate the equations into groups.** A given $k$ is coupled only to the wavenumbers $k-\tfrac{2\pi}{\Lambda}m$. Label each group by its smallest wavenumber $K$; the group contains $K-\tfrac{2\pi}{\Lambda}m$ only.

6. **Sum one group.**

   $$
   E(x)=\sum_mA\!\left(K-\frac{2\pi}{\Lambda}m\right)e^{-i\left(K-\frac{2\pi}{\Lambda}m\right)x}=e^{-iKx}\sum_mA\!\left(K-\frac{2\pi}{\Lambda}m\right)e^{i\frac{2\pi}{\Lambda}mx}=e^{-iKx}E_K(x)
   $$

   Factoring out $e^{-iKx}$ leaves a Fourier series in $e^{i\frac{2\pi}{\Lambda}mx}$, which is periodic with period $\Lambda$. That periodic remainder is the Bloch function $E_K$.

## Result

$$
E(x)=e^{-iKx}E_K(x),\qquad E_K(x)=\sum_mA\!\left(K-\frac{2\pi}{\Lambda}m\right)e^{i\frac{2\pi}{\Lambda}mx},\qquad E(x+\Lambda)=e^{-iK\Lambda}E(x)
$$

$K$ is the Bloch wavenumber (may be complex) and can be restricted to $-\tfrac{\pi}{\Lambda}<K<\tfrac{\pi}{\Lambda}$.

## Where It's Used

**Concept:** [Bloch Theorem](Bloch%20Theorem.md)

---

## Links

**Related:** [Reciprocal Lattice](Reciprocal%20Lattice.md)
