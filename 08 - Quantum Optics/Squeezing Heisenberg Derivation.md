---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

This derives the Bogoliubov transformation produced by a [parametric-squeezing Hamiltonian](Optical%20Parametric%20Amplifier.md), solved directly from the Heisenberg equations of motion rather than by [BCH operator conjugation](Squeezing%20Operator%20Derivation.md). It covers the general case with detuning included, and identifies the condition under which the dynamics produces genuine, unbounded exponential amplification.

## Starting Point

- Pure squeezing Hamiltonian $\hat H=\hbar\kappa^*\hat a^2+\hbar\kappa\hat a^{\dagger2}$, the quantized degenerate parametric-amplification interaction from [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md)
- Heisenberg equation of motion $\dot{\hat O}=\tfrac{1}{i\hbar}[\hat O,\hat H]$
- Commutator $[\hat a,\hat a^{\dagger2}]=2\hat a^\dagger$
- Quadratures $\hat X=\tfrac{1}{\sqrt2}(\hat a+\hat a^\dagger)$, $\hat Y=\tfrac{1}{i\sqrt2}(\hat a-\hat a^\dagger)$

## Full Derivation

1. **Pure squeezing.**

   $$
   \dot{\hat a}=-2i\kappa\hat a^\dagger, \qquad \dot{\hat a}^\dagger=2i\kappa^*\hat a
   $$

   Computing the Heisenberg equations of motion for $\hat a,\hat a^\dagger$ under $\hat H$ gives these. This is done because the Heisenberg picture turns the abstract operator-algebra problem (as solved via BCH elsewhere) into an ordinary pair of coupled linear differential equations, which can be solved by standard means.

2. **Decouple the equations.**

   $$
   \ddot{\hat a}=4|\kappa|^2\hat a
   $$

   Differentiating again to decouple the pair gives this equation; the general solution is a combination of $\cosh$ and $\sinh$ of $2|\kappa|t$, with the two integration constants fixed using the initial conditions $\hat a(0)=\hat A$ and $\hat a^\dagger(0)$. This step is taken because a linear second-order equation with constant (real, positive) coefficients has an exponential — here hyperbolic — general solution, unlike the oscillatory solution a harmonic (rotation) Hamiltonian would give; the difference in sign is exactly the SU(2)-versus-SU(1,1) distinction.

3. **Identify the Bogoliubov transformation.**

   $$
   \hat a(t)=\cosh r\,\hat a(0)-e^{2i\theta}\sinh(r)\,\hat a^\dagger(0), \qquad r=2|\kappa|t
   $$

   This is the resulting solution. Writing the general form $\hat a(t)=\mu\hat a(0)-\nu\hat a^\dagger(0)$, it satisfies

   $$
   |\mu|^2-|\nu|^2=1
   $$

   This constraint is highlighted because it is the operator analogue of unitarity — it guarantees the transformed operator still satisfies the canonical commutation relation, exactly as $|t|^2+|r|^2=1$ does for a beamsplitter.

4. **Squeezing with detuning.**

   $$
   \hat H=\hbar\Delta\hat a^\dagger\hat a+\hbar\kappa^*\hat a^2+\hbar\kappa\hat a^{\dagger2}
   $$

   Adding a rotation (phase-mismatch) term to the Hamiltonian and rewriting the resulting equations of motion in terms of the quadratures $\hat X,\hat Y$, they decouple into

   $$
   \dot{\hat X}=(\Delta-2\kappa)\hat Y, \qquad \dot{\hat Y}=-(\Delta+2\kappa)\hat X
   $$

   Working in the quadrature basis is done because detuning (a rotation generator) and squeezing (a boost generator) act very differently on $\hat X,\hat Y$, and only in this basis does the resulting second-order equation decouple cleanly.

5. **Solve the decoupled equation.**

   $$
   \ddot{\hat X}=\left(4|\kappa|^2-\Delta^2\right)\hat X
   $$

   Solving this and converting back to $\hat a,\hat a^\dagger$ gives the general detuned Bogoliubov transformation, with effective rate $\Omega\equiv\sqrt{4|\kappa|^2-\Delta^2}\,t=\sqrt{r^2-(\Delta t)^2}$. This generalizes the pure-squeezing result to the realistic case where perfect phase matching is not achieved, showing detuning competes directly against squeezing in the exponent.

6. **Effective squeezing parameter.**

   $$
   \tilde r=\sinh^{-1}(|\nu|)
   $$

   Reading off the Bogoliubov coefficients $\mu,\nu$ from the detuned solution, verify $|\mu|^2-|\nu|^2=1$ holds generically (confirming this is a universal feature of any Hamiltonian quadratic in $\hat a,\hat a^\dagger$, not a special property of the undetuned case), and define the effective squeezing parameter above. This step is included to give a single physically meaningful number — the *net* squeezing actually achieved — that folds detuning's degrading effect into one parameter comparable directly to the ideal, phase-matched case.

7. **Phase matching is required for true amplification.**

   $$
   \hat X_{\pi/4}(t)=\frac{1}{\sqrt2}\left(\hat X(0)+\hat Y(0)\right)e^{r}, \qquad \hat Y_{\pi/4}(t)=\frac{1}{\sqrt2}\left(\hat X(0)-\hat Y(0)\right)e^{-r}
   $$

   Setting $\Delta=0$ in the general solution and rewriting $\hat X(t),\hat Y(t)$ in terms of the $\pi/4$-rotated quadratures diagonalizes the dynamics into pure exponentials, as above. This final step confirms explicitly that only with perfect phase matching does the dynamics produce clean, unbounded exponential growth in one quadrature and decay in the other — any residual detuning instead mixes the growth into an oscillatory-hyperbolic combination that never cleanly amplifies.

## Result

$$
\hat a(t) = \left[\cosh\Omega-i\frac{\Delta t}{\Omega}\sinh\Omega\right]\hat a(0) - \left[e^{2i\theta}\frac{r}{\Omega}\sinh\Omega\right]\hat a^\dagger(0), \qquad \Omega=\sqrt{r^2-(\Delta t)^2}
$$

## Where It's Used

**Concept:** [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md)

---

## Links

**Related:** [SU(2) and SU(1,1) Dynamics](SU(2)%20and%20SU(1,1)%20Dynamics.md), [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md), [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md)
