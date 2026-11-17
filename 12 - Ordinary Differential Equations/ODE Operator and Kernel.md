---
tags:
  - ordinary-differential-equations
  - concept
---
---
## Core Idea

The derivative can be treated as an operator $D$, so a linear ODE becomes $Ty=g$ for a linear operator $T$, and the solutions of the homogeneous ODE are exactly the kernel of $T$.

## Key Equation

$$
T=D^n+a_{n-1}D^{n-1}+\cdots+a_0I,\qquad Ty=g(x),\qquad \text{homogeneous: } Ty=0\iff y\in\ker T
$$

**Derived From:** notation. Define $D=\dfrac{d}{dx}$ (so $D(y)=y'$, $D^2(y)=y''$) and the identity operator $I(y)=y$. Then $y^{(n)}+a_{n-1}y^{(n-1)}+\cdots+a_0y=g(x)$ can be written as $\left(D^n+a_{n-1}D^{n-1}+\cdots+a_0I\right)y=g(x)$. The source stresses that this is a compact way of writing what was already seen, not a new method.

## Supporting Formulas

- $D$ is not a number or a function but an **operator**: it takes a function and returns another function. $T$ is also a linear operator.
- $\ker(T)$ is the set of all functions $y$ with $T(y)=0$; the general solution of the homogeneous ODE is exactly $\ker T$.
- The solutions form a [vector subspace](../11%20-%20Linear%20Algebra/Subspaces.md) whose dimension equals the order of the ODE; the general solution is a linear combination of the elements of a basis.
- With constant coefficients, $T=p(D)$ where $p$ is the characteristic polynomial (see [Characteristic Equation Method](../12%20-%20Ordinary%20Differential%20Equations/Characteristic%20Equation%20Method.md)).
- Example: $y''-3y'+2y=0$ is $(D^2-3D+2I)y=0$, with $\ker T=\mathrm{span}\{e^{x},e^{2x}\}$ and $y=C_1e^{x}+C_2e^{2x}$.
- Example (from an exam): for $T=(x-1)D-I$, find $y\neq0$ in $\ker T$: $Ty=(x-1)y'-y=0$ is separable, $\dfrac{dy}{y}=\dfrac{dx}{x-1}$, so $|y|=c|x-1|$; choosing $c=1$ gives $y=x-1$.

## Derivation Outline

Solving $y''-3y'+2y=0$ with operators:

1. Identify: linear, homogeneous, constant coefficients, order 2.
2. Write the operator $Ty=(D^2-3D+2I)y=0$ and factor it: $(D^2-3D+2I)=(D-1I)(D-2I)$. Whatever annihilates one factor also annihilates $T$.
3. Solve $(D-1I)y=y'-y=0$ (separable): $y=Ce^{x}$.
4. Solve $(D-2I)y=y'-2y=0$: $y=Ce^{2x}$.
5. Check linear independence of $e^{x}$ and $e^{2x}$ ($C_1e^{x}+C_2e^{2x}=0\Rightarrow C_1=C_2=0$).
6. Conclude $y=C_1e^{x}+C_2e^{2x}$, $\ker T=\mathrm{span}\{e^{x},e^{2x}\}$, dimension $2=n$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Linear ODE](../12%20-%20Ordinary%20Differential%20Equations/Linear%20ODE.md), [Higher-Order ODE Solutions](../12%20-%20Ordinary%20Differential%20Equations/Higher-Order%20ODE%20Solutions.md), [Characteristic Equation Method](../12%20-%20Ordinary%20Differential%20Equations/Characteristic%20Equation%20Method.md), [Linear Independence](../11%20-%20Linear%20Algebra/Linear%20Independence.md), [Subspaces](../11%20-%20Linear%20Algebra/Subspaces.md)
**Full Derivation:** 
