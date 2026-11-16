---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The steady-state field transfer functions of a single-bus ring (all-pass filter configuration): the circulating field $E_1/E_{in}$ and the through-port field $E_{out}/E_{in}$, plus their simplified near-resonance form in which the round-trip phase becomes $\varphi=\Delta\omega/\Delta\nu_{FSR}$.

## Starting Point

- Bus and ring are joined by a lossless directional coupler with power coupling coefficient $\kappa$ (from [Directional Coupler](Directional%20Coupler.md)):
  $$\begin{pmatrix}E_{out}\\E_1\end{pmatrix}=\begin{pmatrix}\sqrt{1-\kappa}&-i\sqrt{\kappa}\\-i\sqrt{\kappa}&\sqrt{1-\kappa}\end{pmatrix}\begin{pmatrix}E_{in}\\E_2\end{pmatrix}$$
  where $E_1$ is the field entering the ring just after the coupler and $E_2$ is the field returning to the coupler after one round trip.
- Round-trip propagation with loss: $E_2=E_1\sqrt{1-\alpha}\,e^{-i\varphi}$, where $\alpha$ is the fractional power loss per revolution and $\varphi=L k_0 n_{eff}(\omega)$ is the round-trip phase.
- Resonance condition $\dfrac{L}{c}\omega_0 n_{eff}(\omega_0)=2\pi m$ and group index $n_g=n_{eff}+\omega\,dn_{eff}/d\omega$.

## Full Derivation

1. **Write out the two coupler equations.**

   $$
   E_1=-i\sqrt{\kappa}\,E_{in}+\sqrt{1-\kappa}\,E_2,\qquad
   E_{out}=\sqrt{1-\kappa}\,E_{in}-i\sqrt{\kappa}\,E_2
   $$

   These are just the two rows of the coupler matrix. $E_1$ and $E_{out}$ are both driven by the input and by the field $E_2$ coming back around the ring.

2. **Close the loop.**

   $$
   E_1=-i\sqrt{\kappa}\,E_{in}+\sqrt{1-\kappa}\,\sqrt{1-\alpha}\,e^{-i\varphi}\,E_1
   $$

   Substitute the round-trip relation $E_2=E_1\sqrt{1-\alpha}\,e^{-i\varphi}$ into the first coupler equation. Now $E_1$ appears on both sides — the ring feeds itself.

3. **Solve for the circulating field.**

   $$
   E_1=\frac{-i\sqrt{\kappa}\,E_{in}}{1-\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\varphi}}
   $$

   Collecting the $E_1$ terms and dividing. The denominator $1-\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\varphi}$ is the resonant denominator: it becomes smallest when $\varphi$ is a multiple of $2\pi$, producing the field build-up.

4. **Solve for the through-port field.**

   $$
   E_{out}=\sqrt{1-\kappa}\,E_{in}-i\sqrt{\kappa}\left(\sqrt{1-\alpha}\,e^{-i\varphi}E_1\right)
   =\frac{\sqrt{1-\kappa}-\sqrt{1-\alpha}\,e^{-i\varphi}}{1-\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\varphi}}\,E_{in}
   $$

   Substitute $E_2=\sqrt{1-\alpha}\,e^{-i\varphi}E_1$ and then the step-3 result for $E_1$ into the second coupler equation; combine over the common denominator. The $-i\sqrt{\kappa}\cdot(-i\sqrt{\kappa})=-\kappa$ term combines with $\sqrt{1-\kappa}\left(1-\sqrt{(1-\kappa)(1-\alpha)}e^{-i\varphi}\right)$ in the numerator and simplifies using $1-\kappa+\kappa=1$.

5. **Expand the round-trip phase near a resonance.**

   $$
   \varphi=\frac{L}{c}\,n_{eff}(\omega)\,\omega\approx\frac{L}{c}(\omega_0+\Delta\omega)\left[n_{eff}(\omega_0)+\frac{dn_{eff}}{d\omega}\Delta\omega\right]
   $$

   Write $\omega=\omega_0+\Delta\omega$ with $\omega_0$ a resonance, and linearize $n_{eff}$ in $\Delta\omega$ (Taylor series in both $\omega$ and $n_{eff}$).

6. **Multiply out and drop the quadratic term.**

   $$
   \varphi\approx\frac{L}{c}\left\{\omega_0n_{eff}(\omega_0)+\Delta\omega\left[n_{eff}(\omega_0)+\omega_0\frac{dn_{eff}}{d\omega}\right]+\frac{dn_{eff}}{d\omega}\Delta\omega^2\right\}
   $$

   The first term is the resonance condition $\dfrac{L}{c}\omega_0n_{eff}(\omega_0)=2\pi m$ and drops out of $e^{-i\varphi}$ (it contributes only a $2\pi m$ phase). The bracket multiplying $\Delta\omega$ is the group index $n_g$. The $\Delta\omega^2$ term is second order and is discarded.

7. **Identify the reduced phase.**

   $$
   \varphi=\frac{L}{c}\,n_g\,\Delta\omega=\frac{\Delta\omega}{\Delta\nu_{FSR}}\pmod{2\pi}
   $$

   Using $\Delta\nu_{FSR}=c/(L\,n_g)$. So near resonance the ring's frequency response is governed entirely by the single detuning variable $\Delta\omega/\Delta\nu_{FSR}$.

## Result

$$
\frac{E_1}{E_{in}}=\frac{-i\sqrt{\kappa}}{1-\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}},\qquad
\frac{E_{out}}{E_{in}}=\frac{\sqrt{1-\kappa}-\sqrt{1-\alpha}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}}{1-\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}}
$$

The through-port magnitude $|E_{out}/E_{in}|$ is unity when $\alpha=0$ for all detunings (hence "all-pass"); loss turns the resonances into notches. The build-up intensity is
$$
\left|\frac{E_1}{E_{in}}\right|^2=\frac{\kappa}{1+(1-\kappa)(1-\alpha)-2\sqrt{(1-\kappa)(1-\alpha)}\cos\!\left(\Delta\omega/\Delta\nu_{FSR}\right)}
$$

## Where It's Used

**Concept:** [Ring Resonator](Ring%20Resonator.md)

---

## Links

**Related:** [Directional Coupler](Directional%20Coupler.md), [Critical Coupling](Critical%20Coupling.md), [Ring Resonator Rate Equations](Ring%20Resonator%20Rate%20Equations.md), [Free Spectral Range](Free%20Spectral%20Range.md)
