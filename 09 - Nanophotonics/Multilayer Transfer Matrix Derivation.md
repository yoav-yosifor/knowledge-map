---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The $2\times2$ transfer matrix $\bar T$ that relates the field amplitudes in one layer of a [multilayer dielectric stack](Multilayer%20Waveguide%20Transfer%20Matrix.md) to the amplitudes in the next, from the boundary conditions at the interface between them — and, by concatenating across all layers and applying the [Radiation Condition](Radiation%20Condition.md), the scalar mode equation whose roots are the allowed propagation constants $\beta$.

## Starting Point

- Per-layer field ansatz: $E_y^{(k)}(x)=A_ke^{p_kx}+B_ke^{-p_kx}$, with $p_k$ the (possibly imaginary) decay/oscillation constant of layer $k$.
- Boundary conditions at the interface $x=d_k$ between layer $k$ and layer $k+1$: continuity of the field and of $\alpha\cdot(\text{its derivative})$, where $\alpha_k=1/\mu_k$ for TE or $1/\varepsilon_k$ for TM:
  $$
  E_y(x=d_k^-)=E_y(x=d_k^+), \qquad \alpha_k\,\partial_xE_y(x=d_k^-)=\alpha_{k+1}\,\partial_xE_y(x=d_k^+)
  $$

## Full Derivation

1. **Substitute the field ansatz into both boundary conditions at $x=d_k$.**

   $$
   A_ke^{p_kd_k}+B_ke^{-p_kd_k} = A_{k+1}e^{p_{k+1}d_k}+B_{k+1}e^{-p_{k+1}d_k}
   $$

   $$
   \alpha_kp_k\!\left(A_ke^{p_kd_k}-B_ke^{-p_kd_k}\right) = \alpha_{k+1}p_{k+1}\!\left(A_{k+1}e^{p_{k+1}d_k}-B_{k+1}e^{-p_{k+1}d_k}\right)
   $$

   This is two linear equations in the two unknowns $A_{k+1},B_{k+1}$ — everything about layer $k$ is already fixed.

2. **Divide the second equation by $\alpha_{k+1}p_{k+1}$ and name the resulting ratio.**

   $$
   r_{k+1,k}=1+\frac{p_k\alpha_k}{p_{k+1}\alpha_{k+1}}, \qquad s_{k+1,k}=1-\frac{p_k\alpha_k}{p_{k+1}\alpha_{k+1}}
   $$

   This ratio $\alpha_kp_k/(\alpha_{k+1}p_{k+1})$ is the layer-to-layer impedance mismatch — it's what makes an interface partially reflective; if the two layers were identical it would equal $1$, giving $r_{k+1,k}=2$, $s_{k+1,k}=0$.

3. **Add and subtract the two boundary-condition equations to isolate $A_{k+1}$ and $B_{k+1}$ separately.**

   $$
   A_{k+1}=\tfrac12\left[e^{(p_k-p_{k+1})d_k}r_{k+1,k}\,A_k+e^{-(p_k+p_{k+1})d_k}s_{k+1,k}\,B_k\right]
   $$

   $$
   B_{k+1}=\tfrac12\left[e^{(p_k+p_{k+1})d_k}s_{k+1,k}\,A_k+e^{-(p_k-p_{k+1})d_k}r_{k+1,k}\,B_k\right]
   $$

   Adding the two boundary-condition equations cancels the $B_{k+1}$ term (leaving $A_{k+1}$); subtracting cancels the $A_{k+1}$ term (leaving $B_{k+1}$) — standard elimination for a $2\times2$ linear system.

