---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The position-space wavefunction of the [two-mode squeezed vacuum](Two-Mode%20Squeezed%20Vacuum.md), and its infinite-squeezing limit, showing that the state converges onto the continuous-variable [EPR](../10%20-%20Quantum%20Information/EPR%20Argument.md) eigenstate.

## Starting Point

- Two-mode squeezing operator $\hat S_{AB}(r)=\exp[r(\hat a^\dagger\hat b^\dagger-\hat a\hat b)]$ and its position-quadrature Bogoliubov transform, $\hat S_{AB}^\dagger\hat X_A\hat S_{AB}=\cosh r\,\hat X_A+\sinh r\,\hat X_B$ (and the $B$-mode counterpart) — from [Two-Mode Squeezed Vacuum](Two-Mode%20Squeezed%20Vacuum.md)
- $\hat S_{AB}^\dagger(r)=\hat S_{AB}(-r)$
- Two-mode vacuum position wavefunction: $\langle X_A',X_B'|0,0\rangle=\frac{1}{\sqrt\pi}e^{-(X_A'^2+X_B'^2)/4}$

## Full Derivation

1. Act with $\hat X_A\hat X_B$ on $\hat S_{AB}(r)|X_A\rangle_A|X_B\rangle_B$ and insert $\hat S_{AB}^\dagger\hat S_{AB}=\hat I$ next to each position operator, converting it into $\hat S_{AB}(r)$ acting on the *transformed* eigenvalues $(\cosh r\,X_A+\sinh r\,X_B)(\cosh r\,X_B+\sinh r\,X_A)$. This is done because it identifies $\hat S_{AB}(r)|X_A\rangle_A|X_B\rangle_B$ as a simultaneous eigenstate of $\hat X_A,\hat X_B$ with shifted eigenvalues, avoiding having to solve a differential equation directly — squeezing a position eigenstate just relabels which eigenvalue it belongs to.

2. Conclude, up to normalization, $\hat S_{AB}(r)|X_A\rangle_A|X_B\rangle_B=|\cosh r\,X_A+\sinh r\,X_B\rangle_A|\cosh r\,X_B+\sinh r\,X_A\rangle_B$. This step is taken because it turns the abstract operator action into an explicit statement of which position eigenstate the squeezing operator maps the input to, which is exactly what's needed to build the wavefunction next.

3. Write the squeezed vacuum's position wavefunction as $\Psi_r(X_A,X_B)=\langle X_A,X_B|0,0\rangle_r=\langle X_A,X_B|\hat S_{AB}(r)|0\rangle_A|0\rangle_B$, then move $\hat S_{AB}(r)$ off the ket and onto the bra using $\hat S_{AB}^\dagger(r)=\hat S_{AB}(-r)$. This is done so the eigenvalue-shift result from step 2 can be reused directly (with $r\to-r$) instead of re-deriving a second, separate case for the bra side.

4. Substitute the shifted eigenvalues $X_A'=\cosh r\,X_A-\sinh r\,X_B$, $X_B'=\cosh r\,X_B-\sinh r\,X_A$ into the known Gaussian vacuum wavefunction $\langle X_A',X_B'|0,0\rangle=\frac{1}{\sqrt\pi}e^{-(X_A'^2+X_B'^2)/4}$. This converts the abstract wavefunction into an explicit Gaussian in $X_A,X_B$ that can be simplified and taken to a limit.

5. Expand $X_A'^2+X_B'^2$ and collect terms using the double-angle hyperbolic identities $\cosh2r=\cosh^2r+\sinh^2r$ and $\sinh2r=2\cosh r\sinh r$, regrouping the exponent into the sum and difference coordinates $X_A-X_B$ and $X_A+X_B$. This regrouping is done because the physically meaningful EPR observables are exactly the relative position and the center-of-mass-like combination of the two modes, so writing the Gaussian in these coordinates is what reveals the state's EPR structure.

6. Arrive at $\Psi_r(X_A,X_B)=\frac{1}{\sqrt\pi}\exp\left[-\frac14\left(e^{2r}(X_A-X_B)^2+e^{-2r}(X_A+X_B)^2\right)\right]$. This final form is derived because it makes explicit that the relative coordinate $X_A-X_B$ is weighted by a rapidly growing exponential (squeezing it toward zero) while the sum coordinate $X_A+X_B$ is weighted by a rapidly shrinking exponential (letting it spread freely) as $r$ grows.

7. Take the limit $r\to\infty$: the $e^{2r}$ factor forces $X_A-X_B\to0$, collapsing the Gaussian in the relative coordinate to a delta function, while the $e^{-2r}$ factor lets $X_A+X_B$ fluctuate with unbounded variance, giving $\Psi_r(X_A,X_B)\to\delta(X_A-X_B)$. This limit is taken because it is the direct demonstration that the two-mode squeezed vacuum converges exactly onto the (unnormalizable, idealized) continuous-variable EPR eigenstate as the squeezing becomes infinite.

## Result

$$
\Psi_r(X_A,X_B) = \frac{1}{\sqrt\pi}\exp\left[-\frac14\left(e^{2r}(X_A-X_B)^2+e^{-2r}(X_A+X_B)^2\right)\right] \;\xrightarrow[r\to\infty]{}\; \delta(X_A-X_B)
$$

## Where It's Used

**Concept:** [Two-Mode Squeezed Vacuum](Two-Mode%20Squeezed%20Vacuum.md)

---

## Links

**Related:** [Two-Mode Squeezed Vacuum](Two-Mode%20Squeezed%20Vacuum.md), [SPDC Time-Frequency Entanglement](SPDC%20Time-Frequency%20Entanglement.md), [EPR Argument](../10%20-%20Quantum%20Information/EPR%20Argument.md)
