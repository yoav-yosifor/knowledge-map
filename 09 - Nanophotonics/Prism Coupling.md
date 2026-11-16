---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A prism of index $n_p>n_{eff}$ supplies the extra momentum a free-space beam is missing to couple into a waveguide: the beam totally-internally-reflects inside the prism, its evanescent tail crosses a thin air gap, and it re-emerges as the waveguide's guided wave — and by reciprocity, the same geometry couples light back out of the waveguide.

## Key Equation

$$
n_p\sin\theta_p=n_2\sin\theta_2=n_{eff}
\;\Rightarrow\;
n_p=\frac{n_{eff}}{\sin\theta_p}
$$

**Derived From:** stated directly in the source via Snell's law at the prism-waveguide interface; a real solution requires $n_p>n_{eff}$.

## Supporting Formulas

- Leaky-wave field profile outside the coupling region: $\left|E\right|=\begin{cases}0 & z_r<0\\ E_0e^{-\alpha z_r\sec\theta} & z_r>0\end{cases}$, with equivalent width $W_{eq}$ set by $\alpha\cdot W_{eq}=\cos\theta$ and $\sin\theta=\beta/n_pk_0\approx\beta_{WG}/n_pk_0$.
- Full field profile near the coupling point: $E=E_0\exp(-ik_0x_r-\alpha z_r\sec\theta)\cdot\mathrm{erfc}\!\left(\dfrac{\alpha W}{2}-\dfrac{x_r}{W}\right)$, $W^2=-2i\,x/k_0\cos\theta$.
- The decay constant $\alpha$ is set by the prism–waveguide gap: $\alpha\propto e^{-2\gamma_ah_a}$, where $h_a$ is the gap thickness and $\gamma_a=k_0\sqrt{n_{eff}^2-n_a^2}$ is the field's decay constant in the gap.
- For good out-coupling it is desired that $\beta\approx\beta_{WG}\gg\alpha$, where $\beta_{WG}$ is the waveguide's propagation constant.
- Out-coupling efficiency: $\eta=1-e^{-2\alpha l_p}$, where $l_p$ is the coupling-region length; $\eta\to1$ as $l_p\to\infty$.
- In-coupling efficiency as a mode-overlap integral: $\eta=\dfrac{\left|\int E_{out}^*(z_r)E_{in}(z_r)\,dz_r\right|^2}{\int\left|E_{out}(z_r)\right|^2dz_r\int\left|E_{in}(z_r)\right|^2dz_r}$.
- Optimal incident-beam parameters (beam waist $w$, aiming point $z_c$): for a Gaussian beam, $2\alpha w_0=1.36$, $z_c/w_0=0.733$, giving $\eta_{Gauss}=80.1\%$; for a rectangular beam of width $b$, $\alpha b_0=1.25$, $z_c/b_0=0.5$, $b_0=b\sec\theta$, giving $\eta_{Rect}=81\%$. The efficiency is relatively insensitive to the beam parameters.

## Derivation Outline

1. Require phase matching at the prism-base interface: $n_p\sin\theta_p=n_2\sin\theta_2$ (Snell's law).
2. At resonance the wave at the prism base couples to the guided mode, whose effective index is $n_{eff}$, so $n_2\sin\theta_2=n_{eff}$.
3. Combine the two to get $n_p\sin\theta_p=n_{eff}$, which requires $n_p>n_{eff}$ for a real solution to exist.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Waveguide Coupling Condition](Waveguide%20Coupling%20Condition.md), [Frustrated Total Internal Reflection](Frustrated%20Total%20Internal%20Reflection.md), [Leaky Waveguide Modes](Leaky%20Waveguide%20Modes.md), [Grating Coupling](Grating%20Coupling.md)
**Full Derivation:**
