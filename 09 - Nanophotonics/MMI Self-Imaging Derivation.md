---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The propagation length $L$ at which an [MMI device](MMI%20Devices.md) reproduces (perfectly, as a mirror image, or as multiple weighted copies) an arbitrary input field profile, starting from the guided-mode dispersion relation of the wide multimode slab waveguide.

## Starting Point

- The MMI is a wide waveguide of width $w_m$, indices $n_f$ (core) / $n_c$ (cladding), supporting $m$ guided modes $\nu=0,\dots,m-1$
- Guided-mode dispersion relation (from [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md)): $k_{y\nu}^2+\beta_\nu^2=k_0^2n_f^2$, $k_0=\omega/c$, $k_{y\nu}=(\nu+1)\pi/w_{eq}$
- $w_{eq}$ is the effective width once the [Goos-Hänschen shift](Goos-Hänschen%20Shift.md) is accounted for
- Characteristic equation of the even TE modes of the slab: $\tan\!\left(\dfrac{k_yw_m}{2}\right)=\dfrac{p}{k_y}=\sqrt{\dfrac{k_0^2(n_f^2-n_c^2)}{k_y^2}-1}$

## Full Derivation

1. **Rewrite the characteristic equation in terms of the width deficit from $w_{eq}$.**

   $$
   \tan\!\left(\tfrac12 k_y(w_{eq}-x)\right)=\cot\!\left(\tfrac12 k_yx\right)
   $$

   Defining $w_m=w_{eq}-x$ turns the characteristic equation into this form, using $k_y\cdot w_{eq}=\pi$ for the fundamental mode ($\nu=0$).

2. **Approximate the effective width for the fundamental mode.**

   $$
   \frac{2}{k_yx}=\frac{k_0}{k_y}\sqrt{\left(n_f^2-n_c^2\right)-\left(\frac{k_y}{k_0}\right)^2}\approx\frac{k_0}{k_y}\sqrt{n_f^2-n_c^2}
   $$

   Since $x\ll w_{eq}$ and $k_y$ is small for the first mode, $\tan(\tfrac12k_yx)\approx\tfrac12k_yx$; substituting this linearization into the characteristic equation and dropping the small $(k_y/k_0)^2$ term gives this relation for $x$.

   $$
   w_{eq}=w_m+x\approx w_m+\frac{\lambda_0}{\pi}\left(n_f^2-n_c^2\right)^{-1/2}\quad\text{(TE)}
   $$

   Solving the previous line for $x$ and adding it to $w_m$ gives the TE effective width. The analogous TM calculation gives $w_{eq}\approx w_m+\dfrac{\lambda_0}{\pi}\left(\dfrac{n_c}{n_f}\right)^2\left(n_f^2-n_c^2\right)^{-1/2}$. It is common to assume $w_{eq,0}=w_{eq,\nu}$ for every mode when many modes are supported.

3. **Find the paraxial propagation constant of mode $\nu$.**

   $$
   \beta_\nu\approx k_0n_f-\frac{(\nu+1)^2\pi\lambda_0}{4n_fw_{eq}^2}
   $$

   Under the paraxial assumption $k_{y\nu}^2\ll k_0^2n_f^2$, the dispersion relation $k_{y\nu}^2+\beta_\nu^2=k_0^2n_f^2$ can be linearized in $k_{y\nu}^2/k_0^2n_f^2$, giving $\beta_\nu$ as the unconfined wavevector $k_0n_f$ minus a mode-dependent correction.

4. **Define the beat length between the first two modes, and show it sets the spacing between every mode pair.**

   $$
   L_\pi=\frac{\pi}{\beta_0-\beta_1}\approx\frac{4n_fw_{eq}^2}{3\lambda_0}
   $$

   $L_\pi$ is the propagation distance over which modes 0 and 1 accumulate a relative phase of $\pi$; it comes directly from the step-3 expression evaluated at $\nu=0,1$: $\beta_0-\beta_1\approx\dfrac{\pi\lambda_0}{4n_fw_{eq}^2}\cdot\left(2^2-1^2\right)=\dfrac{3\pi\lambda_0}{4n_fw_{eq}^2}$, inverted and multiplied by $\pi$.

   Because step 3's $\beta_\nu$ depends on the mode number only through $(\nu+1)^2$, the spacing between *any* mode $\nu$ and mode $0$ is
   $$
   \beta_0-\beta_\nu\approx\frac{\pi\lambda_0}{4n_fw_{eq}^2}\left[(\nu+1)^2-1\right]=\frac{\pi\lambda_0}{4n_fw_{eq}^2}\,\nu(\nu+2)
   $$
   which is just $\nu(\nu+2)$ copies of the same base unit $\pi\lambda_0/(4n_fw_{eq}^2)$ that separates modes 0 and 1 — i.e. exactly $\pi/(3L_\pi)$. Substituting gives
   $$
   \beta_0-\beta_\nu\approx\frac{\nu(\nu+2)\pi}{3L_\pi}
   $$
   This is why $L_\pi$, though defined from only the closest mode pair, ends up as the single length scale controlling the phase relationship between *every* pair of modes — and therefore the periodicity of the imaging condition derived in the remaining steps: the quadratic $(\nu+1)^2$ dependence of $\beta_\nu$ means all mode spacings are integer multiples of the same beat unit, so there's only one characteristic length in the problem, not one per mode pair.

