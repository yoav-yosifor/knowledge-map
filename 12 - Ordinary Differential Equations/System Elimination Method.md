---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

A two-equation linear system can be turned into a single second-order ODE for one unknown by differentiating one equation and eliminating the other unknown, then the second unknown is recovered from the first. (The source calls this the Gauss method.)

## Key Equation

$$
\begin{cases}x'=a_{11}x+a_{12}y+f_1(t)\\ y'=a_{21}x+a_{22}y+f_2(t)\end{cases}\ \Longrightarrow\ x''+p\,x'+q\,x=g(t)
$$

**Derived From:** the source's procedure — differentiate the first equation, substitute $y'$ from the second, and substitute $y$ from the first equation. This gives a second-order linear ODE for $x$ alone (the coefficients $p,q$ and the right-hand side $g$ depend on the system).

## Supporting Formulas

Procedure (from the source):

1. Differentiate the first equation.
2. Take $y'$ from the second equation.
3. Take $y$ from the first equation.
4. Solve the homogeneous equation.
5. Solve the non-homogeneous equation by the [guessing method](../12%20-%20Ordinary%20Differential%20Equations/Undetermined%20Coefficients.md).
6. This gives $x(t)$.
7. Substitute $x,x'$ into the (isolated) expression for $y$ to find $y$.
8. Find $c_1,\dots,c_n$ from the initial conditions for a particular solution.

Example 1: $x'=5x-3y+2e^{3t}$, $y'=x+y+5e^{-t}$, $x(0)=-3$, $y(0)=\tfrac83$.
- Eliminating $y$ gives $x''-6x'+8x=4e^{3t}-15e^{-t}$; $\lambda^2-6\lambda+8=0$ gives $\lambda=2,4$, so $x_h=c_1e^{2t}+c_2e^{4t}$.
- Guessing $\tilde x_1=Ae^{3t}$, $\tilde x_2=Be^{-t}$ gives $A=-4$, $B=-1$, so $x(t)=c_1e^{2t}+c_2e^{4t}-4e^{3t}-e^{-t}$.
- From $3y=5x-x'+2e^{3t}$: $y(t)=c_1e^{2t}+\tfrac13c_2e^{4t}-2e^{3t}-2e^{-t}$.
- **Flag:** the source then substitutes the initial conditions and gets $c_1=\tfrac52$, $c_2=-\tfrac12$ with a final answer $y(t)=-\tfrac56e^{2t}+\tfrac23e^{4t}+4e^{3t}-\tfrac13e^{-t}$. That last $y(t)$ does not match the general $y(t)$ above (and the source's $y(0)$ substitution uses different coefficients than that $y$), so the initial-condition step in the source should be re-checked.

Example 2: $x'=x-y+8t$, $y'=5x-y$, $x(0)=-3$, $y(0)=\tfrac83$.
- Eliminating $y$ gives $x''+4x=8t+8$; $\lambda=\pm2i$, so $x_h=c_1\cos2t+c_2\sin2t$; guess $\tilde x=At+B$ gives $A=B=2$.
- $x(t)=c_1\cos2t+c_2\sin2t+2t+2$, and from $y=x-x'+8t$: $y(t)=(c_1-2c_2)\cos2t+(2c_1+c_2)\sin2t+10t$.
- Initial conditions: $c_1=-5$, $c_2=-\tfrac{23}{6}$, so
  $x(t)=-5\cos2t-\tfrac{23}{6}\sin2t+2t+2$ and $y(t)=\tfrac83\cos2t-\tfrac{83}{6}\sin2t+10t$.

## Derivation Outline

1. Differentiate the first equation and use the second to replace $y'$.
2. Use the first equation to replace $y$, getting a second-order ODE for $x$.
3. Solve it (characteristic polynomial for $x_h$, guessing for $x_p$).
4. Recover $y$ from the first equation using $x$ and $x'$.
5. Use the initial conditions for the two constants.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [ODE Systems](../12%20-%20Ordinary%20Differential%20Equations/ODE%20Systems.md), [Characteristic Equation Method](../12%20-%20Ordinary%20Differential%20Equations/Characteristic%20Equation%20Method.md), [Undetermined Coefficients](../12%20-%20Ordinary%20Differential%20Equations/Undetermined%20Coefficients.md), [System Eigenvalue Method](../12%20-%20Ordinary%20Differential%20Equations/System%20Eigenvalue%20Method.md)
**Full Derivation:** 
