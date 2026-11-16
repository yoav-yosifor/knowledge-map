---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

This derives the output operator, the mean and variance of the photon number, and the resulting phase sensitivity of an [SU(1,1) interferometer](SU(1,1)%20Interferometer.md). The interferometer is built from two degenerate optical parametric amplifiers with a [relative phase](Phase-Space%20Rotation%20Operator.md) between them.

## Starting Point

- Single squeezing (OPA) stage: $\hat a\to\hat a\cosh g+\hat a^\dagger\sinh g$, from [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md)
- Phase-rotation operator: $\hat a\to\hat a\,e^{i\phi}$, from [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md)
- Undepleted pump and degenerate down-conversion assumed, so signal and idler collapse to a single mode $\hat a$
- Vacuum input state

## Full Derivation

1. **Propagate through the first OPA.**

   $$
   \hat a_1=\hat a\cosh g+\hat a^\dagger\sinh g
   $$

   This is done because each nonlinear crystal, in the undepleted-pump approximation, acts on the field exactly like the squeezing operator conjugation already established for a single stage.

2. **Apply the phase rotation.**

   $$
   \hat a_2=\hat a\cosh g\,e^{i\phi}+\hat a^\dagger\sinh g\,e^{-i\phi}
   $$

   Applying the phase rotation between the two stages gives this. This step inserts the one adjustable knob of the device — the relative phase between the two crystals — exactly the role a path-length difference plays in an ordinary interferometer.

3. **Propagate through the second OPA.**

   $$
   \hat a_{out}=\hat a\left[\cosh^2g\,e^{i\phi}+\sinh^2g\,e^{-i\phi}\right]+\hat a^\dagger\sinh(2g)\cos\phi
   $$

   Propagating through the second OPA and collecting terms gives this. This combines both nonlinear stages into a single effective input-output relation, the SU(1,1) analogue of propagating through two beamsplitters in an ordinary Mach-Zehnder interferometer.

4. **Evaluate the two special phases.**

   $$
   \hat a_{out}\big|_{\phi=0}=\hat a\cosh(2g)+\hat a^\dagger\sinh(2g), \qquad \hat a_{out}\big|_{\phi=\pi/2}=i\hat a
   $$

   At $\phi=0$ the two stages add directly, giving the first expression above (identical to one crystal of double length); at $\phi=\pi/2$, using $\cosh^2g-\sinh^2g=1$, the stages exactly cancel, giving the second. This step reveals where the device's interference lives — not in an intensity fringe as in an ordinary interferometer, but in whether the accumulated squeezing from the first stage is reinforced or undone by the second.

5. **Compute the mean photon number.**

   $$
   \left\langle\hat a_{out}^\dagger\hat a_{out}\right\rangle=\sinh^2(2g)\cos^2\phi
   $$

   With vacuum input: since $\langle\hat a^\dagger\hat a\rangle=0$ and $\langle\hat a\hat a^\dagger\rangle=1$ on vacuum, only the normal-ordered $\hat a\hat a^\dagger$ contribution survives, giving this. This is the key qualitative result: even though nothing but vacuum was sent in, the device produces a real, phase-dependent output signal, because the nonlinear stages actively create photon pairs rather than merely redistributing existing ones.

6. **Compute the variance.**

   $$
   \Delta^2(\hat a_{out}^\dagger\hat a_{out})\big|_{\phi=\pi/2}=\sinh^2(2g)\cos^2\phi\left[\sinh^2(2g)\cos2\phi+2\sinh^4g+2\cosh^4g\right]
   $$

   Expanding $\langle(\hat a_{out}^\dagger\hat a_{out})^2\rangle$, keeping only terms with an even number of creation/annihilation operators (odd terms vanish on vacuum), and simplifying using $\sinh^2g-\cosh^2g=-1$ gives this. This step supplies the noise half of the sensitivity calculation, mirroring how the variance was needed in the ordinary Mach-Zehnder case.

7. **Form the sensitivity.**

   $$
   \Delta\phi_{min}=\frac{\sqrt{\Delta^2(\hat a_{out}^\dagger\hat a_{out})}}{\left|\partial_\phi\langle\hat a_{out}^\dagger\hat a_{out}\rangle\right|}
   $$

   A factor of $\cos\phi$ cancels between numerator and denominator, leaving a finite ratio even though both individually vanish at $\phi=\pi/2$. This cancellation is what makes $\phi=\pi/2$ usable as an operating point at all, exactly as the dark-fringe cancellation did for the beamsplitter-based interferometer.

8. **Take the strong-squeezing limit.**

   $$
   \Delta\phi_{min}\big|_{\phi=\pi/2}=\frac{1}{\sqrt2\,\sinh2g} \;\;\xrightarrow{\sinh(2g)\approx e^{2g}/2}\;\; \Delta\phi_{min}\approx\sqrt2\,e^{-2g}
   $$

   Evaluating at $\phi=\pi/2$ (where $\cos2\phi=-1$) gives the first expression, then taking the strong-squeezing limit gives the second. This final limit is where the headline result becomes visible: the sensitivity improves exponentially in $g$ with no coherent seed light needed anywhere in the device, in contrast to the $e^{g}/\alpha$ scaling of the beamsplitter-based squeezed interferometer.

## Result

$$
\Delta\phi_{min}\big|_{\phi=\pi/2} = \frac{1}{\sqrt2\,\sinh(2g)} \approx \frac{\sqrt2}{e^{2g}}
$$

## Where It's Used

**Concept:** [SU(1,1) Interferometer](SU(1,1)%20Interferometer.md)

---

## Links

**Related:** [SU(1,1) Interferometer](SU(1,1)%20Interferometer.md), [Squeezed-Light Mach-Zehnder Sensitivity Derivation](Squeezed-Light%20Mach-Zehnder%20Sensitivity%20Derivation.md), [Squeezing Operator Derivation](Squeezing%20Operator%20Derivation.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md)
