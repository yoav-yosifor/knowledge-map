---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The field amplitudes of a DBR unit cell are related by a $2\times2$ transfer matrix $M_{TE}$ (TE polarization); $N$ cells give $M_{TE}^N$, from which the reflection and transmission coefficients follow.

## Starting Point

- Unit cell of two layers ($n_1,d_1$; $n_2,d_2$). $E_n^\pm$ are the right/left-propagating fields at the entrance to cell $n$; $\bar E_n^\pm$ are defined immediately after the interface, in medium $n_1$.
- TE polarization (electric field orthogonal to the slide's plane): the boundary conditions are continuity of $E$ and of its derivative.
- By Snell's law $k_y$ is identical in both layers.

$$
k_{1z}=\sqrt{k_0^2n_1^2-k_y^2},\qquad k_{2z}=\sqrt{k_0^2n_2^2-k_y^2}
$$

## Full Derivation

1. **Write the field on both sides of the interface at $z=0$.**

   $$
   E(z<0)=E_n^+e^{-ik_{2z}z-ik_yy}+E_n^-e^{ik_{2z}z-ik_yy},\qquad E(z>0)=\bar E_n^+e^{-ik_{1z}z-ik_yy}+\bar E_n^-e^{ik_{1z}z-ik_yy}
   $$

   Each side is a sum of a right- and left-going wave with the $z$-wavenumber of that layer.

2. **Apply the boundary conditions.**

   $$
   E_n^++E_n^-=\bar E_n^++\bar E_n^-,\qquad k_{2z}\left(E_n^+-E_n^-\right)=k_{1z}\left(\bar E_n^+-\bar E_n^-\right)
   $$

   Continuity of $E$ gives the first; continuity of its $z$-derivative gives the second (the $e^{-ik_yy}$ factor is common because of Snell's law).

3. **Write the interface relation as a matrix.**

   $$
   \begin{pmatrix}\bar E_n^+\\ \bar E_n^-\end{pmatrix}=\frac12\begin{bmatrix}1+k_{2z}/k_{1z}&1-k_{2z}/k_{1z}\\1-k_{2z}/k_{1z}&1+k_{2z}/k_{1z}\end{bmatrix}\begin{pmatrix}E_n^+\\E_n^-\end{pmatrix}=M_{2\to1}\begin{pmatrix}E_n^+\\E_n^-\end{pmatrix}
   $$

   Solving the two equations of step 2 for $\bar E_n^\pm$ gives this matrix.

4. **Write the other interface and the propagation matrices.**

   $$
   M_{1\to2}=\frac12\begin{bmatrix}1+k_{1z}/k_{2z}&1-k_{1z}/k_{2z}\\1-k_{1z}/k_{2z}&1+k_{1z}/k_{2z}\end{bmatrix},\quad M_{d_1}=\begin{bmatrix}e^{-ik_{1z}d_1}&0\\0&e^{ik_{1z}d_1}\end{bmatrix},\quad M_{d_2}=\begin{bmatrix}e^{-ik_{2z}d_2}&0\\0&e^{ik_{2z}d_2}\end{bmatrix}
   $$

   The interface matrices carry the impedance mismatch; the diagonal matrices carry the phase accumulated across each layer.

5. **Chain them across one unit cell.**

   $$
   \begin{pmatrix}E_{n+1}^+\\E_{n+1}^-\end{pmatrix}=M_{d_2}M_{1\to2}M_{d_1}M_{2\to1}\begin{pmatrix}E_n^+\\E_n^-\end{pmatrix}=M_{TE}\begin{pmatrix}E_n^+\\E_n^-\end{pmatrix}
   $$

   Matrices act right to left in the order the wave meets them: interface $2\to1$, layer $d_1$, interface $1\to2$, layer $d_2$.

6. **Unit-cell matrix elements (as given in the lecture — product expansion not shown on the slide, to be filled in by hand).**

   $$
   M_{TE}^{11}=e^{-ik_{2z}d_2}\left[\cos(k_{1z}d_1)-\frac i2\left(\frac{k_{2z}}{k_{1z}}+\frac{k_{1z}}{k_{2z}}\right)\sin(k_{1z}d_1)\right],\qquad M_{TE}^{22}=\left(M_{TE}^{11}\right)^*
   $$

   $$
   M_{TE}^{12}=-\frac i2e^{-ik_{2z}d_2}\left(\frac{k_{1z}}{k_{2z}}-\frac{k_{2z}}{k_{1z}}\right)\sin(k_{1z}d_1),\qquad M_{TE}^{21}=\left(M_{TE}^{12}\right)^*
   $$

7. **Stack $N$ cells and extract $r$ and $t$.**

   $$
   \begin{pmatrix}E_N^+\\E_N^-\end{pmatrix}=M_{TE}^N\begin{pmatrix}E_0^+\\E_0^-\end{pmatrix},\qquad \begin{pmatrix}E_t\\0\end{pmatrix}=\mathbf M\begin{pmatrix}E_{in}\\E_r\end{pmatrix}
   $$

   With $\mathbf M=M_{TE}^N$ and no incoming wave from the far side (the lower component is zero), the second row gives $r$ and the first gives $t$.

## Result

$$
r=\frac{E_r}{E_{in}}=-\frac{\mathbf M^{21}}{\mathbf M^{22}},\qquad t=\frac{E_t}{E_{in}}=\mathbf M^{11}-\frac{\mathbf M^{12}\mathbf M^{21}}{\mathbf M^{22}}
$$

## Where It's Used

**Concept:** [Distributed Bragg Reflector](Distributed%20Bragg%20Reflector.md)

---

## Links

**Related:** [Multilayer Transfer Matrix Derivation](Multilayer%20Transfer%20Matrix%20Derivation.md), [Bloch Theorem](Bloch%20Theorem.md)
