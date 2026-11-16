---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

Waves in a periodic structure are a plane wave $e^{-i\vec K\cdot\vec r}$ times a function that has the periodicity of the lattice, so moving one unit cell only multiplies the wave by a phase.

## Key Equation

$$
\vec E=\vec E_{\vec K}(\vec r)\,e^{-i\vec K\cdot\vec r}
$$

**Derived From:** starting with the wave equation $\nabla^2E+\varepsilon_r(x)k_0^2E=0$ and a Fourier-integral field, applying the Fourier series of $\varepsilon_r$ couples each $k$ only to $k-\tfrac{2\pi}{\Lambda}m$; each coupled group, labelled by its smallest wavenumber $K$, sums to $e^{-iKx}$ times a $\Lambda$-periodic function. Full steps in [Bloch Theorem Derivation](Bloch%20Theorem%20Derivation.md).

- $\vec E_{\vec K}(\vec r)$ — Bloch function, periodic with the lattice
- $\vec K$ — Bloch wave vector (wavenumber $K$ in 1D); can be complex, in which case it also modifies the amplitude

## Supporting Formulas

- $$ E(x+\Lambda)=e^{-iK\Lambda}E(x) $$ — crossing one unit cell gives a phase shift $e^{-iK\Lambda}$
- $$ -\frac{\pi}{\Lambda}<K<\frac{\pi}{\Lambda} $$ — range over which $K$ needs to be defined
- $$ E_K(x)=\sum_m A\!\left(K-\frac{2\pi}{\Lambda}m\right)e^{i\frac{2\pi}{\Lambda}mx} $$ — the Bloch function, a Fourier series with period $\Lambda$
- $$ k^2A(k)-k_0^2\sum_{m=-\infty}^{\infty}\varepsilon_mA\!\left(k-\frac{2\pi}{\Lambda}m\right)=0 $$ — the infinite set of coupled equations that splits into groups

## Derivation Outline

1. Insert $E(x)=\int A(k)e^{-ikx}dk$ and the Fourier series of $\varepsilon_r$ into the wave equation
2. Shift the integration variable and relabel the dummy variable
3. A Fourier transform is zero only if every component is zero: one equation for every $k$
4. The equations separate into groups where $k$ couples only to $k-\tfrac{2\pi}{\Lambda}m$; label each group by its smallest wavenumber $K$
5. Summing a group gives $E(x)=e^{-iKx}E_K(x)$ with $E_K$ periodic

## Physical Intuition


## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Reciprocal Lattice](Reciprocal%20Lattice.md), [Distributed Bragg Reflector](Distributed%20Bragg%20Reflector.md)
**Full Derivation:** [Bloch Theorem Derivation](Bloch%20Theorem%20Derivation.md)
