---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The frequency spacing between adjacent ring-resonator resonances, $\Delta\omega_{FSR}=2\pi c/(L\,n_g)$, showing that it is the **group** index $n_g$ — not the phase index $n_{eff}$ — that sets the spacing.

## Starting Point

- Ring of round-trip length $L$, effective index $n_{eff}(\omega)$.
- Resonance condition: the round-trip phase is a multiple of $2\pi$, $\dfrac{\omega_m}{c}\,n_{eff}(\omega_m)\,L=2\pi m$ with integer $m$.
- Linear structural dispersion over one FSR: $n_{eff}(\omega)\approx n_{eff}(\omega_m)+\dfrac{dn_{eff}}{d\omega}\,(\omega-\omega_m)$.
- Group index definition $n_g=n_{eff}+\omega\,dn_{eff}/d\omega$ (from [Structural Dispersion and Group Index](Structural%20Dispersion%20and%20Group%20Index.md)).

## Full Derivation

1. **Write the resonance condition for the next mode.**

   $$
   L\,\frac{\omega_m+\Delta\omega_{FSR}}{c}\left[n_{eff}(\omega_m)+\frac{dn_{eff}}{d\omega}\,\Delta\omega_{FSR}\right]=2\pi(m+1)
   $$

   The resonance one step up in $m$ sits at $\omega_m+\Delta\omega_{FSR}$; its round-trip phase must equal $2\pi(m+1)$. The effective index is evaluated at the shifted frequency using the linear expansion.

2. **Expand the product on the left.**

   $$
   \frac{L}{c}\left[\omega_m n_{eff}(\omega_m)+\Delta\omega_{FSR}\,n_{eff}(\omega_m)+\omega_m\frac{dn_{eff}}{d\omega}\Delta\omega_{FSR}+\frac{dn_{eff}}{d\omega}\Delta\omega_{FSR}^{\,2}\right]=2\pi(m+1)
   $$

   Multiplying out the two brackets produces four terms: the zeroth-order term, two terms linear in $\Delta\omega_{FSR}$, and one quadratic term.

3. **Subtract the $\omega_m$ resonance condition.**

   $$
   \frac{L}{c}\left[\Delta\omega_{FSR}\,n_{eff}(\omega_m)+\omega_m\frac{dn_{eff}}{d\omega}\Delta\omega_{FSR}+\frac{dn_{eff}}{d\omega}\Delta\omega_{FSR}^{\,2}\right]=2\pi
   $$

   The zeroth-order term $\dfrac{L}{c}\omega_m n_{eff}(\omega_m)=2\pi m$ cancels against the $2\pi m$ on the right, leaving $2\pi(m+1)-2\pi m=2\pi$.

4. **Drop the quadratic term and identify the group index.**

   $$
   \frac{L}{c}\left[n_{eff}(\omega_m)+\omega_m\frac{dn_{eff}}{d\omega}\right]\Delta\omega_{FSR}=2\pi
   $$

   $\Delta\omega_{FSR}$ is small compared with $\omega_m$, so the term $\propto\Delta\omega_{FSR}^2$ is second order and is discarded. The bracket that multiplies the linear term is exactly the group index $n_g$.

5. **Solve for the FSR.**

   $$
   \Delta\omega_{FSR}=\frac{2\pi c}{L\,n_g}
   $$

   Rearranging the previous line. Dividing by $2\pi$ gives the ordinary-frequency form $\Delta\nu_{FSR}=c/(L\,n_g)=1/\tau_{RT}$, the inverse round-trip time.

## Result

$$
\Delta\omega_{FSR}=\frac{2\pi c}{L\,n_g},\qquad
\Delta\nu_{FSR}=\frac{c}{L\,n_g}=\frac{1}{\tau_{RT}},\qquad
n_g=n_{eff}+\omega\frac{\partial n_{eff}}{\partial\omega}
$$

The FSR depends on the group index, so in HIC rings (strong structural dispersion) it is 25–30% smaller than the naive $2\pi c/(L\,n_{eff})$ estimate.

## Where It's Used

**Concept:** [Free Spectral Range](Free%20Spectral%20Range.md)

---

## Links

**Related:** [Structural Dispersion and Group Index](Structural%20Dispersion%20and%20Group%20Index.md), [Ring Resonator](Ring%20Resonator.md)
