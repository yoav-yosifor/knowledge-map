---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

An inner product on a vector space $V$ over $\mathbb{F}=\mathbb{R}$ or $\mathbb{C}$ is a function $\langle\cdot,\cdot\rangle:V\times V\to\mathbb{F}$ that assigns a scalar to every pair of vectors and satisfies linearity in the first slot, Hermitian symmetry, and positivity.

## Key Equation

*The three axioms, for all $\alpha\in\mathbb{F}$ and $v,u,w\in V$:*

$$
\langle\alpha v+u,\,w\rangle=\alpha\langle v,w\rangle+\langle u,w\rangle,\qquad \langle v,u\rangle=\overline{\langle u,v\rangle},\qquad \langle v,v\rangle\ge 0\ \text{ and }\ \langle v,v\rangle=0\iff v=0
$$

**Derived From:** definition, for $V$ a vector space over $\mathbb{F}$ — the source splits the axioms as (1) linearity in the first component, (2) Hermitian symmetry, (3) non-negativity.

## Supporting Formulas

Axiom 1, split into its two parts:

- $$ \langle\alpha v,w\rangle=\alpha\langle v,w\rangle $$ — homogeneity in the first slot
- $$ \langle v+u,w\rangle=\langle v,w\rangle+\langle u,w\rangle $$ — additivity in the first slot

Axiom 2 and 3 remarks:

- If $\mathbb{F}=\mathbb{R}$, Hermitian symmetry reduces to ordinary symmetry: $\langle v,u\rangle=\langle u,v\rangle$.
- From axiom 2, $\langle v,v\rangle=\overline{\langle v,v\rangle}$, hence $\langle v,v\rangle\in\mathbb{R}$ (this is what makes "$\ge 0$" meaningful).

Properties that follow:

- $$ \langle v,\alpha u+w\rangle=\bar\alpha\langle v,u\rangle+\langle v,w\rangle $$ — conjugate-linear (almost linear) in the second slot
- $$ \Big\langle\sum_{i=1}^{n}\alpha_i v_i,\ \sum_{j=1}^{m}\beta_j w_j\Big\rangle=\sum_{i=1}^{n}\sum_{j=1}^{m}\alpha_i\bar\beta_j\langle v_i,w_j\rangle $$ — generalization (the source leaves the proof as a homework exercise)
- $$ \langle 0,v\rangle=\langle v,0\rangle=0\quad\forall v\in V $$

**Examples (from the source):**

- $V=\mathbb{R}^n$ over $\mathbb{R}$ — the dot product: $\langle x,y\rangle=\sum_{i=1}^{n}x_iy_i=x^{t}y$
- $V=\mathbb{C}^n$ over $\mathbb{C}$: $\langle z,w\rangle=\sum_{i=1}^{n}z_i\bar w_i=z^{t}\bar w$

## Derivation Outline

1. Take a candidate function $V\times V\to\mathbb{F}$.
2. Check linearity in the first component.
3. Check Hermitian symmetry.
4. Check non-negativity and that $\langle v,v\rangle=0$ only for $v=0$.

## Physical Intuition

A bare vector space only knows how to add vectors and scale them; it has no built-in geometry. The inner product is the tool that adds all the geometric concepts to the space. That is why an inner product space is, in one phrase, "vector space + geometry". The [norm](../11%20-%20Linear%20Algebra/Norm.md) it induces is the first of these geometric notions.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Vector Spaces](../11%20-%20Linear%20Algebra/Vector%20Spaces.md), [Norm](../11%20-%20Linear%20Algebra/Norm.md), [Cauchy-Schwarz Inequality](../11%20-%20Linear%20Algebra/Cauchy-Schwarz%20Inequality.md), [Transpose](../11%20-%20Linear%20Algebra/Transpose.md), [Complex Conjugate](../11%20-%20Linear%20Algebra/Complex%20Conjugate.md), [Inner and Outer Products](../10%20-%20Quantum%20Information/Inner%20and%20Outer%20Products.md)
**Full Derivation:** 
