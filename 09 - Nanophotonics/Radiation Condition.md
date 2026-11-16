---
tags:
  - nanophotonics
  - concept
  - technique
---
---
## Core Idea

A physical mode field in an open, multilayer structure must carry no power in from infinity — waves may only *exit* the structure through its two unbounded outer layers, never enter it; this one-directional constraint is what turns the multilayer transfer-matrix relation into a solvable equation for the propagation constant $\beta$.

## Key Equation

$$
A_{N+1}=0,\qquad B_0=0 \quad\Longrightarrow\quad \begin{pmatrix}0\\B_{N+1}\end{pmatrix}=\bar T_{N+1,0}\begin{pmatrix}A_0\\0\end{pmatrix}
$$

**Derived From:** stated directly in the source as a physical boundary condition applied to the two semi-infinite outer layers (index $0$ and $N+1$) of the [Multilayer Waveguide Transfer Matrix](Multilayer%20Waveguide%20Transfer%20Matrix.md) formulation, where $E^o_k=(A_k,B_k)^T$ are the forward/backward field amplitudes in layer $k$.

## Supporting Formulas

- With $A_0=1$ (free normalization), the matrix relation collapses to a single scalar mode equation: $t^{11}_{N+1,0}=0$ — an equation for $\beta$ alone, from which everything else (the $T$ matrices, the modal field profile) can be obtained.
- The condition is applied to whichever amplitude multiplies the field component that would grow, or travel inward, at that boundary. For evanescent outer layers ($\beta>n_kk_0$, real $p_k$) this is equivalent to requiring a bounded (decaying) field; for radiating outer layers (imaginary $p_k$) it is equivalent to requiring an outgoing traveling wave only.
- $t^{11}_{N+1,0}=0$ may have many solutions or none, depending on the structure's parameters — each root is one guided mode.

## Derivation Outline

1. Concatenate the per-layer transfer matrices to relate the field amplitudes in the outermost layers, $(A_{N+1},B_{N+1})^T=\bar T_{N+1,0}(A_0,B_0)^T$.
2. Impose no incoming wave from $x\to+\infty$ ($A_{N+1}=0$) and no incoming wave from $x\to-\infty$ ($B_0=0$).
3. Set $A_0=1$ (free normalization) and read off the scalar mode condition $t^{11}_{N+1,0}=0$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Multilayer Waveguide Transfer Matrix](Multilayer%20Waveguide%20Transfer%20Matrix.md)
**Full Derivation:**
