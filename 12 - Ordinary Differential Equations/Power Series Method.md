---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

When the coefficients of a linear ODE are functions rather than constants and the standard tools fail, assume the solution is a power series, substitute it into the ODE, and use the resulting recurrence relation to find the coefficients.

## Key Equation

$$
y(x)=\sum_{n=0}^{\infty}a_n\,(x-x_0)^n
$$

**Derived From:** the source's rationale — assume $y(x)$ has a power series expansion around some point $x_0$ (the point around which the series is developed). Then differentiate as needed, substitute into the ODE, rearrange, merge the sums, and arrive at a recurrence relation that gives the solution as a series.

## Supporting Formulas

- Termwise derivatives for a series around $x_0=0$: $\;y'=\sum_{n=1}^{\infty}na_nx^{n-1},\quad y''=\sum_{n=2}^{\infty}n(n-1)a_nx^{n-2}$.
- **Shifting the index** (e.g. $m=n-2\Rightarrow n=m+2$) so that all sums have the same power $x^m$ and can be merged.
- If a sum starts at a lower index than the others, **pull out terms** so that all sums start at the same $n$, and compare the pulled-out terms separately.
- The series equals $0$ for all $x$, so the coefficient of each power $x^m$ must be $0$; this gives the recurrence relation.
- Example 1: $y''+y=0$, $y(0)=0$, $y'(0)=1$, around $x=0$. Substituting gives $\sum_{m=0}^{\infty}\left[(m+2)(m+1)a_{m+2}+a_m\right]x^m=0$, so $a_{m+2}=-\dfrac{a_m}{(m+2)(m+1)}$. Then $a_2=-\dfrac{a_0}{2\cdot1}$, $a_3=-\dfrac{a_1}{2\cdot3}$, $a_4=\dfrac{a_0}{4!}$, $a_5=\dfrac{a_1}{5!}$, and in general for odd terms $a_{2n+1}=(-1)^n\dfrac{a_1}{(2n+1)!}$. The initial conditions give $a_0=0$ (so all even terms vanish) and $a_1=1$, so $y(x)=\sum_{n=0}^{\infty}(-1)^n\dfrac{x^{2n+1}}{(2n+1)!}=\sin(x)$.
- Example 2: $y'=\dfrac{2x-y}{1-x}$, general solution around $x=0$ with $y=\sum c_nx^n$. Multiply by $(1-x)$: $(1-x)\sum_{n=1}^{\infty}nc_nx^{n-1}=2x-\sum_{n=0}^{\infty}c_nx^n$. After shifting the index and pulling out terms: $\sum_{n=2}^{\infty}\left[(n+1)c_{n+1}-nc_n+c_n\right]x^n+c_0-2x+c_1+(2c_2-c_1+c_1)x=0$. Comparing coefficients: $c_0+c_1=0$ (so $c_0=-c_1$); $2c_2-2=0$ (so $c_2=1$); and for $n\ge2$: $(n+1)c_{n+1}-nc_n+c_n=0$, i.e. $c_{n+1}=\dfrac{n-1}{n+1}c_n$. This gives $c_3=\tfrac13$, $c_4=\tfrac16$, $c_5=\tfrac1{10}$, … and $y=c_0(1-x)+\left(x^2+\tfrac13x^3+\tfrac16x^4+\tfrac1{10}x^5+\tfrac1{15}x^6+\dots\right)$.

## Derivation Outline

1. Assume $y=\sum a_n(x-x_0)^n$ and differentiate as many times as the ODE requires.
2. Substitute into the ODE (multiply out any denominators first).
3. Shift indices (and pull out terms if needed) so that all sums have the same power and the same starting index.
4. Merge the sums and set the coefficient of each power to zero to get a recurrence relation (plus separate equations for the pulled-out terms).
5. Compute the coefficients from the recurrence and write the series; use initial conditions to fix the free coefficients.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE.md), [Initial Value Problem](../12%20-%20Ordinary%20Differential%20Equations/Initial%20Value%20Problem.md), [Higher-Order ODE Solutions](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20ODE%20Solutions.md)
**Full Derivation:** 
