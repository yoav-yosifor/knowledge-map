---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

Why optical loss cannot be modeled as a bare rescaling of a field operator. Why mixing in a vacuum-populated second mode through a [beamsplitter-like transformation](Beam%20Splitter%20Transformation.md) is the only way to keep the bosonic commutation relation intact.

## Starting Point

- Bosonic commutation relation for any physical mode: $[\hat a,\hat a^\dagger]=1$
- A naive loss model: attenuate the amplitude by a factor $\eta<1$, $\hat a^{out}\overset{?}{=}\eta\,\hat a^{in}$
- The two-mode beamsplitter scattering matrix $\begin{bmatrix}t&r\\r&t\end{bmatrix}$ with $|t|^2+|r|^2=1$, from [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md)

## Full Derivation

1. Test the naive rescaling $\hat a^{out}=\eta\,\hat a^{in}$ against the bosonic commutator:

   $$
   [\hat a^{out},\hat a^{\dagger out}]=\eta^2[\hat a^{in},\hat a^{\dagger in}]=\eta^2\leq1
   $$

   This step is done because the commutator must equal exactly $1$ for the output to still describe a legitimate quantum field mode; checking it directly against the proposed model is the fastest way to see whether "loss = shrink the amplitude" can possibly be the whole story.

2. Conclude that the naive rescaling is inconsistent whenever $\eta<1$, since it produces a commutator strictly less than $1$, which would let the output mode's quantum noise shrink below what the uncertainty principle allows. This step matters physically: it shows that "losing" some of a beam's amplitude can never be modeled as simply throwing away energy — the field's inherent fluctuations are tied to the commutator, and nothing is allowed to shrink them by fiat.

3. Restore consistency by introducing a second, independent mode $\hat b^{in}$, prepared in the vacuum, and mixing it in with the same structure as a beamsplitter scattering matrix:

   $$
   \hat a^{out}=t\,\hat a^{in}+r\,\hat b^{in}, \qquad t=\eta
   $$

   This step is taken because the only way to keep the transformation linear while restoring the missing commutator "budget" is to bring in a second mode that supplies the rest — physically, this is exactly what happens at a real partially-reflecting or absorbing element, where the "lost" light is replaced by whatever vacuum sits on the other side.

4. Recompute the commutator with both terms present:

   $$
   [\hat a^{out},\hat a^{\dagger out}]=|t|^2[\hat a^{in},\hat a^{\dagger in}]+|r|^2[\hat b^{in},\hat b^{\dagger in}]=|t|^2+|r|^2
   $$

   (the cross terms vanish because the two input modes are independent and commute). This step is done to explicitly verify that mixing in the second mode, rather than being an arbitrary patch, is forced by demanding the algebra come out consistent.

5. Fix $|r|^2=1-|t|^2=1-\eta^2$ so that the commutator equals exactly $1$ again, giving the loss transformation:

   $$
   \hat a^{out}=\eta\,\hat a^{in}+\sqrt{1-\eta^2}\,\hat b^{in}
   $$

   This is the step where the physical content becomes explicit: whatever amplitude is not transmitted is not simply deleted — it is replaced, in exactly the right proportion, by vacuum noise entering from the "lost" side of the effective beamsplitter, so the output always carries at least the ordinary vacuum-level fluctuations even when $\eta\to0$.

## Result

$$
\hat a_{out} = \eta\,\hat a_{in} + \sqrt{1-\eta^2}\,\hat b_{in}, \qquad [\hat a_{out},\hat a_{out}^\dagger]=\eta^2+(1-\eta^2)=1
$$

## Where It's Used

**Concept:** [Beamsplitter Loss Model](Beamsplitter%20Loss%20Model.md)

---

## Links

**Related:** [Beamsplitter Loss Model](Beamsplitter%20Loss%20Model.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Quantum Beamsplitter](Quantum%20Beamsplitter.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md)
