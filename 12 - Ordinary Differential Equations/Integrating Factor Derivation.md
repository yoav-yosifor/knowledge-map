---
tags:
  - ordinary-differential-equations
  - derivation
---
---
## Statement of Result

If $P\,dx+Q\,dy=0$ is not exact, multiplying by $\mu(x)=e^{\int\frac{P_y-Q_x}{Q}dx}$ (or by $\mu(y)=e^{\int\frac{Q_x-P_y}{P}dy}$) makes it exact, provided the exponent's integrand depends on only that one variable.

## Starting Point

- $P_y(x,y)\neq Q_x(x,y)$, so the ODE is not exact.
- An ODE $p\,dx+q\,dy=0$ is [exact](../12%20-%20Ordinary%20Differential%20Equations/Exact%20ODE.md) when $p_y=q_x$.
- Product rule for derivatives.

## Full Derivation

1. **Require that the multiplied ODE be exact.** We look for a function $\mu$ such that

   $$
   \mu\cdot\left[P\,dx+Q\,dy\right]=0
   $$

   is exact, i.e. $(\mu P)_y=(\mu Q)_x$. We want this because an exact ODE can be solved by the method of [exact ODEs](../12%20-%20Ordinary%20Differential%20Equations/Exact%20ODE.md); $\mu$ can depend on $x$ or on $y$.

2. **Apply the product rule to both sides.**

   $$
   \mu_y\,P+P_y\,\mu=\mu_x\,Q+Q_x\,\mu
   $$

   Differentiating $(\mu P)_y$ and $(\mu Q)_x$ with the product rule gives this condition on $\mu$.

3. **Rearrange.**

   $$
   \mu\left[P_y-Q_x\right]=\mu_x\,Q-\mu_y\,P
   $$

   Collecting the terms containing $\mu$ itself on the left and the terms with derivatives of $\mu$ on the right.

4. **Assume $\mu$ depends on $x$ only.** Then $\mu_y=0$ and

   $$
   \mu\left[P_y-Q_x\right]=\mu_x\,Q\quad\Longrightarrow\quad \frac{1}{Q}\left[P_y-Q_x\right]=\frac{\mu_x}{\mu}
   $$

   Setting $\mu_y=0$ removes the $P$ term, leaving an equation we can separate. For this to make sense, the left-hand side must depend on $x$ only.

5. **Separate variables and integrate.**

   $$
   \ln|\mu|=\int\frac{1}{Q}\left[P_y-Q_x\right]dx
   $$

   Writing $\dfrac{\mu_x}{\mu}\,dx=\dfrac{d\mu}{\mu}$ is the algebraic step of separating variables; integrating both sides gives the logarithm of $\mu$.

6. **Exponentiate.**

   $$
   \mu(x)=e^{\int\frac{1}{Q}\left[P_y-Q_x\right]dx}
   $$

   Applying the inverse of the logarithm gives $\mu(x)$.

7. **Repeat for $\mu$ depending on $y$ only.** Performing the same steps with $\mu_x=0$ gives

   $$
   \mu(y)=e^{\int\frac{1}{P}\left[Q_x-P_y\right]dy}
   $$

   The same procedure with the roles of $x$ and $y$ swapped.

## Result

$$
\mu(x)=e^{\int\frac{P_y-Q_x}{Q}\,dx}\qquad\Big|\qquad \mu(y)=e^{\int\frac{Q_x-P_y}{P}\,dy}
$$

## Where It's Used

**Concept:** [Integrating Factor](../12%20-%20Ordinary%20Differential%20Equations/Integrating%20Factor.md)

---

## Links

**Related:** [Exact ODE](../12%20-%20Ordinary%20Differential%20Equations/Exact%20ODE.md)
