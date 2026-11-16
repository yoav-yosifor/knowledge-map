---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The propagation constants and mode profiles of the two supermodes of a compound waveguide built from two coupled single-mode waveguides.

## Starting Point

- Each waveguide's own mode satisfies its unperturbed equation: $\left[\partial^2/\partial x^2+k_0^2(n_s^2+\Delta n_{a,b}^2)\right]E_{a,b}=\beta_{a,b}^2E_{a,b}$.
- Power-normalization: $\int_{-\infty}^{\infty}|E_{a,b}|^2\,dx=1$.
- Overlap integral: $I=\int_{-\infty}^{\infty}E_b^*(x)E_a(x)\,dx$.

## Full Derivation

1. **Write the trial eigenmode as a fixed superposition of the two waveguides' own modes.**

   $$
   E(x,z)=\left[C_aE_a(x)+C_bE_b(x)\right]e^{i(\omega t-\beta z)}
   $$

   Unlike the CMT picture (where $A(z),B(z)$ vary along $z$), here $C_a,C_b$ and $\beta$ are constants — this is a genuine eigenmode of the *combined* structure, not a beat pattern between two separate modes.

2. **Substitute into the wave equation and use each waveguide's own mode equation.**

   $$
   C_a\left[\beta_a^2-\beta^2+k_0^2\Delta n_b^2(x)\right]E_a(x)+C_b\left[\beta_b^2-\beta^2+k_0^2\Delta n_a^2(x)\right]E_b(x)=0
   $$

   This splits into two separate terms — one carrying $E_a(x)$, the other $E_b(x)$ — because the trial eigenmode in Step 1 is a *sum* of two independent terms, and substituting a sum into the (linear) wave equation keeps each summand's contribution separate; no term mixes $C_a$ with $E_b$ or $C_b$ with $E_a$. Each waveguide's own unperturbed wave equation then cancels the parts of each term that don't involve the *other* waveguide's index perturbation, leaving only the cross-coupling terms shown.

3. **Project onto $E_a^*$ and $E_b^*$, integrate over $x$, and use the normalization condition.**

   $$
   \begin{pmatrix}\beta_a^2-\beta^2+K_a & J_a+I^*(\beta_b^2-\beta^2)\\ J_b+I(\beta_a^2-\beta^2) & \beta_b^2-\beta^2+K_b\end{pmatrix}\begin{pmatrix}C_a\\C_b\end{pmatrix}=0
   $$

   where $J_a=k_0^2\int E_a^*\Delta n_a^2E_b\,dx$, $K_a=k_0^2\int E_a^*\Delta n_b^2E_a\,dx$ (and $J_b,K_b$ analogously). This is the eigenvalue problem for the compound-waveguide propagation constant $\beta$.

4. **Require a non-trivial solution: set the determinant of the matrix to zero.**

   $$
   \left[\beta_0^2-\beta^2+K\right]^2=\left[J+I(\beta_0^2-\beta^2)\right]^2
   $$

   This is the special case of two **identical** waveguides ($\beta_a=\beta_b=\beta_0$, $J_a=J_b=J$, $K_a=K_b=K$, $I=I^*$), giving a quadratic equation in $\beta$.

5. **Solve for the two eigenvalues.**

   $$
   \beta_1^2=\beta_0^2+\frac{K+J}{1+I},\qquad\beta_2^2=\beta_0^2+\frac{K-J}{1-I},\qquad E_1=\frac{1}{\sqrt{1+I}}(E_a+E_b),\qquad E_2=\frac{1}{\sqrt{|1-I|}}(E_a-E_b)
   $$

   The two eigenmodes are the symmetric ($E_1$) and antisymmetric ($E_2$) combinations of the individual waveguide modes.

6. **Cross-check against the simplified CMT picture directly.**

   $$
   \begin{vmatrix}-\gamma & \kappa\\ \kappa^* & -\gamma\end{vmatrix}=0\;\;\Rightarrow\;\;\gamma=\pm|\kappa|,\qquad E_1=\begin{pmatrix}1\\1\end{pmatrix},\qquad E_2=\begin{pmatrix}1\\-1\end{pmatrix}
   $$

   Using $E(z)=E_0e^{-i\gamma z}$ directly in the coupled-mode equations for identical waveguides ($\beta_a=\beta_b$, $M_{aa}=M_{bb}\Rightarrow\delta=0$) reproduces the same two eigenmodes, confirming the full eigenvalue problem and the simplified CMT picture agree: $\beta_{1,2}=\beta_0\pm|\kappa|$.

## Result

$$
\beta_{1,2}=\beta_0\pm|\kappa|,\qquad E_1=\frac{1}{\sqrt2}(E_a+E_b),\qquad E_2=\frac{1}{\sqrt2}(E_a-E_b)
$$

## Where It's Used

**Concept:** [Coupled Waveguide Supermodes](Coupled%20Waveguide%20Supermodes.md)

---

## Links

**Related:** [Coupled Mode Equations Derivation](Coupled%20Mode%20Equations%20Derivation.md)
