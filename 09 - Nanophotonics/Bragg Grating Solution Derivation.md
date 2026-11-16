---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

Solution of the counter-propagating coupled-mode equations for a Bragg grating of length $L$: the field profiles $A(z)$, $B(z)$, the reflection coefficient, and the stop-band in which the propagation coefficient becomes complex.

## Starting Point

- Counter-propagating coupled equations (from [Grating-Assisted Coupling Derivation](Grating-Assisted%20Coupling%20Derivation.md)): $\dfrac{dA}{dz}=\kappa^*Be^{i2\Delta\beta z}$, $\dfrac{dB}{dz}=\kappa Ae^{-i2\Delta\beta z}$, with $A\equiv A_s^{(+)}$, $B\equiv A_s^{(-)}$, $\Delta\beta=\beta_s-\frac{\pi}{\Lambda}q$.
- Boundary conditions: light enters at one side, $A(0)=1$, and nothing enters from the other, $B(L)=0$.
- Unperturbed dispersion $\beta(\omega)=n_{eff}\omega/c$, with $n_{eff}$ frequency independent.

## Full Derivation

1. **Eliminate $B$.**

   $$
   A_{zz}-2i\Delta\beta A_z-|\kappa|^2A=0
   $$

   Substituting the two first-order equations into each other gives one second-order equation for $A$. With constant coefficients, the ansatz $A\propto\exp(\gamma z)$ applies.

2. **Solve for the eigenvalues.**

   $$
   \gamma=i\Delta\beta\pm\sqrt{|\kappa|^2-\Delta\beta^2}=\pm S+i\Delta\beta
   $$

   This defines $S=\sqrt{|\kappa|^2-\Delta\beta^2}$. It is real when $|\kappa|>|\Delta\beta|$ (exponential solutions) and imaginary when $|\kappa|<|\Delta\beta|$ (propagating solutions).

3. **General solution for $A$ and $B$.**

   $$
   A=\left(A_0e^{Sz}+B_0e^{-Sz}\right)e^{i\Delta\beta z},\qquad
   B=\frac{e^{-i\Delta\beta z}}{\kappa^*}\left[A_0e^{Sz}(S+i\Delta\beta)+B_0e^{-Sz}(-S+i\Delta\beta)\right]
   $$

   $B$ follows from $A$ through the first coupled equation.

4. **Apply the boundary conditions.**

   $$
   A_0+B_0=1,\qquad B(L)=\frac{e^{-i\Delta\beta L}}{\kappa^*}\left[A_0e^{SL}(S+i\Delta\beta)+B_0e^{-SL}(-S+i\Delta\beta)\right]=0
   $$

   $A(0)=1$ fixes the sum of the constants, and $B(L)=0$ (no incident wave from the far end) gives the second linear equation.

5. **Solve for the constants.**

   $$
   A_0=\frac{\tfrac12e^{-SL}(S-i\Delta\beta)}{S\cosh(SL)+i\Delta\beta\sinh(SL)},\qquad
   B_0=\frac{\tfrac12e^{SL}(S+i\Delta\beta)}{S\cosh(SL)+i\Delta\beta\sinh(SL)}
   $$

   Substituting back gives the profiles in the next step.

6. **Field profiles.**

   $$
   A(z)=\frac{S\cosh[S(L-z)]+i\Delta\beta\sinh[S(L-z)]}{S\cosh(SL)+i\Delta\beta\sinh(SL)}e^{i\Delta\beta z},\qquad
   B(z)=\frac{\kappa\sinh[S(L-z)]}{S\cosh(SL)+i\Delta\beta\sinh(SL)}e^{-i\Delta\beta z}
   $$

7. **Reflection coefficient.**

   $$
   r=\frac{B(0)}{A(0)}=\frac{\kappa\sinh(SL)}{S\cosh(SL)+i\Delta\beta\sinh(SL)}
   $$

   At $\Delta\beta=0$, $S=|\kappa|$ and $|r|=\tanh(|\kappa|L)$.

8. **Stop-band.**

   $$
   |\Delta\beta|=|\beta-\beta_0|<\kappa\;\Rightarrow\;\frac{n_{eff}}{c}|\omega-\omega_0|<|\kappa|\;\Rightarrow\;\Delta\omega_{BG}=\frac{2|\kappa|c}{n_{eff}}
   $$

   Within $-\kappa<\Delta\beta<\kappa$ there are no propagating waves — the optical bandgap. With $\beta_0=\frac{n_{eff}}{c}\omega_0=\frac{\pi q}{\Lambda}$ the band centre sits at $\omega_0=\frac{\pi q}{\Lambda}\frac{c}{n_{eff}}=\frac{2\pi c}{\lambda_0}$, so a grating designed to reflect $\lambda_0$ needs $\Lambda=\frac{q\lambda_0}{2n_{eff}}$.

9. **Band diagram.**

   $$
   \beta'=\beta_0\mp iS=\beta_0\mp i\frac{n_{eff}}{c}\sqrt{\omega_\kappa^2-(\omega-\omega_0)^2},\qquad\omega_\kappa=\frac{c}{n_{eff}}|\kappa|
   $$

   The forward wave is $e^{-i\beta z}e^{\gamma z}=e^{-i(\beta_0-iS)z}$, so the forward and backward waves have $\beta'=\beta_0\mp iS$. Inside the gap $\mathrm{Re}(\beta')=\beta_0$ and $\mathrm{Im}(\beta')$ is the decay constant; outside the gap $\mathrm{Im}(\beta')=0$ and $\mathrm{Re}(\beta')=\beta_0\pm\frac{n_{eff}}{c}\sqrt{(\omega-\omega_0)^2-\omega_\kappa^2}$.

## Result

$$
\Lambda=\frac{q\lambda_0}{2n_{eff}},\qquad\Delta\omega_{BG}=\frac{2|\kappa|c}{n_{eff}},\qquad|r|_{\Delta\beta=0}=\tanh(|\kappa|L)
$$

## Where It's Used

**Concept:** [Waveguide Bragg Grating](Waveguide%20Bragg%20Grating.md)

---

## Links

**Related:** [Grating-Assisted Coupling Derivation](Grating-Assisted%20Coupling%20Derivation.md), [DBR Transfer Matrix Derivation](DBR%20Transfer%20Matrix%20Derivation.md)
