---
tags:
  - electromagnetism
  - concept
---
---
## Core Idea

In a homogeneous, isotropic, source-free medium, plane-wave solutions of the Helmholtz equation need not have real wavevector components — allowing $k_x,k_z$ to be complex gives "inhomogeneous" plane waves whose surfaces of constant phase and surfaces of constant amplitude are both planes, but no longer parallel (or even coincident) with each other.

## Key Equation

$$
A(x,z)=A_0e^{-i(k_xx+k_zz)}, \qquad k_x^2+k_z^2=k_0^2
$$

**Derived From:** the homogeneous Helmholtz equation $(\nabla^2+k_0^2)A(x,z)=0$; substituting the plane-wave ansatz gives the dispersion relation $k_x^2+k_z^2=k_0^2$, which places no requirement that $k_x,k_z$ individually be real.

## Supporting Formulas

- Writing $k_x=b-ia$, $k_z=\beta-i\alpha$ (all four real), the dispersion relation splits into real and imaginary parts:
  $$
  \beta^2-\alpha^2+b^2-a^2=k_0^2, \qquad ab+\beta\alpha=0
  $$
- Equi-phase planes: $bx+\beta z=\text{const}$. Equi-amplitude planes: $ax+\alpha z=\text{const}$. The field's amplitude is $|A(x,z)|^2=A_0^2e^{-2\alpha z-2ax}$ — not constant along a plane of constant phase, which is the defining feature of an inhomogeneous wave.
- The [Fresnel coefficients](Fresnel%20Coefficients.md) extend directly to this complex-$k_x$ case:
  $$
  r_{TE}=\frac{k_{x,1}-k_{x,2}}{k_{x,1}+k_{x,2}}, \qquad r_{TM}=\frac{k_{x,1}-\left(\tfrac{n_1}{n_2}\right)^2k_{x,2}}{k_{x,1}+\left(\tfrac{n_1}{n_2}\right)^2k_{x,2}}
  $$
- In a TIR scenario, if $k_{x,2}$ is not purely imaginary then $|r|\neq1$ — i.e. there is no TIR for inhomogeneous plane waves in general.

## Derivation Outline

1. Start from the homogeneous Helmholtz equation for a plane wave and allow $k_x,k_z$ to be complex, $k_x=b-ia$, $k_z=\beta-i\alpha$.
2. Separate the resulting dispersion relation into real and imaginary parts: $\beta^2-\alpha^2+b^2-a^2=k_0^2$ and $ab+\beta\alpha=0$.
3. Identify the equi-phase planes ($bx+\beta z=\text{const}$) and equi-amplitude planes ($ax+\alpha z=\text{const}$) from the real and imaginary parts of the exponent.
4. Extend the Fresnel coefficients to this complex-$k_x$ case; note that TIR's unimodular reflection ($|r|=1$) requires $k_{x,2}$ to be purely imaginary, which does not hold in general for inhomogeneous waves — so ordinary TIR does not occur between two inhomogeneous-wave regions.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Fresnel Coefficients](Fresnel%20Coefficients.md), [TIR Phase Shift](../05%20-%20Optics/TIR%20Phase%20Shift.md)
**Full Derivation:**
