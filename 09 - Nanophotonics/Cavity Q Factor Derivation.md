---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The ring resonator's loaded and intrinsic $Q$ factors, obtained from the cavity photon lifetime $\tau_c$ — first via the time-domain rate equation with the input switched off, then, as a cross-check, from the per-round-trip power loss.

## Starting Point

- Near-resonance rate equation for the circulating envelope (from [Ring Resonator Rate Equations](Ring%20Resonator%20Rate%20Equations.md)):
  $$\frac{dA_1}{dt}=-\frac{i\sqrt{\kappa}\,\Delta\nu_{FSR}}{\sqrt{(1-\kappa)(1-\alpha)}}A_{in}-\frac{1-\sqrt{(1-\kappa)(1-\alpha)}}{\sqrt{(1-\kappa)(1-\alpha)}}\,\Delta\nu_{FSR}\,A_1$$
- Definition of $Q$ through energy decay: $|E(t)|^2=E_0^2e^{-t/\tau_c}$ and $Q=\omega_0\tau_c$.
- Round-trip time $\tau_{RT}=L/(c/n_g)=1/\Delta\nu_{FSR}$.
- For a resonance at $\omega_0$: $Q\approx\lambda/\lambda_{FWHM}$.

## Full Derivation

1. **Switch off the input.**

   $$
   \frac{dA_1}{dt}=-\frac{1-\sqrt{(1-\kappa)(1-\alpha)}}{\sqrt{(1-\kappa)(1-\alpha)}}\,\Delta\nu_{FSR}\,A_1\equiv-\frac{A_1}{2\tau_c}
   $$

   With the ring in steady state and $A_{in}$ suddenly set to zero, only the decay term survives. Its coefficient defines the amplitude decay rate $1/2\tau_c$ (the factor 2 because energy $\propto|A_1|^2$ decays twice as fast as the amplitude).

2. **Read off the cavity lifetime.**

   $$
   \frac{1}{2\tau_c}=\frac{1-\sqrt{(1-\kappa)(1-\alpha)}}{\sqrt{(1-\kappa)(1-\alpha)}}\,\Delta\nu_{FSR}
   \quad\Longrightarrow\quad
   \tau_c=\frac{\sqrt{(1-\kappa)(1-\alpha)}}{2\left[1-\sqrt{(1-\kappa)(1-\alpha)}\right]\Delta\nu_{FSR}}
   $$

   Just inverting the coefficient. Both $\kappa$ (power leaking back through the coupler) and $\alpha$ (internal loss) shorten $\tau_c$ — they are the two ways energy leaves the resonator.

3. **Form the loaded $Q$.**

   $$
   Q=\omega_0\tau_c=\frac{\omega_0\,\sqrt{(1-\alpha)(1-\kappa)}}{2\left[1-\sqrt{(1-\alpha)(1-\kappa)}\right]\Delta\nu_{FSR}}\approx\frac{\lambda}{\lambda_{FWHM}}
   $$

   Multiplying $\tau_c$ by $\omega_0$. This is the **loaded** $Q$: it includes the bus coupling, so it is what a transmission measurement of the notch linewidth returns.

4. **Take the $\kappa\to0$ limit for the intrinsic $Q$.**

   $$
   Q_{int}=\frac{\omega_0\,\sqrt{1-\alpha}}{2\left[1-\sqrt{1-\alpha}\right]\Delta\nu_{FSR}}
   $$

   Setting $\kappa=0$ removes the coupler-leakage channel, leaving the $Q$ set purely by internal loss $\alpha$ — the best achievable $Q$ for that ring.

5. **Small-loss approximation.**

   $$
   1-\sqrt{1-\alpha}\approx\frac{\alpha}{2}\quad\Longrightarrow\quad Q_{int}\approx\frac{\omega_0}{\alpha\,\Delta\nu_{FSR}}
   $$

   Expanding $\sqrt{1-\alpha}\approx1-\alpha/2$ for $\alpha\ll1$ and using $\sqrt{1-\alpha}\approx1$ in the numerator.

6. **Cross-check: energy decay from the per-round-trip loss.**

   $$
   e^{-\tau_{RT}/\tau_c}=1-\alpha\quad\Longrightarrow\quad\tau_c=-\frac{1}{\ln(1-\alpha)\,\Delta\nu_{FSR}}
   $$

   Each round trip the stored power is multiplied by $1-\alpha$; assuming exponential decay in time, one round-trip interval $\tau_{RT}=1/\Delta\nu_{FSR}$ corresponds to the factor $e^{-\tau_{RT}/\tau_c}$. Equate and solve for $\tau_c$.

7. **Recover the same intrinsic $Q$.**

   $$
   Q_{int}=\omega_0\tau_c=\frac{\omega_0}{\left|\ln(1-\alpha)\right|\Delta\nu_{FSR}}\ \xrightarrow[\ \alpha\ll1\ ]{}\ \frac{\omega_0}{\alpha\,\Delta\nu_{FSR}}
   $$

   Using $\ln(1-\alpha)\approx-\alpha$ for small $\alpha$ reproduces the step-5 result — the two routes agree.

## Result

$$
Q=\frac{\omega_0\sqrt{(1-\alpha)(1-\kappa)}}{2\left[1-\sqrt{(1-\alpha)(1-\kappa)}\right]\Delta\nu_{FSR}}
\quad\xrightarrow[\ \kappa\to0\ ]{}\quad
Q_{int}=\frac{\omega_0\sqrt{1-\alpha}}{2\left[1-\sqrt{1-\alpha}\right]\Delta\nu_{FSR}}\approx\frac{\omega_0}{\alpha\,\Delta\nu_{FSR}}
$$

Because the loaded $Q$ contains both $\kappa$ and $\alpha$, a linewidth measurement gives the loaded value; the intrinsic $Q$ (material/bend loss only) is extracted by measuring several rings of different gap and extrapolating $\kappa\to0$.

## Where It's Used

**Concept:** [Cavity Q Factor and Finesse](Cavity%20Q%20Factor%20and%20Finesse.md)

---

## Links

**Related:** [Ring Resonator Rate Equations](Ring%20Resonator%20Rate%20Equations.md), [Free Spectral Range](Free%20Spectral%20Range.md), [Ring Resonator](Ring%20Resonator.md)