5. **Decompose an arbitrary input into the guided modes.**

   $$
   \psi(y,z)=\sum_{\nu=0}^{m-1}C_\nu\psi_\nu(y)e^{-i\beta_\nu z},\qquad C_\nu=\frac{\int\psi(y,0)\,\psi_\nu^*(y)\,dy}{\int|\psi_\nu(y)|^2\,dy}
   $$

   Any field launched into the MMI is a superposition of its guided modes with weights $C_\nu$; the weights are found by projecting the input profile $\psi(y,0)$ onto each mode $\psi_\nu$.

6. **Write the field at $z=L$ relative to the mode-0 phase.**

   $$
   \psi(y,L)=\sum_{\nu=0}^{m-1}C_\nu\,\psi_\nu(y)\,e^{-i(\beta_\nu-\beta_0)L}=\sum_{\nu=0}^{m-1}C_\nu\,\psi_\nu(y)\,e^{-i\frac{\nu(\nu+2)\pi}{3L_\pi}L}
   $$

   Factoring out the common phase $e^{-i\beta_0L}$ and substituting the spacing relation from step 4 expresses the propagated field entirely in terms of $L_\pi$. This is done because $\nu(\nu+2)$ is even when $\nu$ is even and odd when $\nu$ is odd, and because the mode symmetry gives $\psi_\nu(-y)=\psi_\nu(y)$ for $\nu$ even and $\psi_\nu(-y)=-\psi_\nu(y)$ for $\nu$ odd — the two facts that make the imaging condition below tractable.

7. **Find the single-image condition.**

   $$
   e^{-i\frac{1}{3L_\pi}\nu(\nu+2)\pi L}=1\ \text{ or }\ (-1)^\nu \quad\Longrightarrow\quad L=p\cdot3L_\pi,\ \ p=1,2,\dots
   $$

   The phase factor multiplying every mode must reduce to either $1$ (reconstructing every mode's original phase — a perfect image) or $(-1)^\nu$ (flipping the odd modes' sign, which by the symmetry noted in step 6 produces a mirror image) for the sum to reproduce a copy of the input. This occurs at $L=p\cdot3L_\pi$; even $p$ gives a perfect image, odd $p$ gives a mirror image.

8. **Split the field at the half-integer points into even and odd mode sums.**

   $$
   \psi\!\left(y,\tfrac{p}{2}3L_\pi\right)=\sum_{\nu\ \text{even}}C_\nu\psi_\nu(y)+i^p\sum_{\nu\ \text{odd}}C_\nu\psi_\nu(y),\qquad p=1,3,5,\dots
   $$

   Evaluating the step-6 sum at $L=\tfrac12p\cdot3L_\pi$ makes the phase factor $e^{-i\frac{\nu(\nu+2)\pi}{2}p}$, which equals $1$ for every even $\nu$ and $i^p$ for every odd $\nu$; splitting the sum accordingly separates it into its even- and odd-mode parts.

9. **Rewrite the even/odd mode sums in terms of the input field and its mirror image.**

   $$
   \sum_{\nu\ \text{even}}C_\nu\psi_\nu(y)=\tfrac12\left[\psi(y,0)+\psi(-y,0)\right],\qquad \sum_{\nu\ \text{odd}}C_\nu\psi_\nu(y)=\tfrac12\left[\psi(y,0)-\psi(-y,0)\right]
   $$

   Because $\psi(y,0)=\sum_\nu C_\nu\psi_\nu(y)$ and $\psi(-y,0)=\sum_\nu C_\nu\psi_\nu(-y)=\sum_{\nu\ \text{even}}C_\nu\psi_\nu(y)-\sum_{\nu\ \text{odd}}C_\nu\psi_\nu(y)$ (using the mode symmetry from step 6), adding and subtracting these two expressions isolates the even- and odd-mode sums individually. Substituting both into step 8's result gives the final multiple-imaging formula.

## Result

$$
\psi\!\left(y,\tfrac{p}{2}3L_\pi\right)=\frac{1+i^p}{2}\,\psi(y,0)+\frac{1-i^p}{2}\,\psi(-y,0),\qquad p=1,3,5,\dots
$$

together with the single-image condition $L=p\cdot3L_\pi$ (perfect image for even $p$, mirror image for odd $p$). The multiple-imaging result is two weighted copies of the input field, one direct and one mirrored — the mechanism behind an MMI power splitter.

## Where It's Used

**Concept:** [MMI Devices](MMI%20Devices.md)

---

## Links

**Related:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md), [Goos-Hänschen Shift](Goos-Hänschen%20Shift.md)
