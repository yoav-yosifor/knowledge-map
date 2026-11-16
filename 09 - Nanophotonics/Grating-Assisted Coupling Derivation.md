---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The coupled-mode equations for two guided modes of a waveguide whose dielectric profile is weakly and periodically perturbed, with a coupling coefficient set by the $q$-th Fourier component of the perturbation and a phase mismatch $\Delta\beta$.

## Starting Point

- Perturbed permittivity: $\varepsilon_r'(\mathbf r)=\varepsilon_r(\mathbf r)+\Delta\varepsilon_r(\mathbf r)$, with $\Delta\varepsilon_r\ll\varepsilon_r$.
- Guided modes of the unperturbed waveguide satisfy $\left(\dfrac{d^2}{dx^2}-\beta_m^2\right)E_m+k_0^2\varepsilon_r(x)E_m=0$.
- Mode orthogonality: $\displaystyle\int_{-\infty}^{\infty}E_m E_s\,dx=\dfrac{2\omega\mu}{\beta_s}\delta_{ms}$.
- SVEA: $\left|\dfrac{d^2A_m}{dz^2}\right|\ll\left|2\beta_m\dfrac{dA_m}{dz}\right|$.
- Periodic perturbation: $\Delta\varepsilon_r(x,z)=\overline{\Delta\varepsilon_r}(x)\displaystyle\sum_q a_q e^{-i\frac{2\pi}{\Lambda}qz}$.

## Full Derivation

1. **Wave equation with the perturbation as a source.**

   $$
   \nabla^2E+k_0^2\varepsilon_r(\mathbf r)E=-k_0^2\Delta\varepsilon_r(\mathbf r)E
   $$

   Starting from $\nabla^2E+k_0^2(\varepsilon_r+\Delta\varepsilon_r)E=0$, the perturbation term is moved to the right-hand side, where it plays the role of a source driving the unperturbed waveguide.

2. **Expand in guided modes.**

   $$
   E=\sum_m A_m(z)E_m(x)\exp(-i\beta_m z)
   $$

   Only the guided modes are kept (the radiating modes are not included). The perturbation is assumed to make the amplitudes $A_m$ vary slowly with $z$.

3. **Substitute and cancel using the mode equation.**

   $$
   \sum_m\left[\left(\frac{d^2A_m}{dz^2}-2i\beta_m\frac{dA_m}{dz}\right)E_m\right]e^{-i\beta_m z}=-k_0^2\Delta\varepsilon_r(x,z)\sum_m A_m(z)E_m(x)e^{-i\beta_m z}
   $$

   The terms $-\beta_m^2E_m+\frac{d^2E_m}{dx^2}+k_0^2\varepsilon_rE_m$ vanish by each mode's own wave equation (crossed out on the slide), leaving only the derivatives of the amplitudes.

4. **Apply the SVEA.**

   $$
   2i\sum_m\left(\beta_m\frac{dA_m}{dz}\right)E_me^{-i\beta_m z}=k_0^2\Delta\varepsilon_r(x,z)\sum_m A_m(z)E_m(x)e^{-i\beta_m z}
   $$

   Dropping $d^2A_m/dz^2$ relative to $2\beta_m\,dA_m/dz$ turns the second-order equation into a first-order rate equation.

5. **Project onto mode $s$ with orthogonality.**

   $$
   \frac{dA_s^{(+)}}{dz}e^{-i\beta_sz}-\frac{dA_s^{(-)}}{dz}e^{i\beta_sz}=-\tfrac14 i\omega\varepsilon_0\sum_mA_me^{-i\beta_mz}\int\Delta\varepsilon_r(x,z)E_m(x)E_s(x)\,dx
   $$

   Here $A_s^{(\pm)}$ are the amplitudes of the forward and backward propagating waves sharing the same transverse profile. The perturbation couples any two modes; the right-hand side terms act as sources for the left-hand side.

6. **Pick out the phase-matched term.** Project on a specific $\beta$ by multiplying by $e^{i\beta_sz}$ and averaging, $\frac{\beta_s}{2\pi}\int_0^{2\pi/\beta_s}(\cdots)e^{i\beta_sz}dz$.

   $$
   \frac{\beta_s}{2\pi}\int\frac{dA_s^{(+)}}{dz}dz-\frac{\beta_s}{2\pi}\int\frac{dA_s^{(-)}}{dz}e^{2i\beta_sz}dz=-\tfrac14 i\omega\varepsilon_0\sum_mA_m\int dz\,e^{-i(\beta_m-\beta_s)z}\sum_qa_qe^{-i\frac{2\pi}{\Lambda}qz}\int\overline{\Delta\varepsilon_r}E_mE_s\,dx
   $$

   The $e^{2i\beta_sz}$ term averages to zero. On the right, the integral over $z$ averages to zero unless $\beta_m-\beta_s+\frac{2\pi}{\Lambda}q\approx0$ — the phase-matching condition. The periodic structure supplies the missing wavevector in units of $2\pi/\Lambda$ (equivalently, lattice momentum conservation).

7. **Keep the matched term and define $\kappa$.**

   $$
   \frac{dA_s^{(+)}}{dz}=-\tfrac14 i\omega\varepsilon_0A_m^{(+)}\int\overline{\Delta\varepsilon_r}(x)a_qE_m(x)E_s(x)\,dx\cdot e^{i\left(\beta_s-\beta_m-\frac{2\pi}{\Lambda}q\right)z}
   $$

   Defining $\kappa\equiv\tfrac14 i\omega\varepsilon_0\int\overline{\Delta\varepsilon_r}(x)a_qE_mE_s\,dx$ and $2\Delta\beta=\beta_s-\beta_m-\frac{2\pi}{\Lambda}q$ packages the overlap integral into one coupling constant, and the residual mismatch into one exponent. Repeating the procedure for $A_me^{-i\beta_mz}$ gives the partner equation.

## Result

$$
\frac{dA_s^{(+)}}{dz}=\kappa^*A_m^{(+)}(z)e^{i2\Delta\beta z},\qquad
\frac{dA_m^{(+)}}{dz}=\kappa A_s^{(+)}(z)e^{-i2\Delta\beta z},\qquad
\Delta\beta=\tfrac12(\beta_s-\beta_m)-\frac{\pi}{\Lambda}q
$$

with $\Delta\beta\ll\beta_s,\beta_m$. For $\beta_s=-\beta_m$ (counter-propagating) the pair couples $A_s^{(+)}$ and $A_s^{(-)}$:

$$
\frac{dA_s^{(+)}}{dz}=\kappa^*A_s^{(-)}(z)e^{i2\Delta\beta z},\qquad
\frac{dA_s^{(-)}}{dz}=\kappa A_s^{(+)}(z)e^{-i2\Delta\beta z},\qquad
\Delta\beta=\beta_s-\frac{\pi}{\Lambda}q
$$

## Where It's Used

**Concept:** [Grating-Assisted Mode Coupling](Grating-Assisted%20Mode%20Coupling.md)

---

## Links

**Related:** [Coupled Mode Equations Derivation](Coupled%20Mode%20Equations%20Derivation.md), [Bragg Grating Solution Derivation](Bragg%20Grating%20Solution%20Derivation.md)
