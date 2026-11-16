---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The guided-mode characteristic equation for a dielectric [slab waveguide](Slab%20Waveguide%20Modes.md), obtained rigorously from Maxwell's equations rather than the [ray-optics picture](TIR%20Self-Consistency%20Derivation.md) — for TE and TM polarization, ending in both the raw (index-explicit) and normalized $(V,b,a)$ forms.

## Full Derivation

### Setup and assumptions

- **Geometry, three materials, symmetric slab:** substrate ($\epsilon_s,n_s$, $x<-d/2$), core/film ($\epsilon_f,n_f$, $|x|<d/2$), cladding ($\epsilon_c,n_c$, $x>d/2$), with $n_f>n_s>n_c$ — origin at the slab's center.
- **Maxwell's equations**, source-free, with Faraday's law and Ampère's law as the two curl equations:
  $$
  \underbrace{\nabla\times\bar E=-\frac{\partial\bar B}{\partial t}}_{\text{Faraday}},\qquad
  \underbrace{\nabla\times\bar H=\frac{\partial\bar D}{\partial t}}_{\text{Amp\`ere}},\qquad
  \nabla\cdot\bar D=0,\qquad
  \nabla\cdot\bar B=0
  $$
  with constitutive relations $\bar D=\epsilon\bar E$, $\bar B=\mu_0\bar H$ (non-magnetic; no free current, $\bar J=0$, since each layer is an ideal dielectric), and boundary conditions at each interface: tangential $\bar E$ and tangential $\bar H$ continuous, normal $\bar D$ and normal $\bar B$ continuous (no free surface charge or current on an ideal dielectric interface).
- **Assumptions**, each justified for this system:
  1. *The cross-section is $z$-independent.* The slab stack is uniform along the propagation direction — an ideal waveguide by definition doesn't taper, bend, or change composition along $z$.
  2. *$\partial_y=0$.* The slab extends uniformly in $y$ with no structure varying in that direction, so no physical quantity can depend on $y$ — the translational symmetry that makes the problem effectively 1D (in $x$) instead of 2D.
  3. *Propagation is along $z$*, with $x$ reserved for the direction across which the index profile $n(x)$ varies.
  4. *Single frequency, $\partial_t\to i\omega$.* Maxwell's equations are linear, so any time-dependent field is a Fourier sum of single-frequency fields, each solving the equations independently — solving for one $\omega$ loses no generality.
  5. *Fixed EM field profile in $x$ — a mode:* $\bar E=\bar E_\nu(x)e^{i(\beta_\nu z-\omega t)}$, $\bar H=\bar H_\nu(x)e^{i(\beta_\nu z-\omega t)}$, $k_y=0$. This is the defining ansatz of a mode — a transverse field pattern that reproduces itself, up to phase, as it propagates. It turns Maxwell's PDEs into an eigenvalue problem in $x$ (eigenvalue $\beta_\nu$), and the resulting mode functions form a complete basis, so any field in the waveguide is a sum over modes of this form without loss of generality.

### 1. Component Form of Ampère's and Faraday's Laws Under the Mode Ansatz

With $\partial_y=0$, $\partial_z\to i\beta$, $\partial_t\to-i\omega$, each vector curl equation splits into three scalar equations, one per Cartesian direction:

$$
(\nabla\times\bar E)_x = i\beta E_y,\qquad
(\nabla\times\bar E)_y = -i\beta E_x-\partial_x E_z,\qquad
(\nabla\times\bar E)_z = \partial_x E_y
$$

and the same pattern for $\bar H$. Setting $\nabla\times\bar E=-i\omega\mu_0\bar H$ (Faraday) and $\nabla\times\bar H=i\omega\epsilon(x)\bar E$ (Ampère) component by component gives six coupled scalar equations, which split cleanly into two columns:

$$
\begin{aligned}
\beta E_y &= -\omega\mu_0 H_x, & \partial_x E_y &= -i\omega\mu_0 H_z, & \partial_x H_z + i\beta H_x &= -i\omega\epsilon E_y \\[4pt]
\beta H_y &= \omega\epsilon E_x, & \partial_x H_y &= i\omega\epsilon E_z, & \partial_x E_z + i\beta E_x &= i\omega\mu_0 H_y
\end{aligned}
$$

This is pure substitution — no approximation yet, only the geometry ($\partial_y=0$) and the propagating-mode ansatz have been used.

### 2. TE/TM Decoupling

The top row involves only $E_y,H_x,H_z$; the bottom row involves only $E_x,H_y,E_z$ — and neither row ever references a variable from the other. This is forced by the geometry: the only terms that could have linked the two groups are ones like $\partial_yE_z,\partial_yE_x,\partial_yH_z,\partial_yH_x$, and every one of them is killed by $\partial_y=0$. So $E_y$ can only ever appear alongside $H_x,H_z$ (never $E_x$ or $H_y$), and $E_x$ can only ever appear alongside $H_y,E_z$ (never $E_y$ or $H_x$).

That is why **TE** is $(E_y,H_x,H_z)$ and not, say, $(E_y,E_x,H_z)$: $E_x$ is simply never in the same equation as $E_y$ once $\partial_y=0$ is imposed, so Maxwell's equations themselves dictate the grouping — it isn't asserted by convention. "TE" (transverse electric) is the group whose only electric field component, $E_y$, has no component along $z$ (i.e. $E_z=0$); **TM** (transverse magnetic) is the mirror case, whose only magnetic field component, $H_y$, has $H_z=0$. From the top-row and bottom-row equations above:

$$
\text{TE:}\quad H_x=-\frac{\beta}{\omega\mu_0}E_y,\quad H_z=-\frac{i}{\omega\mu_0}E_y' \qquad\qquad
\text{TM:}\quad E_x=\frac{\beta}{\omega\epsilon(x)}H_y,\quad E_z=\frac{i}{\omega\epsilon(x)}H_y'
$$

Each group is a complete, self-consistent solution of Maxwell's equations on its own, so the most general field in the guide is a TE mode and a TM mode superposed independently.

### 3. Reduction to the One-Dimensional Helmholtz Equation

Substituting the TE relations above back into the remaining curl equation (and the mirror substitution for TM) collapses the coupled first-order system into a single second-order equation per polarization:

$$
E_y''(x) + \big(n^2(x)k_0^2-\beta^2\big)E_y(x) = 0 \qquad\text{(TE)}, \qquad\qquad
H_y''(x) + \big(n^2(x)k_0^2-\beta^2\big)H_y(x) = 0 \qquad\text{(TM)}
$$

with $k_0=\omega/c$. This is the 1D Helmholtz equation, piecewise-constant-coefficient since $n(x)$ is constant within each of the three layers. It is also formally identical to the time-independent Schrödinger equation, $\psi''+(2m/\hbar^2)(E-V)\psi=0$, under the dictionary $\psi\Leftrightarrow E_y\text{ or }H_y$, $V(x)\Leftrightarrow-n^2(x)$, $\mathcal E\Leftrightarrow-\beta^2$ — so bound-state intuition from quantum mechanics carries over directly: guided modes are the waveguide analog of bound states.

### 4. Guided-Mode Condition

$$
n_s k_0 < \beta < n_f k_0 \quad\Leftrightarrow\quad \text{guided modes}
$$

Guided modes are harmonic (oscillatory) in the core and exponentially decaying in both substrate and cladding — the waveguide analog of a bound state. If $\beta/k_0$ falls between $n_c$ and $n_s$ instead, the solution is harmonic in core and substrate but still decaying in the cladding (substrate modes); if $\beta/k_0<n_c,n_s$, the solution is harmonic everywhere (radiation modes) — equivalent to the ray angle no longer exceeding the critical angle for total internal reflection.

### 5. Piecewise Field Ansatz

Master field ($E_y$ for TE, $H_y$ for TM), general solution of the Helmholtz equation in each uniform-index region — harmonic in the core, exponential decay in substrate and cladding:

$$
\begin{cases}
De^{\gamma_s(x+d/2)} & x<-d/2\\[2pt]
a_1\cos(\kappa_fx)+a_2\sin(\kappa_fx) & |x|<d/2\\[2pt]
Ae^{-\gamma_c(x-d/2)} & x>d/2
\end{cases}, \qquad
\kappa_f^2=n_f^2k_0^2-\beta^2,\ \ \gamma_s^2=\beta^2-n_s^2k_0^2,\ \ \gamma_c^2=\beta^2-n_c^2k_0^2
$$

Four constants ($A,D,a_1,a_2$) remain to be fixed by boundary matching, up to one overall normalization.

### 6. TE Characteristic Equation via Boundary Matching

Continuity of $E_y,E_y'$ (equivalently $E_y,H_z$, since $\mu_0$ is the same everywhere) at each interface. Rather than eliminating all four constants simultaneously, match each interface *separately* and solve for the ratio $r\equiv a_1/a_2$; writing $\theta\equiv\kappa_fd/2$:

$$
x=d/2:\ \ \frac{a_1}{a_2}=-\frac{\kappa_f\cos\theta+\gamma_c\sin\theta}{\gamma_c\cos\theta-\kappa_f\sin\theta},
\qquad
x=-d/2:\ \ \frac{a_1}{a_2}=-\frac{\kappa_f\cos\theta+\gamma_s\sin\theta}{\kappa_f\sin\theta-\gamma_s\cos\theta}
$$

One core field must satisfy both interfaces at once, so these two expressions for $r$ must agree. Cross-multiplying, writing $t\equiv\tan\theta$, and collecting $t^2,t,\text{const}$ terms gives the quadratic

$$
\kappa_f(\gamma_s+\gamma_c)\,t^2 + 2t(\kappa_f^2-\gamma_s\gamma_c) - \kappa_f(\gamma_s+\gamma_c) = 0
$$

Dividing by $(1-t^2)$ and using the double-angle identity $\tan(2\theta)=2t/(1-t^2)$ isolates the **TE characteristic equation**:

$$
\tan(2\theta)=\frac{\kappa_f(\gamma_s+\gamma_c)}{\kappa_f^2-\gamma_s\gamma_c} \qquad\text{(TE)}
$$

### 7. TM Characteristic Equation via Boundary Matching

The continuous quantities are now $H_y$ and $\dfrac1\epsilon\partial_xH_y$ (equivalent to $H_y,E_z$ continuity). Dividing that derivative-continuity equation by the value-continuity equation and clearing denominators (multiply through by $\epsilon_f\epsilon_c$ at $x=d/2$, by $\epsilon_f\epsilon_s$ at $x=-d/2$) gives the two ratios with the permittivities sitting exactly where the boundary condition put them:

$$
x=d/2:\ \ \frac{a_1}{a_2}=-\frac{\kappa_f\epsilon_c\cos\theta+\gamma_c\epsilon_f\sin\theta}{\gamma_c\epsilon_f\cos\theta-\kappa_f\epsilon_c\sin\theta},
\qquad
x=-d/2:\ \ \frac{a_1}{a_2}=-\frac{\kappa_f\epsilon_s\cos\theta+\gamma_s\epsilon_f\sin\theta}{\kappa_f\epsilon_s\sin\theta-\gamma_s\epsilon_f\cos\theta}
$$

Setting these equal, dividing by $\cos\theta$, cross-multiplying, and collecting terms exactly as in step 6:

$$
\kappa_f\epsilon_f(\gamma_c\epsilon_s+\gamma_s\epsilon_c)\,t^2 + 2t\big(\kappa_f^2\epsilon_c\epsilon_s-\gamma_s\gamma_c\epsilon_f^2\big) - \kappa_f\epsilon_f(\gamma_c\epsilon_s+\gamma_s\epsilon_c) = 0
\ \Rightarrow\
\tan(2\theta)=\frac{\kappa_f\epsilon_f(\epsilon_c\gamma_s+\epsilon_s\gamma_c)}{\epsilon_s\epsilon_c\kappa_f^2-\epsilon_f^2\gamma_s\gamma_c} \quad\text{(TM, raw)}
$$

This is messier than TE only because the $\epsilon$'s haven't been packaged yet: every $\gamma$ that touches an interface picked up that interface's $\epsilon$, and every $\kappa_f$ that touches an interface picked up the *other* $\epsilon$ — a direct consequence of matching $\frac1\epsilon\partial_xH_y$ rather than $\partial_xH_y$ itself.

**Compress it into the same shape as TE:**

1. Divide numerator and denominator by $\epsilon_s\epsilon_c$ (legal — same nonzero factor top and bottom):
   $$
   \tan(2\theta)=\dfrac{\dfrac{\kappa_f\epsilon_f(\epsilon_c\gamma_s+\epsilon_s\gamma_c)}{\epsilon_s\epsilon_c}}{\kappa_f^2-\dfrac{\epsilon_f^2\gamma_s\gamma_c}{\epsilon_s\epsilon_c}}
   $$
2. Split the numerator's fraction across its two terms and factor $\epsilon_f$ into each individually:
   $$
   \frac{\kappa_f\epsilon_f(\epsilon_c\gamma_s+\epsilon_s\gamma_c)}{\epsilon_s\epsilon_c}=\kappa_f\epsilon_f\Big(\frac{\gamma_s}{\epsilon_s}+\frac{\gamma_c}{\epsilon_c}\Big)=\kappa_f\Big(\frac{\epsilon_f}{\epsilon_s}\gamma_s+\frac{\epsilon_f}{\epsilon_c}\gamma_c\Big)
   $$
3. The denominator's fraction splits the same way:
   $$
   \frac{\epsilon_f^2\gamma_s\gamma_c}{\epsilon_s\epsilon_c}=\frac{\epsilon_f}{\epsilon_s}\gamma_s\cdot\frac{\epsilon_f}{\epsilon_c}\gamma_c
   $$
4. Both simplifications produced the same recurring object, $\frac{\epsilon_f}{\epsilon_i}\gamma_i$ — name it:
   $$
   \bar\gamma_s\equiv\frac{\epsilon_f}{\epsilon_s}\gamma_s=\Big(\frac{n_f}{n_s}\Big)^{2}\gamma_s, \qquad
   \bar\gamma_c\equiv\frac{\epsilon_f}{\epsilon_c}\gamma_c=\Big(\frac{n_f}{n_c}\Big)^{2}\gamma_c
   $$
   (using $\epsilon_i\propto n_i^2$, so $\epsilon$-ratios equal $n^2$-ratios).
5. Substitute back — the **TM characteristic equation**:
   $$
   \tan(2\theta)=\frac{\kappa_f(\bar\gamma_s+\bar\gamma_c)}{\kappa_f^2-\bar\gamma_s\bar\gamma_c} \qquad\text{(TM)}
   $$

The "trick" is nothing but factoring $\epsilon_f$ out of each term individually and naming the resulting $\frac{\epsilon_f}{\epsilon_i}\gamma_i$ combinations — the physics behind *why* that specific ratio appears was already fixed at the boundary-matching step, where continuity of $\frac1\epsilon\partial_xH_y$ pins an $\epsilon_f/\epsilon_i$ factor onto every decay constant.

### 8. Normalization to the Dimensionless $(V,b,a)$ Form

Define the normalized frequency $V=k_0d\sqrt{n_f^2-n_s^2}$, asymmetry $a=(n_s^2-n_c^2)/(n_f^2-n_s^2)$, and normalized propagation coefficient $b=(n_{eff}^2-n_s^2)/(n_f^2-n_s^2)$, $n_{eff}=\beta/k_0$. Substituting into the definitions of $\kappa_f,\gamma_s,\gamma_c$ (step 5) gives, by direct algebra,

$$
\kappa_f=\frac{V}{d}\sqrt{1-b}, \qquad \gamma_s=\frac{V}{d}\sqrt{b}, \qquad \gamma_c=\frac{V}{d}\sqrt{a+b}
\qquad\Rightarrow\qquad
2\theta=\kappa_fd=V\sqrt{1-b}
$$

**TE:** apply the tangent-addition identity $\tan(A+B)=\dfrac{\tan A+\tan B}{1-\tan A\tan B}$ with $\tan A=\gamma_s/\kappa_f$, $\tan B=\gamma_c/\kappa_f$ — this reproduces exactly the RHS of the TE equation in step 6, so $\tan(2\theta)=\tan(A+B)$ gives, unfolding the tangent's $\pi$-periodicity into an explicit branch index $N$,

$$
2\theta = \tan^{-1}\sqrt{\tfrac{b}{1-b}} + \tan^{-1}\sqrt{\tfrac{a+b}{1-b}} + N\pi
\ \Rightarrow\
\tan^{-1}\sqrt{\frac{b}{1-b}} + \tan^{-1}\sqrt{\frac{a+b}{1-b}} = V\sqrt{1-b}-N\pi
$$

**TM:** the same identity with $\tan A=\bar\gamma_s/\kappa_f=(n_f/n_s)^2\sqrt{b/(1-b)}$, $\tan B=\bar\gamma_c/\kappa_f=(n_f/n_c)^2\sqrt{(a+b)/(1-b)}$ gives

$$
\tan^{-1}\!\left[\Big(\frac{n_f}{n_s}\Big)^{2}\sqrt{\frac{b}{1-b}}\right] + \tan^{-1}\!\left[\Big(\frac{n_f}{n_c}\Big)^{2}\sqrt{\frac{a+b}{1-b}}\right] = V\sqrt{1-b}-N\pi
$$

Both are, symbol for symbol, the "Key Equation" / TM supporting formula of the [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md) concept note — the raw $\tan(2\theta)=\ldots$ forms fall straight out of the boundary-condition algebra (steps 6–7); the normalized arctan forms result from (i) applying the tan-addition identity so each mode branch $N$ is explicit instead of hidden in $\tan$'s periodicity, and (ii) nondimensionalizing so one curve, indexed only by $a$ and $N$, describes every slab rather than just this one's specific $n_c,n_f,n_s,d$.

## Result

$$
\tan(2\theta)=\frac{\kappa_f(\gamma_s+\gamma_c)}{\kappa_f^2-\gamma_s\gamma_c} \quad\text{(TE)}, \qquad
\tan(2\theta)=\frac{\kappa_f(\bar\gamma_s+\bar\gamma_c)}{\kappa_f^2-\bar\gamma_s\bar\gamma_c} \quad\text{(TM)}, \qquad \theta=\frac{\kappa_fd}{2}
$$

Equivalent, dimensionless forms:

$$
\tan^{-1}\sqrt{\tfrac{b}{1-b}} + \tan^{-1}\sqrt{\tfrac{a+b}{1-b}} = V\sqrt{1-b}-N\pi \quad\text{(TE)}
$$

$$
\tan^{-1}\!\left[\Big(\tfrac{n_f}{n_s}\Big)^{2}\sqrt{\tfrac{b}{1-b}}\right] + \tan^{-1}\!\left[\Big(\tfrac{n_f}{n_c}\Big)^{2}\sqrt{\tfrac{a+b}{1-b}}\right] = V\sqrt{1-b}-N\pi \quad\text{(TM)}
$$

## Where It's Used

**Concept:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md)

---

## Links

**Related:** [TIR Self-Consistency Derivation](TIR%20Self-Consistency%20Derivation.md) (alternate, ray-optics route to the same condition), [Fresnel Coefficients](../02%20-%20Electromagnetism/Fresnel%20Coefficients.md)
