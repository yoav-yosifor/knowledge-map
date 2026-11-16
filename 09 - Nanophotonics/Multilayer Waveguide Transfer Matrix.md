---
tags:
  - nanophotonics
  - system
  - device
---
---
## Overview

A general method for finding the guided modes of a stack of $N$ parallel dielectric (or magnetic) layers, each with its own $(\varepsilon_k,\mu_k)$, by representing the field in every layer as a 2-vector of forward/backward exponential amplitudes and relating adjacent layers through a $2\times2$ transfer matrix built from the boundary conditions — reducing the whole multilayer eigenvalue problem to finding the roots of one scalar equation in $\beta$.

Per layer $k$ (interfaces at $x=d_{k-1}$ and $x=d_k$), the master field obeys a 1D Helmholtz equation with piecewise-constant index:
$$
\frac{\partial^2E_y^{(k)}}{\partial x^2}-\left(\beta^2-n_k^2k_0^2\right)E_y^{(k)}=0, \qquad E_y^{(k)}=A_ke^{p_kx}+B_ke^{-p_kx}
$$
with $p_k=\bar p_k=\sqrt{|\beta^2-n_k^2k_0^2|}$ if $\beta>n_kk_0$, or $p_k=i\bar p_k$ if $\beta<n_kk_0$. Matching the boundary conditions (TE: $E_y,\tfrac1\mu\partial_xE_y$ continuous; TM: $H_y,\tfrac1\varepsilon\partial_xH_y$ continuous) at each interface gives a transfer matrix $\bar T_{k+1,k}$ relating the amplitude vectors of adjacent layers, $E^o_{k+1}=\bar T_{k+1,k}\cdot E^o_k$ with $E^o_k=(A_k,B_k)^T$:

$$
\bar T_{k+1,k} = \frac12\begin{pmatrix}a_{k+1,k}r_{k+1,k} & b_{k+1,k}^{-1}s_{k+1,k}\\ b_{k+1,k}s_{k+1,k} & a_{k+1,k}^{-1}r_{k+1,k}\end{pmatrix}, \qquad
\begin{aligned}
a_{k+1,k}&=e^{(p_k-p_{k+1})d_k}, & b_{k+1,k}&=e^{(p_k+p_{k+1})d_k}\\
r_{k+1,k}&=1+\frac{p_k\alpha_k}{p_{k+1}\alpha_{k+1}}, & s_{k+1,k}&=1-\frac{p_k\alpha_k}{p_{k+1}\alpha_{k+1}}
\end{aligned}
$$

$a_{k+1,k},b_{k+1,k}$ carry the propagation phase/decay accumulated across the interface; $r_{k+1,k},s_{k+1,k}$ carry the impedance mismatch between the two layers (equal layers give $r=2,s=0$ — no reflection). Full derivation of these elements from the boundary conditions: [Multilayer Transfer Matrix Derivation](Multilayer%20Transfer%20Matrix%20Derivation.md).

Concatenating these across all $N$ layers relates the two outermost (semi-infinite) layers directly:

$$
\begin{pmatrix}A_{N+1}\\B_{N+1}\end{pmatrix}=\bar T_{N+1,0}\begin{pmatrix}A_0\\B_0\end{pmatrix}=\begin{pmatrix}t^{11}_{N+1,0}&t^{12}_{N+1,0}\\t^{21}_{N+1,0}&t^{22}_{N+1,0}\end{pmatrix}\begin{pmatrix}A_0\\B_0\end{pmatrix}
$$

The [Radiation Condition](Radiation%20Condition.md) — no wave enters from either semi-infinite outer layer — sets $A_{N+1}=0$ and $B_0=0$; with $A_0=1$ (free normalization) this collapses the matrix relation to a single scalar equation:

$$
\begin{pmatrix}0\\B_{N+1}\end{pmatrix}=\begin{pmatrix}t^{11}_{N+1,0}&t^{12}_{N+1,0}\\t^{21}_{N+1,0}&t^{22}_{N+1,0}\end{pmatrix}\begin{pmatrix}1\\0\end{pmatrix} \quad\Longrightarrow\quad t^{11}_{N+1,0}(\beta)=0
$$

whose roots give the allowed propagation constants $\beta$; from each $\beta$, the $T$ matrices and full modal field profile follow.

## Prerequisite Concepts

- [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md) — the two-interface special case ($N=1$ layer) that this method generalizes.
- [Radiation Condition](Radiation%20Condition.md) — the boundary condition on the two outermost (semi-infinite) layers that closes the eigenvalue problem for $\beta$.

## Regimes and Parameters

- Each layer's $p_k$ comes out real (evanescent, decaying field) if $\beta>n_kk_0$, or imaginary (oscillatory, radiating field) if $\beta<n_kk_0$ — the same formalism covers both guided and radiating layers, distinguished only by which branch $p_k$ falls on.
- The polarization sets which boundary-matching constant is used: $\alpha_k=1/\mu_k$ for TE, $\alpha_k=1/\varepsilon_k$ for TM (generally $\varepsilon_k=n_k^2$, $\mu_k=1$).
- The allowed range of effective index for a guided wave is bounded by the two outermost layers' indices and the largest index anywhere in the stack: $n_{N+1}<n_{eff}<n_{max}$, with $n_{eff}=\beta/k_0$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md)
**Concepts Used:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md), [Radiation Condition](Radiation%20Condition.md)
