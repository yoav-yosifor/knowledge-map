---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The time-domain rate equation for a ring resonator, $\dfrac{dA_1}{dt}=-i\kappa_t A_{in}-\dfrac{\gamma}{2}A_1$, starting from the frequency-domain all-pass transfer function, and the identification $\kappa_t=\sqrt{\kappa}/\tau_{RT}$, $\gamma=(\kappa+\alpha)/\tau_{RT}$. A parallel derivation from a series RLC circuit is given as a cross-check.

## Starting Point

- All-pass filter relation between the circulating and input fields (from [All-Pass Ring Transfer Function Derivation](All-Pass%20Ring%20Transfer%20Function%20Derivation.md)):
  $$\left(1-\sqrt{(1-\kappa)(1-\alpha)}\,e^{-i\Delta\omega/\Delta\nu_{FSR}}\right)E_1=-i\sqrt{\kappa}\,E_{in}$$
- SVEA (slowly varying envelope): $E_{in}=A_{in}(t)e^{i\omega_0t}$, $E_1=A_1(t)e^{i\omega_0t}$, $E_{out}=A_{out}(t)e^{i\omega_0t}$, with $\omega_0$ a resonance.
- Fourier correspondence for a slowly varying envelope: multiplication by $i\Delta\omega$ in the frequency domain $\leftrightarrow$ $\dfrac{d}{dt}$ in the time domain.
- $\tau_{RT}=1/\Delta\nu_{FSR}$; high-$Q$ regime means $\kappa,\alpha\ll1$.

## Full Derivation

1. **Linearize the round-trip phase factor near resonance.**

   $$
   e^{-i\Delta\omega/\Delta\nu_{FSR}}\approx1-i\frac{\Delta\omega}{\Delta\nu_{FSR}}
   $$

   Close to a resonance the detuning $\Delta\omega$ is small compared with $\Delta\nu_{FSR}$, so the exponential is expanded to first order.

2. **Substitute and separate the two terms.**

   $$
   \left(1-\sqrt{(1-\kappa)(1-\alpha)}\right)A_1+i\,\frac{\sqrt{(1-\kappa)(1-\alpha)}}{\Delta\nu_{FSR}}\,\Delta\omega\,A_1=-i\sqrt{\kappa}\,A_{in}
   $$

   Insert the linearized factor into the APF relation and expand. The common $e^{i\omega_0t}$ carrier divides out, leaving the envelopes. One term is proportional to $A_1$, the other to $\Delta\omega\,A_1$.

3. **Replace $i\Delta\omega A_1$ by a time derivative.**

   $$
   \frac{\sqrt{(1-\kappa)(1-\alpha)}}{\Delta\nu_{FSR}}\,\frac{dA_1}{dt}=-\left(1-\sqrt{(1-\kappa)(1-\alpha)}\right)A_1-i\sqrt{\kappa}\,A_{in}
   $$

   Using $i\Delta\omega A_1\leftrightarrow dA_1/dt$. This turns the algebraic (frequency-domain) relation into a first-order ODE for the envelope.

4. **Divide through to isolate $dA_1/dt$.**

   $$
   \frac{dA_1}{dt}=-\frac{i\sqrt{\kappa}\,\Delta\nu_{FSR}}{\sqrt{(1-\kappa)(1-\alpha)}}\,A_{in}-\frac{1-\sqrt{(1-\kappa)(1-\alpha)}}{\sqrt{(1-\kappa)(1-\alpha)}}\,\Delta\nu_{FSR}\,A_1
   $$

   This is the exact near-resonance rate equation. It already has the structure "drive term $\propto A_{in}$" plus "decay term $\propto A_1$".

5. **Take the high-$Q$ limit.**

   $$
   \sqrt{(1-\kappa)(1-\alpha)}\approx1,\qquad
   1-\sqrt{(1-\kappa)(1-\alpha)}\approx\tfrac12(\kappa+\alpha)
   $$

   For $\kappa,\alpha\ll1$, expand the square root: $\sqrt{(1-\kappa)(1-\alpha)}\approx1-\tfrac12(\kappa+\alpha)$. The denominator $\to1$; the numerator of the decay coefficient $\to\tfrac12(\kappa+\alpha)$.

