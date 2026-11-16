---
tags:
  - optics
  - concept
---
---
## Core Idea

A GRIN (gradient-index) lens focuses light with a continuously varying refractive index $n(r)$ across a flat block of material instead of curved surfaces — rays bend smoothly all the way through the medium rather than snapping direction only at an interface.

## Key Equation

$$
n(r) = n_0\left(1-\frac{\alpha^2 r^2}{2}\right)
$$

**Derived From:** Taylor-expanding a general axially symmetric index profile $n(r)$ about the optical axis; symmetry ($n(r)=n(-r)$) kills every odd term, leaving $n(r)\approx n_0 + \tfrac12 n''(0)\,r^2+\dots$ to lowest order. Writing that (necessarily negative, for a focusing profile) quadratic coefficient as $n_0\left(-\alpha^2\right)$ *defines* the gradient constant $\alpha$ and gives the parabolic profile — the defining, lowest-order model of any GRIN medium. Full steps in [GRIN Lens Derivation](GRIN%20Lens%20Derivation.md).

## Supporting Formulas

- Paraxial ray equation from this profile: $\dfrac{d^2r}{dz^2}+\alpha^2 r(z) = 0$ — a Hooke's-law-like restoring equation, with solution $r(z) = r_0\cos(\alpha z) + \dfrac{\theta_0}{\alpha}\sin(\alpha z)$, $\theta(z) = -r_0\alpha\sin(\alpha z) + \theta_0\cos(\alpha z)$
- **Pitch length** $\Lambda = 2\pi/\alpha$ — the rod length over which a ray completes one full sinusoidal cycle and returns exactly to its starting height and angle. Find it either from the quoted gradient constant $\alpha$ of the rod, or from a measured index profile via $\alpha=\sqrt{-n''(0)/n_0}$ (twice-differentiate $n(r)$ at the axis)
- **Pitch number** $P = z/\Lambda = \alpha z/(2\pi)$ — GRIN rod lengths are conventionally specified as a fraction of $\Lambda$ rather than an absolute length
- Standard rod-lens focal length: $f = \dfrac{1}{n_0\alpha\sin(\alpha L)}$ for a rod of length $L$

**What $P=1/4$ and $P=1/2$ mean** (from evaluating the ray solution above at $z=\Lambda/4=\pi/(2\alpha)$ and $z=\Lambda/2=\pi/\alpha$):

- **Quarter pitch ($P=1/4$):** output height depends only on the *input angle* ($r=\theta_0/\alpha$) and output angle depends only on the *input height* ($\theta=-r_0\alpha$) — position and angle swap roles. A point source on-axis emerges collimated, and collimated input focuses to a point at the exit face. This is the standard fiber-collimator/focusing form of a GRIN lens.
- **Half pitch ($P=1/2$):** every ray reflects through the axis, $r\to-r_0$, $\theta\to-\theta_0$ — the input image is relayed to the output face inverted, at unit magnification. Used as an image-inverting relay.
- (Full pitch $P=1$ just returns $r\to r_0$, $\theta\to\theta_0$ — an erect, unit-magnification relay, the basis of image-transmission bundles.)

## Derivation Outline

1. Taylor-expand a general axisymmetric index profile about the axis and truncate at quadratic order to get the parabolic profile.
2. Start from the general ray equation for inhomogeneous media, derived from Fermat's principle.
3. Restrict to paraxial rays (nearly parallel to the optical axis $z$), so $ds\approx dz$.
4. Insert the parabolic index profile and linearize $\nabla n$ in $r$.
5. Get the simple-harmonic ray equation and solve for $r(z)$ given an initial height and angle.
6. Evaluate the solution at $z=\Lambda/4$ and $z=\Lambda/2$ to read off the quarter- and half-pitch behavior.

## Physical Intuition

Near the axis the material is slightly denser optically than farther out, so light there travels a hair slower. A ray that strays off-axis is riding through progressively "faster" material as it moves outward, which continuously curls its path back toward the center — the same bending a conventional lens does abruptly at one curved surface, except here it happens gradually over the whole length of the rod. Because the bending is continuous and smooth rather than a single kink, the ray path traces out a wave-like, oscillating curve as it travels down the material, alternately crossing the axis and swinging back out, and a short enough slice of that curve looks and acts exactly like a thin lens — flat on both faces, no curvature needed at all.

## Isomorphisms

- The paraxial ray equation $d^2r/dz^2+\alpha^2r=0$ has the same structure as the classical harmonic oscillator $\ddot x+\omega^2x=0$ — the index gradient plays the role of a Hooke's-law restoring force, with $z$ standing in for time.

## Open Questions

- [ ]

---

## Links

**Related:** [Fresnel Coefficients](../02%20-%20Electromagnetism/Fresnel%20Coefficients.md), [TIR Phase Shift](TIR%20Phase%20Shift.md)
**Full Derivation:** [GRIN Lens Derivation](GRIN%20Lens%20Derivation.md)
