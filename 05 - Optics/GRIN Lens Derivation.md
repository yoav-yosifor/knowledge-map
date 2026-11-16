---
tags:
  - optics
  - derivation
---
---
## Statement of Result

The parabolic index profile that defines a GRIN medium, the paraxial ray trajectory it produces, and the pitch-dependent behavior — in particular what the quarter-pitch ($P=1/4$) and half-pitch ($P=1/2$) rod lengths do to a ray bundle.

## Starting Point

- General axially symmetric index profile $n(r)$, smooth and even in $r$ (no assumed functional form yet) — symmetric because there is no physical reason for the medium to prefer $+r$ over $-r$.
- General ray equation for light in an inhomogeneous medium, obtained from Fermat's principle (stationary optical path $\int n\,ds$): $\dfrac{d}{ds}\left(n\dfrac{d\vec r}{ds}\right) = \nabla n$, with $s$ the arc length along the ray.
- Paraxial approximation: the ray travels nearly parallel to the optical axis $z$, so its transverse slope $dr/dz$ is small, arc length $ds\approx dz$ to leading order, and $d\vec r/ds\approx d\vec r/dz$.

## Full Derivation

1. **Taylor-expand the index profile about the axis.** Since $n(r)$ is even ($n(r)=n(-r)$, by the symmetry assumption), its Taylor series about $r=0$ has no odd terms:
   $$
   n(r) = n(0) + \frac12 n''(0)\,r^2 + O(r^4)
   $$
   Naming the on-axis index $n_0\equiv n(0)$ and writing the (negative, for a medium that is denser on-axis and therefore focusing) curvature as $n''(0)\equiv -n_0\alpha^2$ defines the gradient constant $\alpha$:
   $$
   n(r) \approx n_0\left(1-\frac{\alpha^2 r^2}{2}\right)
   $$
   This parabolic profile is the lowest-order, and by far the most common, model for a GRIN medium — every result below follows from truncating the expansion here.

2. **Reduce the general ray equation to a paraxial one in $z$.** Reparametrizing $\dfrac{d}{ds}\left(n\dfrac{d\vec r}{ds}\right)=\nabla n$ by $z$ instead of arc length $s$, and using $ds\approx dz$:
   $$
   \frac{d}{dz}\left(n\frac{dr}{dz}\right) = \frac{\partial n}{\partial r}
   $$
   Expanding the derivative on the left gives $\dfrac{dn}{dz}\dfrac{dr}{dz} + n\dfrac{d^2r}{dz^2}$. The first piece is a product of two already-small paraxial quantities ($dn/dz$ is small since the index varies little across the beam, and $dr/dz$ is small by the paraxial assumption), so it is second order and dropped. On the remaining term, $n\approx n_0$ is used to leading order, since the index departs from $n_0$ only by the small amount being tracked on the right-hand side:
   $$
   n_0\frac{d^2r}{dz^2} \approx \frac{\partial n}{\partial r}
   $$

3. **Insert the parabolic profile and take its gradient.** Differentiating $n(r)=n_0\left(1-\tfrac{\alpha^2r^2}{2}\right)$ with respect to $r$:
   $$
   \frac{\partial n}{\partial r} = -n_0\alpha^2 r
   $$
   This is linear in $r$ — the quadratic index profile is exactly what makes the ray equation linear, the same way a quadratic potential energy gives a linear (Hooke's-law) force.

4. **Combine into the paraxial GRIN ray equation.** Substituting into the result of step 2 and canceling $n_0$:
   $$
   \frac{d^2r}{dz^2} + \alpha^2 r(z) = 0
   $$
   This is the simple-harmonic-oscillator equation with $z$ playing the role of time and $\alpha$ the role of angular frequency.

5. **Solve with general initial conditions.** For a ray entering the medium at height $r_0$ with angle $\theta_0=\left.\dfrac{dr}{dz}\right|_{z=0}$, the general solution of step 4 is:
   $$
   r(z) = r_0\cos(\alpha z) + \frac{\theta_0}{\alpha}\sin(\alpha z)
   $$
   Differentiating gives the ray angle at any depth:
   $$
   \theta(z) = \frac{dr}{dz} = -r_0\alpha\sin(\alpha z) + \theta_0\cos(\alpha z)
   $$

6. **Define the pitch and evaluate the solution at fractions of it.** Since $r(z)$ and $\theta(z)$ are built from $\cos(\alpha z)$ and $\sin(\alpha z)$, they repeat exactly once $\alpha z$ advances by $2\pi$. That repeat length is the **pitch length**,
   $$
   \Lambda = \frac{2\pi}{\alpha}
   $$
   and it is found the same way $\alpha$ itself is found: either read off the gradient constant $\alpha$ quoted for the rod and compute $\Lambda=2\pi/\alpha$ directly, or, from a measured index profile, take the on-axis curvature $\alpha=\sqrt{-n''(0)/n_0}$ from step 1 and use that. A rod's physical length $L$ is then expressed as a **pitch number** $P=L/\Lambda=\alpha L/(2\pi)$, a fraction (or multiple) of one full cycle, rather than as an absolute length — this is how GRIN rod lenses are catalogued. Evaluating step 5 at the three lengths that matter in practice:

   - **Quarter pitch, $P=\tfrac14$ ($z=\Lambda/4=\pi/(2\alpha)$):** $\cos(\alpha z)=0$, $\sin(\alpha z)=1$, so
     $$
     r\!\left(\frac{\pi}{2\alpha}\right) = \frac{\theta_0}{\alpha}, \qquad \theta\!\left(\frac{\pi}{2\alpha}\right) = -r_0\alpha
     $$
     The output height depends only on the input *angle* $\theta_0$, and the output angle depends only on the input *height* $r_0$ — position and angle have swapped roles. Every ray entering with the same angle, regardless of starting height, arrives at the same output point: a collimated beam is focused to a point (or, run the other way, a point source is collimated). This is the standard focusing/collimating GRIN lens.
   - **Half pitch, $P=\tfrac12$ ($z=\Lambda/2=\pi/\alpha$):** $\cos(\alpha z)=-1$, $\sin(\alpha z)=0$, so
     $$
     r\!\left(\frac{\pi}{\alpha}\right) = -r_0, \qquad \theta\!\left(\frac{\pi}{\alpha}\right) = -\theta_0
     $$
     Every ray reflects through the axis: the input pattern reappears at the output face at unit magnification, but inverted. A half-pitch rod is an image-inverting relay.
   - **Full pitch, $P=1$ ($z=\Lambda$):** $\cos(\alpha z)=1$, $\sin(\alpha z)=0$, so $r(\Lambda)=r_0$, $\theta(\Lambda)=\theta_0$ — the ray returns exactly to its starting height and angle. A full-pitch rod relays the input image erect, at unit magnification.

## Result

$$
n(r) = n_0\left(1-\frac{\alpha^2 r^2}{2}\right)
\quad\Longrightarrow\quad
\frac{d^2r}{dz^2} + \alpha^2 r(z) = 0
\quad\Longrightarrow\quad
r(z) = r_0\cos(\alpha z) + \frac{\theta_0}{\alpha}\sin(\alpha z)
$$

with pitch length $\Lambda=2\pi/\alpha$, and pitch-fraction behavior: $P=\tfrac14$ focuses/collimates, $P=\tfrac12$ relays an inverted image, $P=1$ relays an erect image.

## Where It's Used

**Concept:** [GRIN Lens](GRIN%20Lens.md)

---

## Links

**Related:** [Fresnel Coefficients](../02%20-%20Electromagnetism/Fresnel%20Coefficients.md)
