---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The exact output of a [coherent state](Coherent%20States.md) evolved under the full Kerr Hamiltonian for the special interaction time $\chi^{(3)}t=\pi$. The result splits cleanly into an equal-weight superposition of two oppositely-rotated coherent states.

## Starting Point

- Full Kerr Hamiltonian: $\hat H=\tfrac{\hbar\chi^{(3)}}{2}\hat a^\dagger\hat a^\dagger\hat a\hat a=\tfrac{\hbar\chi^{(3)}}{2}(\hat n^2-\hat n)$
- Coherent-state Fock-basis expansion: $|\alpha\rangle=e^{-|\alpha|^2/2}\sum_n\dfrac{\alpha^n}{\sqrt{n!}}|n\rangle$, from [Coherent States](Coherent%20States.md)

## Full Derivation

1. Write the Kerr time-evolution operator:

   $$
   \hat U(t)=e^{-i\hat Ht/\hbar}=\exp\left[-\frac{i\chi^{(3)}t}{2}(\hat n^2-\hat n)\right]
   $$

   which is diagonal in the Fock basis since it is built entirely from the number operator $\hat n$. This is done because $\hat n|n\rangle=n|n\rangle$ makes the exponential trivial to apply term by term once the input state is expanded in Fock states — no operator reordering or approximation is needed, unlike the linearized treatment.

2. Expand the input coherent state $|\alpha\rangle$ in the Fock basis and act with $\hat U(t)$ on each term, so each Fock coefficient picks up a phase:

   $$
   e^{-i\chi^{(3)}t(n^2-n)/2}
   $$

   This step converts the abstract operator evolution into an explicit, evaluable phase attached to each term of the sum — the whole problem now reduces to bookkeeping these phases.

3. Specialize to the interaction time $\chi^{(3)}t=\pi$, so each Fock coefficient acquires the phase:

   $$
   (-i)^{n^2}
   $$

   which takes only two distinct values: $1$ for even $n$ and $-i$ for odd $n$. This particular time is singled out because it is exactly where the $n$-dependent phase collapses onto only two distinct values instead of a continuum, which is what allows the sum to resolve into a clean two-term superposition rather than a hopelessly scrambled state.

4. Rewrite the phase as an algebraic identity that separates it into an $n$-independent piece and a piece that alternates sign with the parity of $n$:

   $$
   (-i)^{n^2}=\frac{1}{\sqrt2}\left(e^{-i\pi/4}+(-1)^ne^{i\pi/4}\right)
   $$

   This rewriting is the key trick: it turns a single sum with an awkward phase into two ordinary coherent-state-like sums, one built from $(-1)^n$ (equivalent to a $\pi$-rotated amplitude) and one without.

5. Substitute into the Fock sum and split it into two pieces, one carrying $(i\alpha)^n$ and the other $(-i\alpha)^n$; each piece, on its own, is exactly the Fock-basis expansion of a coherent state, with amplitude $i\alpha$ in one term and $-i\alpha$ in the other. This step is where the state's structure becomes physically transparent: what began as a single coherent state has split into two, related by a $\pi/2$ phase-space rotation of each other (and hence a $\pi$ rotation of one relative to the other).

6. Collect the two resulting coherent-state sums with their respective overall phases $e^{-i\pi/4}$ and $e^{i\pi/4}$, and normalize by $1/\sqrt2$, giving the final cat state. This final bookkeeping step confirms the state is an equal-weight, coherent (not merely classically mixed) superposition of the two oppositely-rotated coherent states.

## Result

$$
\left|\psi\!\left(t=\pi/\chi^{(3)}\right)\right\rangle = |\text{CAT}\rangle = \frac{1}{\sqrt2}\left(e^{-i\pi/4}|i\alpha\rangle+e^{i\pi/4}|-i\alpha\rangle\right)
$$

## Where It's Used

**Concept:** [Optical Schrodinger Cat States](Optical%20Schrodinger%20Cat%20States.md)

---

## Links

**Related:** [Optical Schrodinger Cat States](Optical%20Schrodinger%20Cat%20States.md), [Kerr-Effect Squeezing](Kerr-Effect%20Squeezing.md), [Coherent States](Coherent%20States.md)
