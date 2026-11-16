---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

A vector space $V$ over a field $\mathbb{F}$ is an algebraic structure closed under addition and scalar multiplication that satisfies a list of axioms.

## Key Equation

*Closure:*

$$
v_1+v_2\in V\quad\forall v_1,v_2\in V,\qquad \alpha v\in V\quad\forall\alpha\in\mathbb{F},\ v\in V
$$

**Derived From:** definition, for $V$ over a field $\mathbb{F}$ — closure plus the eight axioms below.

## Supporting Formulas

Axioms of addition, for all $u,v,w\in V$:

- $$ u+(v+w)=(u+v)+w $$ — associativity of addition
- $$ u+v=v+u $$ — commutativity of addition
- $$ \exists\,0_V\in V:\ v+0_V=v\ \ \forall v\in V $$ — neutral element for addition
- $$ \forall v\ \exists\,{-v}\in V:\ v+(-v)=0_V $$ — additive inverse

Axioms of scalar multiplication, for all $\alpha,\beta\in\mathbb{F}$, $u,v\in V$:

- $$ \alpha(\beta v)=(\alpha\beta)v $$ — associativity of scalars
- $$ 1_{\mathbb{F}}\,v=v $$ — neutral scalar
- $$ \alpha(u+v)=\alpha u+\alpha v $$ — distributivity over vector addition
- $$ (\alpha+\beta)v=\alpha v+\beta v $$ — distributivity over scalar addition

Properties that follow from the axioms:

- $$ (-1_{\mathbb{F}})v=-v $$
- $$ 0_{\mathbb{F}}\,v=0_V $$
- $$ \alpha v=0_V\ \Rightarrow\ \alpha=0_{\mathbb{F}}\ \text{ or }\ v=0_V $$

**Examples (from the source):**

- $\mathbb{F}^{m\times n}$ with the usual matrix addition and scalar multiplication
- $\mathbb{F}_n[x]=\{a_0+a_1x+\cdots+a_nx^n\mid a_i\in\mathbb{F}\}$ — polynomials of degree at most $n$; the source checks every axiom coefficient-wise, e.g. the zero polynomial is the neutral element and $-f=(-a_0)+(-a_1)x+(-a_2)x^2$
- $\mathbb{F}[x]=\{a_0+\cdots+a_nx^n\mid a_i\in\mathbb{F},\ n\in\mathbb{N}\}$ — all polynomials (note: not the same as $\mathbb{F}_n[x]$)
- $\mathbb{F}^n=\{(a_1,\dots,a_n)\mid a_i\in\mathbb{F}\}$ with componentwise operations
- $V=\mathbb{R}$ over $\mathbb{F}=\mathbb{Q}$ is a vector space
- $V=\mathbb{C}^3$ over $\mathbb{F}=\mathbb{R}$ is a vector space
- **Non-example:** $V=\mathbb{R}^3$ over $\mathbb{F}=\mathbb{C}$ is *not* a vector space, since $i(1,1,1)=(i,i,i)\notin V$ (closure under scalars fails)

## Derivation Outline

1. State the two closure conditions.
2. Require the four axioms of addition and the four axioms of scalar multiplication.
3. Check them for a candidate structure — coefficient-wise for polynomials.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Subspaces](../11%20-%20Linear%20Algebra/Subspaces.md), [Linear Combinations](../11%20-%20Linear%20Algebra/Linear%20Combinations.md), [Matrices](../11%20-%20Linear%20Algebra/Matrices.md), [Matrix Addition and Scaling](../11%20-%20Linear%20Algebra/Matrix%20Addition%20and%20Scaling.md)
**Full Derivation:** 
