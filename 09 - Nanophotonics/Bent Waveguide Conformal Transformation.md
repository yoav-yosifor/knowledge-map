---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

That a bent waveguide is equivalent to a *straight* waveguide with a distorted index profile $n_{eq}(u)=n(u)\,e^{u/R}$, obtained by applying a conformal coordinate map to the wave equation. The exponentially rising equivalent index is what explains the outward-pushed, leaky "mode" of a bend.

## Starting Point

- Scalar wave equation in cylindrical coordinates $(\rho,\theta)$ in the plane of the bend: $\dfrac{\partial^2E}{\partial\rho^2}+\dfrac{1}{\rho}\dfrac{\partial E}{\partial\rho}+\dfrac{1}{\rho^2}\dfrac{\partial^2E}{\partial\theta^2}+k_0^2\,n^2(\rho)\,E=0$.
- Conformal coordinate map (given in the source): $u=R\ln(\rho/R)$, $v=R\,\theta$, with $R$ an arbitrary reference radius (the one mapped to $u=0$).
- The map sends $\rho=0\to u=-\infty$ and $\rho\to\infty\to u=+\infty$, so $u$ spans $(-\infty,\infty)$ — the curved guide is unrolled onto an infinite straight domain.
- Standard fact used without proof: under a conformal (analytic) map $w(\zeta)$ of the plane, the Laplacian transforms as $\nabla^2_\zeta=\left|\dfrac{dw}{d\zeta}\right|^2\nabla^2_w$.

## Full Derivation

1. **Write the map as a single analytic function of the complex plane.**

   $$
   w=u+iv=R\ln(\rho/R)+iR\theta=R\ln\!\left(\frac{\rho e^{i\theta}}{R}\right)=R\ln(\zeta/R),\qquad \zeta\equiv\rho e^{i\theta}
   $$

   Combining the two real equations into $w=u+iv$ shows the map is $w=R\ln(\zeta/R)$ — an analytic function of $\zeta$, hence conformal. This is what licenses the Laplacian transformation rule.

2. **Compute the conformal scale factor.**

   $$
   \frac{dw}{d\zeta}=\frac{R}{\zeta}\quad\Longrightarrow\quad\left|\frac{dw}{d\zeta}\right|^2=\frac{R^2}{|\zeta|^2}=\frac{R^2}{\rho^2}
   $$

   Differentiating $w=R\ln(\zeta/R)$. The modulus squared depends only on $\rho=|\zeta|$, which is what makes the transformed equation tractable.

3. **Transform the Laplacian.**

   $$
   \frac{\partial^2E}{\partial\rho^2}+\frac{1}{\rho}\frac{\partial E}{\partial\rho}+\frac{1}{\rho^2}\frac{\partial^2E}{\partial\theta^2}
   =\frac{R^2}{\rho^2}\left(\frac{\partial^2E}{\partial u^2}+\frac{\partial^2E}{\partial v^2}\right)
   $$

   Applying $\nabla^2_\zeta=\left|dw/d\zeta\right|^2\nabla^2_w$ with the scale factor from step 2. The curved-coordinate Laplacian (with its awkward $1/\rho$ and $1/\rho^2$ factors) becomes a plain Cartesian Laplacian in $(u,v)$, scaled by $R^2/\rho^2$.

4. **Substitute into the wave equation.**

   $$
   \frac{R^2}{\rho^2}\left(\frac{\partial^2E}{\partial u^2}+\frac{\partial^2E}{\partial v^2}\right)+k_0^2\,n^2(\rho)\,E=0
   $$

   The index term $k_0^2n^2(\rho)E$ is untouched by the coordinate change; only the derivative part has been rewritten.

5. **Multiply through by $\rho^2/R^2$ and use the map to eliminate $\rho$.**

   $$
   \frac{\partial^2E}{\partial u^2}+\frac{\partial^2E}{\partial v^2}+k_0^2\,n^2(u)\,\frac{\rho^2}{R^2}\,E=0,\qquad
   \frac{\rho^2}{R^2}=\left(e^{u/R}\right)^2
   $$

   Dividing by $R^2/\rho^2$ leaves the two second derivatives bare (the Cartesian form) and multiplies the index term by $\rho^2/R^2$. From $u=R\ln(\rho/R)$ that factor is exactly $e^{2u/R}$, and the profile expressed in the new coordinate is $n(u)$.

6. **Fold the exponential into the index.**

   $$
   \frac{\partial^2E}{\partial u^2}+\frac{\partial^2E}{\partial v^2}+k_0^2\left[n(u)\,e^{u/R}\right]^2E=0
   $$

   Writing $n^2(u)\,e^{2u/R}=\left[n(u)e^{u/R}\right]^2$ puts the equation in the exact form of a straight waveguide whose index is $n_{eq}(u)=n(u)e^{u/R}$.

## Result

$$
\frac{\partial^2E}{\partial u^2}+\frac{\partial^2E}{\partial v^2}+k_0^2\,n_{eq}^2(u)\,E=0,\qquad
n_{eq}(u)=n(u)\,e^{u/R}
$$

In $(u,v)$ the bend is a straight guide whose index profile is the physical step $n(u)$ multiplied by an exponential ramp $e^{u/R}$. The ramp grows without bound as $u\to+\infty$, so no truly bound mode exists; the mode shifts toward the outer edge and radiates — the intrinsic bending loss.

## Where It's Used

**Concept:** [Waveguide Bending Loss](Waveguide%20Bending%20Loss.md)

---

## Links

**Related:** [Leaky Waveguide Modes](Leaky%20Waveguide%20Modes.md), [Radiation Condition](Radiation%20Condition.md), [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md)
