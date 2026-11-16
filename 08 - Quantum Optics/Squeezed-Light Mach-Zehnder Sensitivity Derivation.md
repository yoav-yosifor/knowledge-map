---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

This derives the mean and variance of the output photon-number difference of a balanced [Mach-Zehnder interferometer](Squeezed-Light%20Mach-Zehnder%20Interferometer.md) fed with a coherent state and squeezed vacuum. From those, it also derives the resulting [phase sensitivity](Measurement%20Sensitivity.md), $\Delta\phi_{min}\approx e^{g}/\alpha$.

## Starting Point

- Balanced beamsplitters, $t_1=r_1=t_2=r_2=1/\sqrt2$, from [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md)
- Heisenberg-picture input operators that already absorb the state preparation: $\hat a_{in}\equiv\hat D^\dagger(\alpha)\,\hat a\,\hat D(\alpha)$, $\hat b_{in}\equiv\hat S^\dagger(g)\,\hat b\,\hat S(g)$, so that vacuum expectation values of these operators reproduce the coherent/squeezed-state expectation values of $\hat a,\hat b$
- Squeezing transformation $\hat b_{in}=\hat b\cosh g+\hat b^\dagger\sinh g$, from [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md)

## Full Derivation

1. Define $\hat a_{in},\hat b_{in}$ as the Heisenberg-picture operators that have already absorbed the displacement and squeezing of the input state. This is done so the calculation can be carried out entirely by propagating operators through the interferometer and only substituting the vacuum expectation value at the very end, rather than tracking a complicated evolving state.

2. **Propagate through the interferometer.**

   $$
   \hat a_{out}=\frac12\left[\hat a_{in}(e^{i\phi}-1)+i\hat b_{in}(e^{i\phi}+1)\right]
   $$

   Propagating $\hat a_{in},\hat b_{in}$ through the first beamsplitter (with a phase $\phi$ imprinted in arm $a$) and then the second gives this, and the analogous expression for $\hat b_{out}$. This mirrors ordinary interferometry: two beamsplitters and a relative phase between the arms is exactly what turns a phase difference into an intensity difference at the output.

3. **Form the photon-number difference.**

   $$
   \hat n_a-\hat n_b=-\hat a_{in}^\dagger\hat a_{in}\cos\phi+\left(\hat a_{in}^\dagger\hat b_{in}+\hat b_{in}^\dagger\hat a_{in}\right)\sin\phi+\hat b_{in}^\dagger\hat b_{in}\cos\phi
   $$

   Forming the output photon-number difference $\hat n_a-\hat n_b$ and simplifying using the trigonometric identities for $(e^{\mp i\phi}\mp1)(e^{\pm i\phi}\pm1)$ arrives at this. This is the natural observable to track because it is precisely what a balanced photodetector-difference measurement reads out, and it depends on $\phi$ through both a diagonal ($\cos\phi$) and a cross ($\sin\phi$) term.

4. **Evaluate the mean signal.**

   $$
   \langle\hat n_a-\hat n_b\rangle=\left(\sinh^2g-\alpha^2\right)\cos\phi
   $$

   Evaluating the mean at general $\phi$: since mode $a$ and mode $b$ are prepared independently and $\langle\hat b_{in}\rangle=0$ for a squeezed vacuum, the cross term vanishes in the mean, leaving this. This isolates where the interferometer is most sensitive: wherever $\cos\phi$ is largest the signal is largest, but that is not yet the point of best sensitivity because the noise has not been accounted for.

5. Specialize to the dark fringe $\phi=\pi/2$, where $\cos\phi=0$ kills the diagonal terms entirely and only the cross term $\hat a_{in}^\dagger\hat b_{in}+\hat b_{in}^\dagger\hat a_{in}$ survives; its mean is zero, so the variance equals its second moment. This is the standard operating point for interferometric sensitivity because it is where a tiny phase deviation produces the cleanest linear response against the smallest possible background.

6. **Compute the variance.**

   $$
   \Delta^2(\hat n_a-\hat n_b)\big|_{\phi=\pi/2}=\alpha^2e^{2g}+\sinh^2g
   $$

   Expanding $\langle(\hat a_{in}^\dagger\hat b_{in}+\hat b_{in}^\dagger\hat a_{in})^2\rangle$ into its four operator-ordered terms and evaluating each using $\hat b_{in}=\hat b\cosh g+\hat b^\dagger\sinh g$ and $\langle\hat a_{in}^\dagger\hat a_{in}\rangle=\alpha^2$, then summing using $\sinh2g=2\sinh g\cosh g$ and $\cosh2g+\sinh2g=e^{2g}$, gives this. This step converts the abstract cross-term operator into a concrete number, and it is exactly here that the squeezing parameter $g$ enters the noise budget.

7. **Assemble the sensitivity.**

   $$
   \partial_\phi\langle\hat n_a-\hat n_b\rangle\big|_{\pi/2}=\alpha^2-\sinh^2g
   $$

   Differentiating the mean signal with respect to $\phi$ at the dark fringe gives this, which combines with the variance to form the sensitivity

   $$
   \Delta\phi_{min}=\frac{\sqrt{\Delta^2(\hat n_a-\hat n_b)}}{\left|\partial_\phi\langle\hat n_a-\hat n_b\rangle\right|}
   $$

   This assembles the two ingredients — how fast the signal moves and how much noise sits underneath it — into the one number that answers "how small a phase shift can this device resolve."

8. **Take the strong-field limit.**

   $$
   \sinh^2g\ll\alpha^2 \;\;\Longrightarrow\;\; \Delta\phi_{min}\approx\frac{e^g}{\alpha}
   $$

   This limit is the physically relevant one for a real interferometer, where the bright coherent beam vastly outnumbers the photons contributed by the squeezed vacuum, and it is where the clean exponential improvement over the ordinary $1/\alpha$ shot-noise limit becomes visible.

## Result

$$
\Delta\phi_{min}\big|_{\phi=\pi/2} \approx \frac{e^{g}}{\alpha}
$$

## Where It's Used

**Concept:** [Squeezed-Light Mach-Zehnder Interferometer](Squeezed-Light%20Mach-Zehnder%20Interferometer.md)

---

## Links

**Related:** [Squeezed-Light Mach-Zehnder Interferometer](Squeezed-Light%20Mach-Zehnder%20Interferometer.md), [Standard Quantum Limit](Standard%20Quantum%20Limit.md), [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md), [Measurement Sensitivity](Measurement%20Sensitivity.md)
