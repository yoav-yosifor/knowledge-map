---
tags:
  - ordinary-differential-equations
  - concept
  - technique
---
---
## Core Idea

An exact ODE is one whose left-hand side is the total differential of some function $F(x,y)$, so its solution is simply the implicit equation $F(x,y)=C$.

## Key Equation

$$
p(x,y)\,dx+q(x,y)\,dy=0,\quad p=F_x,\ q=F_y\qquad\text{exact}\iff p_y=q_x
$$

**Derived From:** start from $F(x,y)=C$ and differentiate once, treating $y$ as a function of $x$ (chain rule): $\dfrac{dF}{dx}=F_x+F_y\dfrac{dy}{dx}=0$. Multiplying by $dx$ gives $F_x\,dx+F_y\,dy=0$, which is the template of an exact ODE. The condition $p_y=q_x$ is the statement that the mixed second derivatives of $F$ are equal, $F_{xy}=F_{yx}$.

## Supporting Formulas

- Notation: $F_x=\dfrac{\partial F}{\partial x}$ is a partial derivative (the other variable is held fixed), distinct from the ordinary derivative $\dfrac{dF}{dx}$; $F_{xy}=\dfrac{\partial^2F}{\partial x\,\partial y}$ is a mixed derivative. The source notes that mixed derivatives are not always equal, so the equality $p_y=q_x$ must be checked.
- $$ F(x,y)=\int p(x,y)\,dx+c(y) \quad\text{or}\quad F(x,y)=\int q(x,y)\,dy+c(x) $$ — two ways to build $F$; choose whichever integral is easier.
- The solution of an exact ODE is given implicitly by $F(x,y)=C$.
- Example: $2xyy'=3x^2-y^2$ with $y(1)=-1$ becomes $-(3x^2-y^2)\,dx+2xy\,dy=0$, with $p_y=2y=q_x$. Then $F=xy^2+c(x)$, $c'(x)=-3x^2$, so $F=xy^2-x^3=C$. Solving for $y$ gives $y=\pm\sqrt{\dfrac{C+x^3}{x}}$; $y(1)=-1$ picks the negative root and gives $C=0$, so $y=-x$.
- Example: $\dfrac{2xy+1}{y}\,dx+\dfrac{2-x}{y^2}\,dy=0$ has $p_y=\dfrac{1}{y^2}=q_x$. Then $F=x^2+\dfrac{x}{y}+c(y)$, $c'(y)=\dfrac{2}{y^2}$, so $F=x^2+\dfrac{x}{y}-\dfrac{2}{y}=C$, which gives $y=\dfrac{2-x}{x^2+C}$.

## Derivation Outline

1. Write the ODE as $p\,dx+q\,dy=0$ and check $p_y=q_x$. If it fails, the ODE is not exact (the source says other methods come in later tutorials).
2. Build $F$ by integrating $p$ with respect to $x$ (adding $c(y)$) or $q$ with respect to $y$ (adding $c(x)$).
3. Differentiate $F$ with respect to the other variable.
4. Compare with the other coefficient ($q$ or $p$) to find $c'(y)$ or $c'(x)$.
5. Integrate to get $c$, and write the solution $F(x,y)=C$.
6. Solve for $y$ if possible, and use an initial condition to find $C$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Ordinary Differential Equation](../12%20-%20Ordinary%20Differential%20Equations/Ordinary%20Differential%20Equation.md), [General and Particular Solutions](../12%20-%20Ordinary%20Differential%20Equations/General%20and%20Particular%20Solutions.md), [Initial Value Problem](../12%20-%20Ordinary%20Differential%20Equations/Initial%20Value%20Problem.md), [Separation of Variables](../12%20-%20Ordinary%20Differential%20Equations/Separation%20of%20Variables.md)
**Full Derivation:** 
