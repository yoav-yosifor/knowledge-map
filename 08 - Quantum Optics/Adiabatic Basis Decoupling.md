---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

That, under the [adiabatic approximation](Adiabatic%20Approximation.md), a system's equations of motion are written in its instantaneous (adiabatic) eigenbasis. Normally this produces a fully coupled set of differential equations, all tangled together. This derivation shows they instead collapse into completely independent, exactly solvable equations — one per dressed state.

## Starting Point

- Instantaneous eigenvalue equation: $H(t)|k(t)\rangle = E_k(t)|k(t)\rangle$, defining the adiabatic basis at every instant
- State expansion: $|\psi(t)\rangle = \sum_k c_k(t)|k(t)\rangle$
- Schrödinger equation: $i\hbar\,\partial_t|\psi\rangle = H(t)|\psi\rangle$

## Full Derivation

1. Substitute the adiabatic-basis expansion into the Schrödinger equation and use the product rule on each term, since both the amplitudes $c_k(t)$ and the basis states $|k(t)\rangle$ themselves now depend on time:

   $$
   i\hbar\sum_k(\dot c_k|k\rangle + c_k|\dot k\rangle) = \sum_k c_k E_k|k\rangle
   $$

   This step is necessary because in a moving (time-dependent) basis, differentiating the state produces an extra term from the basis vectors changing, unlike in the fixed-basis case.

2. Project the equation onto a bra $\langle k'|$ and invoke exact orthogonality, $\langle k'|k\rangle=\delta_{k'k}$ — guaranteed by the spectral theorem because $H(t)$ is Hermitian at every fixed instant, so its eigenvectors for different eigenvalues are always perfectly orthogonal, no matter how fast $H$ is changing. This isolates a single amplitude $c_{k'}$ on the left and reduces the sum on the right, giving:

   $$
   i\hbar\,\dot c_{k'} = E_{k'}c_{k'} - i\hbar\sum_k c_k\langle k'|\dot k\rangle
   $$

   This step is done because projecting onto one basis state at a time is what turns a single vector equation into a set of scalar equations, one per dressed state, each still coupled to all the others through the last term.

3. Evaluate the diagonal case ($k=k'$) of the coupling term by differentiating the normalization condition $\langle k|k\rangle=1$: this shows $\langle k|\dot k\rangle$ is purely imaginary, i.e. it can only contribute an unobservable global phase, never a change in population. By absorbing that phase into the definition of $c_k$ (a standard gauge choice), $\langle k|\dot k\rangle$ is set to exactly zero:

   $$
   \langle k|\dot k\rangle = 0
   $$

   This step is done because a quantum state's total probability can never spontaneously grow or shrink — the "velocity" of a normalized state can never point back into itself — so this term cannot represent any real physical transition and can be gauged away.

4. Isolate the true off-diagonal coupling ($k\neq k'$) and evaluate it exactly by differentiating the eigenvalue equation $H|k'\rangle=E_{k'}|k'\rangle$ with respect to time and projecting onto $\langle k|$, giving:

   $$
   \langle k|\dot k'\rangle = \frac{\langle k|\dot H|k'\rangle}{E_{k'}-E_k}
   $$

   This step is done to make explicit that this term — and only this term — is the genuine physical engine of transitions between dressed states, proportional to how fast the Hamiltonian itself is changing (i.e. to $\dot\Omega$, the rate the driving fields are varied).

5. Invoke the adiabatic limit: if the driving changes slowly enough that $\dot H\to0$, then $\langle k|\dot k'\rangle\to0$ for every pair $k\neq k'$ — this is the approximation itself, formally set to zero rather than derived to be exactly zero. This step is done because it is precisely the assumption "slow enough" is translating into: negligible non-adiabatic coupling between distinct dressed states.

6. Substitute the vanishing diagonal and off-diagonal couplings back into the amplitude equation from step 2. Every cross term drops out, leaving:

   $$
   i\hbar\,\dot c_{k'} = E_{k'}(t)c_{k'}
   $$

   for each $k'$ independently. This final step is done because it shows, in matrix language, that the evolution generator has become purely diagonal — each dressed state now evolves completely on its own, accumulating only a dynamical phase, with no leakage into any other dressed state.

## Result

$$
i\hbar\,\dot{c}_{k'} = E_{k'}(t)\,c_{k'} \quad\Longrightarrow\quad c_{k'}(t) = c_{k'}(0)\,\exp\!\left(-\frac{i}{\hbar}\int_0^t E_{k'}(t')\,dt'\right)
$$

## Where It's Used

**Concept:** [Adiabatic Approximation](Adiabatic%20Approximation.md)

---

## Links

**Related:** [Dark State](Dark%20State.md), [STIRAP](STIRAP.md), [Adiabatic Approximation](Adiabatic%20Approximation.md)
