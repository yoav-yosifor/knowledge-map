---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A periodic grating on the waveguide surface supplies the momentum a free-space beam is missing to couple into a guided mode: the grating adds integer multiples of its reciprocal-lattice vector $2\pi/\Lambda$ to the incident wave's in-plane $k$-vector, phase-matching it to the guided mode's propagation constant.

## Key Equation

$$
k_3\sin\theta_3=\beta^{(m)}+\frac{2\pi}{\Lambda}v_3,\qquad v_3=0,\mp1,\mp2,\mp3,\dots
$$

**Derived From:** stated directly in the source as the grating phase-matching condition — the grating's momentum comb (spacing $2\pi/\Lambda$) compensates the mismatch between the incident and guided waves' $z$-components of $k$-vector.

## Supporting Formulas

- Same condition for coupling from the substrate: $k_1\sin\theta_1=\beta^{(m)}+\frac{2\pi}{\Lambda}v_1$, $v_1=0,\mp1,\mp2,\dots$
- Substituting $k_{1,3}=k_0n_{1,3}$ and $\beta^{(m)}=k_0n_{eff}^{(m)}$: $\sin\theta_3=\dfrac{n_{eff}^{(m)}}{n_3}+\dfrac{\lambda_0}{\Lambda}\dfrac{v_3}{n_3}$ (and analogously for $\theta_1$).
- Allowed diffraction-order range: $-1<\dfrac{n_{eff}^{(m)}}{n_3}+\dfrac{\lambda_0}{\Lambda}\dfrac{v_3}{n_3}<1$.
- Number of diffraction lobes: $-\dfrac{\Lambda}{\lambda_0}\left(n_3+n_{eff}^{(m)}\right)\le v_3\le \dfrac{\Lambda}{\lambda_0}\left(n_3-n_{eff}^{(m)}\right)$.
- Since the substrate index is usually larger than the clad index ($n_1>n_3$), there are more diffraction orders toward the substrate than toward the clad. To avoid too many orders it is common to couple from the substrate side, with coupling angles $\sin\theta_3=\dfrac{\lambda_0}{n_3\Lambda}\left[\dfrac{\Lambda}{\lambda_{eff}}+v_3\right]$, $\sin\theta_1=\dfrac{\lambda_0}{n_1\Lambda}\left[\dfrac{\Lambda}{\lambda_{eff}}+v_1\right]$, where $\lambda_{eff}=\lambda_0/n_{eff}^{(m)}$.
- Equivalent $k$-vector form: $k_1\sin\theta_1=\beta^{(m)}+Kv_1$, $k_3\sin\theta_3=\beta^{(m)}+Kv_3$, with $K=2\pi/\Lambda$ and $k_{1,3}=k_0n_{1,3}$.

### k-Vector Picture

- $k_{1,3}\sin\theta_{1,3}$ is the $z$-projection of a point on a circle of radius $k_{1,3}$ centered at the origin.
- $\beta^{(m)}+Kv_{1,3}$ is a comb of marks on the $z$-axis, centered on $\beta^{(m)}$ and spaced by $K=2\pi/\Lambda$.
- An order $v$ is real only if its mark lies inside the circle — its angle is where the vertical line through that mark meets the circle. Marks outside the circle give no propagating order (the diffraction-order bound above, seen graphically).

## Derivation Outline

1. Require phase matching between the impinging free-space wave's in-plane wavevector and the guided mode, allowing the grating to add momentum in units of its reciprocal vector $2\pi/\Lambda$.
2. Substitute $k_{1,3}=k_0n_{1,3}$ and $\beta^{(m)}=k_0n_{eff}^{(m)}$ to express the condition directly in terms of angle, wavelength, and grating period.
3. Bound $\sin\theta_3$ (and $\sin\theta_1$) between $-1$ and $1$ to find which diffraction orders $v_3$ ($v_1$) actually produce a real coupling angle — this sets the number of diffraction lobes.
4. Since $n_1>n_3$ typically, more orders couple toward the substrate than the clad; to get a single clean order it is common to couple from the substrate side and choose $\Lambda$ so only one order has a real solution.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Waveguide Coupling Condition](Waveguide%20Coupling%20Condition.md), [Prism Coupling](Prism%20Coupling.md)
**Full Derivation:**
