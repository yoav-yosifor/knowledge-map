---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The Bogoliubov transformation of $\hat a,\hat a^\dagger$ under the squeezing operator, $\hat S^\dagger\hat a\hat S=\cosh r\,\hat a+\sinh r\,\hat a^\dagger$, and the resulting stretching/compression of the quadratures.

## Starting Point

- $\hat S(r)=\exp\bigl[\tfrac12(r^*\hat a^2-r\hat a^{\dagger2})\bigr]$
- $[\hat a^2,\hat a^\dagger]=2\hat a$ (needed to start the nested-commutator series)
- $\hat X=(\hat a+\hat a^\dagger)/\sqrt2$, $\hat P=(\hat a-\hat a^\dagger)/(i\sqrt2)$

## Full Derivation

1. **Set up the BCH conjugation series.**

   $$
   \hat A=\tfrac12\left(r^*\hat a^2-r\hat a^{\dagger2}\right)
   $$

   Write $\hat S^\dagger\hat a\hat S$ as the Baker–Campbell–Hausdorff conjugation series in nested commutators of this operator with $\hat a$. This mirrors exactly the technique used for the displacement and rotation operators — conjugating $\hat a$ and $\hat a^\dagger$ by an exponential always reduces to resumming a nested-commutator series.

2. Use $[\hat a^2,\hat a^\dagger]=2\hat a$ to evaluate the first nested commutator, then iterate; unlike the rotation case, where the commutators alternated sign but stayed proportional to the same single operator, here each new commutator alternates between being proportional to $\hat a$ and to $\hat a^\dagger$, so the series never closes after a finite number of terms and instead runs to all orders. This open-ended alternation between $\hat a$ and $\hat a^\dagger$, rather than the closed single-operator loop seen for a rotation, is exactly why hyperbolic rather than trigonometric functions appear in the result.

3. **Resum the series.**

   $$
   \hat S^\dagger\hat a\hat S=\cosh r\,\hat a+\sinh r\,\hat a^\dagger
   $$

   Recognizing the resulting series as the Taylor expansions of $\cosh r$ and $\sinh r$ multiplying the $\hat a$ and $\hat a^\dagger$ terms respectively gives this. This is the hallmark of a squeezing (Bogoliubov) transformation, distinct from a rotation, precisely because it mixes $\hat a$ and $\hat a^\dagger$ together rather than merely multiplying $\hat a$ by a phase.

4. **Take the Hermitian conjugate.**

   $$
   \hat S^\dagger\hat a^\dagger\hat S=\cosh r\,\hat a^\dagger+\sinh r\,\hat a
   $$

   Since the transformation must be consistent for both $\hat a$ and its adjoint, this second relation follows immediately by conjugating the first.

5. **Transform the quadratures.**

   $$
   \hat S^\dagger\hat X\hat S=e^r\hat X, \qquad \hat S^\dagger\hat P\hat S=e^{-r}\hat P
   $$

   Substituting both into $\hat X=(\hat a+\hat a^\dagger)/\sqrt2$ and $\hat P=(\hat a-\hat a^\dagger)/(i\sqrt2)$, the cross terms in $\hat a,\hat a^\dagger$ cancel within each combination, using $\cosh r+\sinh r=e^r$ and $\cosh r-\sinh r=e^{-r}$. This is where the abstract operator transformation becomes a physically transparent statement: one real quadrature is simply rescaled by $e^r$, the other by $e^{-r}$, with no leftover mixing between them.

## Result

$$
\hat S^\dagger(r)\,\hat a\,\hat S(r) = \cosh r\,\hat a + \sinh r\,\hat a^\dagger, \qquad \hat S^\dagger\hat X\hat S=e^r\hat X,\ \ \hat S^\dagger\hat P\hat S=e^{-r}\hat P
$$

## Where It's Used

**Concept:** [Squeezed States](Squeezed%20States.md)

---

## Links

**Related:** [Squeezed States](Squeezed%20States.md), [Baker-Campbell-Hausdorff Formula](../06%20-%20Quantum%20Mechanics%201/Baker-Campbell-Hausdorff%20Formula.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md)
