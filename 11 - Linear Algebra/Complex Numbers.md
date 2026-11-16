---
tags:
  - linear-algebra
  - concept
---
---
## Core Idea

The complex numbers extend the reals by defining a new number $i$ that solves $x^2+1=0$, giving the set of all $a+bi$ with real $a,b$, on which addition and multiplication are defined naturally by treating $i$ like an ordinary number with $i^2=-1$.

## Key Equation

$$
\mathbb{C}=\{a+bi \mid a,b\in\mathbb{R}\},\qquad i^2=-1
$$

**Derived From:** the equation $x^2+1=0$ has no real solution, so a solution $i$ is defined by fiat, and the reals are extended to include it.

## Supporting Formulas

- $$ \mathbb{R}\subset\mathbb{C} \quad (\forall r\in\mathbb{R} \leftrightarrow r+0\cdot i\in\mathbb{C}) $$ — every real is a complex number with zero imaginary part
- $$ a+bi=c+di \iff a=c,\ b=d $$ — equality is component-wise
- $$ \operatorname{Re}(z)=a,\quad \operatorname{Im}(z)=b \quad (z=a+bi) $$ — real and imaginary parts
- $$ z=bi \ \ (\operatorname{Re}(z)=0) $$ — called purely imaginary
- $$ z_1+z_2:=(a_1+a_2)+(b_1+b_2)i $$ — addition; e.g. $(2+4i)+(\pi-2i)=(2+\pi)+2i$
- $$ (a_1+b_1i)(a_2+b_2i)=(a_1a_2-b_1b_2)+(b_1a_2+a_1b_2)i $$ — multiplication; e.g. $(1+i)(1-i)=1^2-i^2=2$
- $$ (a,b)\leftrightarrow a+bi $$ — vector representation in $\mathbb{R}^2$ (the complex plane)
- $$ (a_1,b_1)+(a_2,b_2)=(a_1+a_2,\,b_1+b_2) $$ — addition is ordinary vector addition
- $$ (a_1,b_1)\cdot(a_2,b_2)=(a_1a_2-b_1b_2,\,a_1b_2+a_2b_1) $$ — multiplication, matching the definition above

## Derivation Outline

1. Expand the product term by term, treating $i$ as an ordinary number: $a_1a_2+b_1a_2i+a_1b_2i+b_1b_2i^2$.
2. Substitute $i^2=-1$ and collect real and imaginary parts: $(a_1a_2-b_1b_2)+(b_1a_2+a_1b_2)i$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Complex Conjugate](../11%20-%20Linear%20Algebra/Complex%20Conjugate.md), [Complex Modulus](../11%20-%20Linear%20Algebra/Complex%20Modulus.md), [Complex Inverse](../11%20-%20Linear%20Algebra/Complex%20Inverse.md), [Complex Polar Form](../11%20-%20Linear%20Algebra/Complex%20Polar%20Form.md)
**Full Derivation:** 
