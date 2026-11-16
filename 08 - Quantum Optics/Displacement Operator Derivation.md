---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

That $\hat D(\alpha)|0\rangle=|\alpha\rangle$ — the [displacement operator](Displacement%20Operator.md) generates a [coherent state](Coherent%20States.md) from the vacuum — and that $\hat D^\dagger(\alpha)\hat a\hat D(\alpha)=\hat a+\alpha$.

## Starting Point

- $\hat D(\alpha)=e^{\alpha\hat a^\dagger-\alpha^*\hat a}$
- The Baker–Campbell–Hausdorff truncation $e^{\hat A+\hat B}=e^{\hat A}e^{\hat B}e^{-\frac12[\hat A,\hat B]}$, valid whenever $[\hat A,[\hat A,\hat B]]=[\hat B,[\hat A,\hat B]]=0$ — see [Baker-Campbell-Hausdorff Formula](../06%20-%20Quantum%20Mechanics%201/Baker-Campbell-Hausdorff%20Formula.md)
- $[\hat a,\hat a^\dagger]=1$

## Full Derivation

1. Set $\hat A=\alpha\hat a^\dagger$, $\hat B=-\alpha^*\hat a$; compute the commutator:

   $$
   [\hat A,\hat B]=-|\alpha|^2[\hat a^\dagger,\hat a]=|\alpha|^2
   $$

   a plain c-number, so every higher nested commutator vanishes and the BCH truncation applies exactly. This is the key simplification: because the commutator is just a number rather than an operator, the usually-infinite BCH series collapses to a single multiplicative correction factor.

2. Apply the truncation:

   $$
   e^{\alpha\hat a^\dagger-\alpha^*\hat a}|0\rangle = e^{-|\alpha|^2/2}\,e^{\alpha\hat a^\dagger}\,e^{-\alpha^*\hat a}|0\rangle
   $$

   Splitting the exponential into separately-ordered pieces is only valid because of the c-number commutator found in step 1, and the ordering is chosen so the annihilation part acts on the vacuum first.

3. Note:

   $$
   e^{-\alpha^*\hat a}|0\rangle=|0\rangle
   $$

   since every term in the expansion beyond the identity contains a positive power of $\hat a$ acting directly on the vacuum. The vacuum is annihilated by $\hat a$, so any function of $\hat a$ applied to $|0\rangle$ collapses to just its leading (constant) term.

4. Expand, using $|n\rangle=(\hat a^\dagger)^n|0\rangle/\sqrt{n!}$:

   $$
   e^{\alpha\hat a^\dagger}|0\rangle=\sum_n\frac{\alpha^n}{n!}(\hat a^\dagger)^n|0\rangle=\sum_n\frac{\alpha^n}{\sqrt{n!}}|n\rangle
   $$

   Repeated application of the creation operator builds up number states one photon at a time — exactly how Fock states are constructed from the vacuum.

5. Combine with the prefactor $e^{-|\alpha|^2/2}$ to get:

   $$
   |\alpha\rangle=e^{-|\alpha|^2/2}\sum_n\frac{\alpha^n}{\sqrt{n!}}|n\rangle
   $$

   matching the coherent-state Fock expansion found independently from $\hat a|\alpha\rangle=\alpha|\alpha\rangle$. The match between these two independently-derived expressions confirms that the conjectured exponential operator really does produce the coherent state, closing the loop between the two definitions.

6. Separately, transform $\hat a$ itself:

   $$
   \hat D^\dagger(\alpha)\hat a\hat D(\alpha)=e^{\alpha^*\hat a-\alpha\hat a^\dagger}\,\hat a\,e^{\alpha\hat a^\dagger-\alpha^*\hat a}
   $$

   expanded as a BCH conjugation series in nested commutators with $\hat a$; since

   $$
   [\alpha\hat a^\dagger-\alpha^*\hat a,\hat a]=\alpha
   $$

   is again a c-number, the series terminates after the first term. This second calculation exposes the operator meaning of "displacement" directly: it doesn't just move the vacuum, it shifts the annihilation operator itself by a constant, so the same shift applies no matter what state it acts on.

## Result

$$
\hat D(\alpha)|0\rangle = |\alpha\rangle, \qquad \hat D^\dagger(\alpha)\,\hat a\,\hat D(\alpha) = \hat a+\alpha
$$

## Where It's Used

**Concept:** [Displacement Operator](Displacement%20Operator.md)

---

## Links

**Related:** [Displacement Operator](Displacement%20Operator.md), [Baker-Campbell-Hausdorff Formula](../06%20-%20Quantum%20Mechanics%201/Baker-Campbell-Hausdorff%20Formula.md), [Coherent States](Coherent%20States.md)