4. **Name the two recurring exponentials and assemble the matrix.**

   $$
   a_{k+1,k}=e^{(p_k-p_{k+1})d_k}, \qquad b_{k+1,k}=e^{(p_k+p_{k+1})d_k}
   $$

   $$
   \begin{pmatrix}A_{k+1}\\B_{k+1}\end{pmatrix}=\frac12\begin{pmatrix}a_{k+1,k}r_{k+1,k} & b_{k+1,k}^{-1}s_{k+1,k}\\ b_{k+1,k}s_{k+1,k} & a_{k+1,k}^{-1}r_{k+1,k}\end{pmatrix}\begin{pmatrix}A_k\\B_k\end{pmatrix}
   $$

   $a_{k+1,k},b_{k+1,k}$ carry the propagation phase/decay accumulated across the interface position $d_k$; $r_{k+1,k},s_{k+1,k}$ carry the impedance mismatch between the two layers. Together they define $\bar T\equiv\bar T_{k+1,k}$, so $E^o_{k+1}=\bar T_{k+1,k}\cdot E^o_k$ with $E^o_k=(A_k,B_k)^T$.

5. **Concatenate across all $N$ layers.**

   $$
   E^o_{N+1}=\bar T_{N+1,N}\cdot\bar T_{N,N-1}\cdots\bar T_{1,0}\cdot E^o_0 \equiv \bar T_{N+1,0}\cdot E^o_0
   $$

   One matrix multiplication per interface walks the field from the bottom semi-infinite layer to the top one:

   $$
   \begin{pmatrix}A_{N+1}\\B_{N+1}\end{pmatrix}=\begin{pmatrix}t^{11}_{N+1,0}&t^{12}_{N+1,0}\\t^{21}_{N+1,0}&t^{22}_{N+1,0}\end{pmatrix}\begin{pmatrix}A_0\\B_0\end{pmatrix}
   $$

   $\beta$ (and every $p_k$, since $p_k$ depends on $\beta$) is still unknown at this point — the entries of $\bar T_{N+1,0}$ are only *functions* of $\beta$, not numbers yet.

6. **Apply the radiation condition to fix $\beta$.**

   The [Radiation Condition](Radiation%20Condition.md) — no wave enters the structure from either semi-infinite outer layer — sets $A_{N+1}=0$ (nothing incoming from $x\to+\infty$) and $B_0=0$ (nothing incoming from $x\to-\infty$). Substituting into the top row of step 5's matrix equation:

   $$
   0 = t^{11}_{N+1,0}\,A_0 + t^{12}_{N+1,0}\cdot 0 = t^{11}_{N+1,0}\,A_0
   $$

   Since the overall mode amplitude is only defined up to a free scale, set $A_0=1$:

   $$
   t^{11}_{N+1,0}(\beta)=0
   $$

   This scalar equation is the multilayer stack's mode condition — its roots are the discrete allowed values of $\beta$. Once a root is found, every $p_k$, every $\bar T_{k+1,k}$, and the full field profile follow directly.

## Result

$$
\bar T_{k+1,k} = \frac12\begin{pmatrix}a_{k+1,k}r_{k+1,k} & b_{k+1,k}^{-1}s_{k+1,k}\\ b_{k+1,k}s_{k+1,k} & a_{k+1,k}^{-1}r_{k+1,k}\end{pmatrix}, \qquad
\begin{aligned}
a_{k+1,k}&=e^{(p_k-p_{k+1})d_k}, & b_{k+1,k}&=e^{(p_k+p_{k+1})d_k}\\
r_{k+1,k}&=1+\frac{p_k\alpha_k}{p_{k+1}\alpha_{k+1}}, & s_{k+1,k}&=1-\frac{p_k\alpha_k}{p_{k+1}\alpha_{k+1}}
\end{aligned}
$$

$$
t^{11}_{N+1,0}(\beta)=0 \qquad\text{(mode condition, from } \bar T_{N+1,0}=\bar T_{N+1,N}\cdots\bar T_{1,0}\text{)}
$$

## Where It's Used

**Concept:** [Multilayer Waveguide Transfer Matrix](Multilayer%20Waveguide%20Transfer%20Matrix.md)

---

## Links

**Related:** [Radiation Condition](Radiation%20Condition.md) (closes the eigenvalue problem once the matrices are concatenated)
