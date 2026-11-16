---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

A periodic dielectric structure is invariant under shifts by lattice vectors $\vec R$, so its permittivity is a Fourier series over a discrete set of vectors $\vec G$ — the reciprocal lattice — each satisfying $\vec G\cdot\vec R=2\pi N$ for every lattice vector.

## Key Equation

$$
\vec G\cdot\vec R=2\pi N,\qquad \vec R=l\,\vec a_1+m\,\vec a_2+n\,\vec a_3,\quad \vec G=l'\,\vec b_1+m'\,\vec b_2+n'\,\vec b_3
$$

**Derived From:** starting with the translation symmetry $\varepsilon_r(\vec r)=\varepsilon_r(\vec r+\vec R)$ and the Fourier expansion $\varepsilon_r(\vec r)=\sum_{\vec G}\varepsilon_{\vec G}e^{-i\vec G\cdot\vec r}$, applying the shift gives $\sum_{\vec G}\varepsilon_{\vec G}e^{-i\vec G\cdot\vec r}\left(1-e^{-i\vec G\cdot\vec R}\right)=0$; a Fourier series vanishes only if every component vanishes, so $e^{-i\vec G\cdot\vec R}=1$.

- $\vec a_i$ — lattice vectors defining the positions of the unit cells (up to 3); $l,m,n$ and $l',m',n'$ are integers
- $\vec b_j$ — reciprocal lattice vectors, "orthogonal" to the regular lattice

## Supporting Formulas

- $$ \varepsilon_r(x)=\sum_{n=-\infty}^{\infty}\varepsilon_n e^{-i\frac{2\pi}{\Lambda}nx} $$ — 1D periodic structure of period $\Lambda$ as a Fourier series
- $$ \vec G_n=\frac{2\pi}{\Lambda}\,n\,\hat x $$ — reciprocal lattice in 1D
- $$ \varepsilon_r(\vec r)=\sum_{\vec G}\varepsilon_{\vec G}e^{-i\vec G\cdot\vec r},\qquad \varepsilon_{\vec G}=V_c^{-1}\int_{cell}\varepsilon_r(\vec r)\,e^{i\vec G\cdot\vec r}\,dv $$ — 3D expansion; $V_c$ is the unit-cell volume
- $$ \vec a_i\cdot\vec b_j=2\pi\delta_{ij} $$ — orthogonality, a simple (not the only) choice of solution
- $$ \vec b_1=2\pi\frac{\vec a_2\times\vec a_3}{\vec a_1\cdot(\vec a_2\times\vec a_3)},\quad \vec b_2=2\pi\frac{\vec a_3\times\vec a_1}{\vec a_1\cdot(\vec a_2\times\vec a_3)},\quad \vec b_3=2\pi\frac{\vec a_1\times\vec a_2}{\vec a_1\cdot(\vec a_2\times\vec a_3)} $$ — the set $\vec b_j$ this choice gives
- Square lattice: $\vec a_1=a\hat x,\ \vec a_2=a\hat y\ \Rightarrow\ \vec b_1=\tfrac{2\pi}{a}\hat x,\ \vec b_2=\tfrac{2\pi}{a}\hat y$
- Hexagonal lattice: $\vec a_{1,2}=\tfrac a2(\hat x\pm\sqrt3\,\hat y)\ \Rightarrow\ \vec b_{1,2}=\tfrac{2\pi}{a}(\hat x\pm\hat y/\sqrt3)$ (as drawn on the slide)
- Rectangular 2D example from the lecture: $\vec a_1=2\hat x,\ \vec a_2=\hat y$

## Derivation Outline

1. Periodic structure: $\varepsilon_r(\vec r)=\varepsilon_r(\vec r+\vec R)$ with $\vec R$ a lattice vector
2. Expand $\varepsilon_r$ in a Fourier series over $\vec G$
3. Shift by $\vec R$ and subtract — the series must vanish term by term
4. Hence $\vec G\cdot\vec R=2\pi N$; write $\vec G$ in its own basis $\vec b_j$ and pick $\vec a_i\cdot\vec b_j=2\pi\delta_{ij}$

## Physical Intuition


## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Bloch Theorem](Bloch%20Theorem.md)
**Full Derivation:** 
