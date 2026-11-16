---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The coupled-mode equations governing the amplitudes of two weakly-coupled single-mode waveguides, derived from the full two-waveguide wave equation via perturbation theory and the SVEA.

## Starting Point

- Each waveguide's index profile is split into a shared background plus its own perturbation: $n^2(x)=n_s^2+\Delta n_a^2(x)+\Delta n_b^2(x)$, with $\Delta n_a^2$ nonzero only in core $a$ and $\Delta n_b^2$ nonzero only in core $b$.
- Each waveguide has its own unperturbed guided mode, satisfying $\left[\partial^2/\partial x^2+k_0^2(n_s^2+\Delta n_{a,b}^2)\right]E_{a,b}=\beta_{a,b}^2E_{a,b}$.
- Power-normalization condition: $\int_{-\infty}^{\infty}|E_{a,b}|^2\,dx=2\omega\mu/\beta_{a,b}$.

## Full Derivation

1. **Write the full-structure wave equation.**

   $$
   \left[\frac{\partial^2}{\partial z^2}+\frac{\partial^2}{\partial x^2}+k_0^2\left(n_s^2+\Delta n_a^2+\Delta n_b^2\right)\right]E=0
   $$

   This is the exact equation for the field $E(x,z)$ in the combined two-waveguide structure, under the perturbation-theory assumptions: small perturbations, SVEA, and single-mode waveguides.

   $\partial^2/\partial z^2$ is just the ordinary Helmholtz equation term for a field depending on $z$. Each waveguide's *own* mode equation could drop it (replacing it with $-\beta_{a,b}^2$) because a lone waveguide's mode has one fixed propagation constant, $e^{-i\beta_{a,b}z}$. The *combined* field's $z$-dependence isn't known yet — that's what this derivation solves for — so it stays explicit here.

2. **Write the field as a slowly-varying superposition of the two waveguides' own modes.**

   $$
   E(x,z)=A(z)E_a(x)e^{i(\omega t-\beta_a z)}+B(z)E_b(x)e^{i(\omega t-\beta_b z)}
   $$

   The perturbation from each waveguide on the other is assumed to show up only as a slow change in the amplitude of the wave already guided by that waveguide — not as a new mode shape.

3. **Take the second $z$-derivative of the ansatz.**

   $$
   \frac{\partial^2E}{\partial z^2}=\left(A_{zz}-2i\beta_aA_z-\beta_a^2A\right)E_ae^{-i\beta_az}+\left(B_{zz}-2i\beta_bB_z-\beta_b^2B\right)E_be^{-i\beta_bz}
   $$

   This splits into two separate lines — one carrying $E_a e^{-i\beta_a z}$, the other $E_b e^{-i\beta_b z}$ — because $E(x,z)$ from Step 2 is a *sum* of two independent terms, each with its own amplitude $A(z)$/$B(z)$ and its own phase factor $e^{-i\beta_{a,b}z}$. Differentiation is linear, so $\partial^2/\partial z^2$ acts on each summand on its own via the product rule; there is no term that mixes $A$ with $E_b$ or $B$ with $E_a$, since the two summands never multiply each other.

4. **Apply the SVEA to each line separately.**

   $$
   \frac{\partial^2E}{\partial z^2}\approx-\left(2i\beta_aA_z+\beta_a^2A\right)E_ae^{-i\beta_az}-\left(2i\beta_bB_z+\beta_b^2B\right)E_be^{-i\beta_bz}
   $$

   with the SVEA condition $|A_{zz}|\ll|2i\beta_aA_z|\ll|\beta_a^2A|$ (and the same for $B$) justifying dropping the second-derivative terms $A_{zz}$, $B_{zz}$ from each line independently.

5. **Insert this into the full wave equation and subtract off each waveguide's own unperturbed wave equation.**

   $$
   2i\beta_aA_zE_ae^{-i\beta_az}+2i\beta_bB_zE_be^{-i\beta_bz}=k_0^2\Delta n_b^2AE_ae^{-i\beta_az}+k_0^2\Delta n_a^2BE_be^{-i\beta_bz}
   $$

   Using each waveguide's own mode equation cancels the terms that don't involve the other waveguide's index perturbation, leaving only the cross terms shown.

6. **Project onto each mode and integrate.**

   $$
   \kappa_{ab}=\frac{\omega}{4}\varepsilon_0\int_{-\infty}^{\infty}E_a^*(x)\Delta n_a^2(x)E_b(x)\,dx,\qquad M_{aa}=\frac{\omega}{4}\varepsilon_0\int_{-\infty}^{\infty}E_a^*(x)\Delta n_b^2(x)E_a(x)\,dx
   $$

   Multiplying by $E_a^*$ (and separately $E_b^*$) and integrating over $x$, then using the power-normalization condition, converts the overlap integrals into the coupling coefficients $\kappa_{ab}$, $\kappa_{ba}$ and self-frequency-shift terms $M_{aa}$, $M_{bb}$.

7. **Arrive at the coupled-mode equations.**

   $$
   \frac{\partial A}{\partial z}=-i\kappa_{ab}B(z)e^{i(\beta_a-\beta_b)z}-iM_{aa}A(z),\qquad\frac{\partial B}{\partial z}=-i\kappa_{ba}A(z)e^{-i(\beta_a-\beta_b)z}-iM_{bb}B(z)
   $$

   $\kappa_{ab},\kappa_{ba}$ are the coupling coefficients ($\kappa_{ab}=\kappa_{ba}^*$); $M_{aa},M_{bb}$ are self-frequency shifts in each waveguide's propagation constant caused merely by the presence of the other waveguide.

8. **Absorb the self-frequency shifts into the amplitudes.**

   $$
   A(z)=A'(z)e^{-iM_{aa}z},\qquad B(z)=B'(z)e^{-iM_{bb}z}\;\;\Rightarrow\;\;\frac{\partial A'}{\partial z}=-i\kappa B'(z)e^{2i\delta z},\qquad\frac{\partial B'}{\partial z}=-i\kappa A'(z)e^{-2i\delta z}
   $$

   with $\kappa_{ab}=\kappa_{ba}=\kappa$ and $2\delta=(\beta_a+M_{aa})-(\beta_b+M_{bb})$. Relabeling $A'\to A$, $B'\to B$ gives the standard two-wave coupled-mode equations.

9. **Check power conservation.**

   $$
   \frac{\partial}{\partial z}\left(|A|^2+|B|^2\right)=-i\kappa BA^*e^{2i\delta z}+i\kappa^*AB^*e^{-2i\delta z}-i\kappa^*AB^*e^{-2i\delta z}+i\kappa BA^*e^{2i\delta z}=0
   $$

   The total power in the two waveguides is conserved by the coupled-mode equations, as it must be for a lossless coupling process.

## Result

$$
\frac{\partial A}{\partial z}=-i\kappa B(z)e^{2i\delta z},\qquad\frac{\partial B}{\partial z}=-i\kappa A(z)e^{-2i\delta z}
$$

## Where It's Used

**Concept:** [Coupled Mode Theory](Coupled%20Mode%20Theory.md)

---

## Links

**Related:** [Directional Coupler](Directional%20Coupler.md)