6. **Write the reduced rate equation.**

   $$
   \frac{dA_1}{dt}=-i\sqrt{\kappa}\,\Delta\nu_{FSR}\,A_{in}-\tfrac12(\kappa+\alpha)\,\Delta\nu_{FSR}\,A_1
   =-i\,\frac{\sqrt{\kappa}}{\tau_{RT}}\,A_{in}-\tfrac12\,\frac{\kappa+\alpha}{\tau_{RT}}\,A_1
   $$

   Substituting the step-5 approximations and then $\Delta\nu_{FSR}=1/\tau_{RT}$.

7. **Match to the canonical rate-equation form.**

   $$
   \frac{dA_1}{dt}=-i\kappa_t\,A_{in}-\frac{\gamma}{2}\,A_1
   \quad\Longrightarrow\quad
   \kappa_t=\frac{\sqrt{\kappa}}{\tau_{RT}},\qquad
   \gamma=\frac{\kappa+\alpha}{\tau_{RT}}
   $$

   Comparing term by term. The coupling rate $\kappa_t$ is the field coupling coefficient $\sqrt{\kappa}$ spread over one round trip; the linewidth $\gamma$ is the total fractional power lost (coupling + internal) per round trip.

8. **Cross-check — the same equation from a series RLC circuit.**

   $$
   \ddot v_c+\gamma\,\dot v_c+\omega_0^2\,v_c=\omega_0^2\,v(t),\qquad \omega_0^2=\frac{1}{LC},\ \ \gamma=\frac{R}{L}
   $$

   Kirchhoff's voltage law for a driven series $LCR$ loop ($v_c+L\dot i+iR=v$, $i=C\dot v_c$) gives this damped-driven-oscillator equation.

9. **Apply SVEA to the RLC equation.**

   $$
   v(t)=v_d(t)e^{i\omega_0t},\quad v_c(t)=v_0(t)e^{i\omega_0t}\ \Longrightarrow\
   \frac{dv_0}{dt}=-i\,\frac{\omega_0}{2}\,v_d-\frac{\gamma}{2}\,v_0
   $$

   Insert the envelopes; the $\ddot v_0$ and $\gamma\dot v_0$ terms are negligible (slow envelope, $\gamma\ll\omega_0$), and $-\omega_0^2v_0+\omega_0^2v_0$ cancels. What remains is first order in $dv_0/dt$ — identical in form to the ring rate equation.

10. **Restore the input coupler in the circuit picture.**

    $$
    \frac{dv_0}{dt}=-i\,\kappa_t\,v_d-\frac{\gamma}{2}\,v_0,\qquad
    \kappa_t=\frac{\omega_0}{2}\,\frac{R}{R+R_S}
    $$

    The RLC loop has no analogue of the bus coupler; adding a large source resistor $R_S$ so the drive the loop actually sees is $v_{eff}=\dfrac{R}{R+R_S}v_d$ reproduces a tunable coupling rate $\kappa_t$, completing the analogy.

## Result

$$
\frac{dA_1}{dt}=-i\kappa_t\,A_{in}-\frac{\gamma}{2}\,A_1,\qquad
\kappa_t=\frac{\sqrt{\kappa}}{\tau_{RT}},\qquad
\gamma=\frac{\kappa+\alpha}{\tau_{RT}}
$$

Valid for high $Q$ and near-resonance operation (SVEA). The same first-order form governs a driven, damped harmonic oscillator and a series RLC circuit — the ring is one more realization of that universal equation.

## Where It's Used

**Concept:** [Ring Resonator Rate Equations](Ring%20Resonator%20Rate%20Equations.md)

---

## Links

**Related:** [All-Pass Ring Transfer Function Derivation](All-Pass%20Ring%20Transfer%20Function%20Derivation.md), [Cavity Q Factor Derivation](Cavity%20Q%20Factor%20Derivation.md), [Coupled Mode Theory](Coupled%20Mode%20Theory.md)
