---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

That the photocurrent difference from a balanced [homodyne detector](Homodyne%20Detection.md) is exactly proportional to a single field quadrature of the signal, $\Delta\hat N=\sqrt{2I_{LO}}\,\hat X_\theta$, with the local-oscillator phase $\theta$ selecting which quadrature is read out — and, since this holds as an operator identity, that the *variance* of the measured photocurrent difference reproduces the variance of that quadrature, $\Delta^2\hat N=2I_{LO}\,\Delta^2\hat X_\theta$. This second relation is the one that actually matters experimentally: the mean $\langle\Delta\hat N\rangle$ only sees a classical-like mean field, while the noise floor, squeezing below vacuum, and any other genuinely quantum property of the signal show up only in $\Delta^2\hat N$.

## Starting Point

- Two input modes on a beamsplitter: a weak signal $\hat a$ (arbitrary, unknown quantum state) and a strong local oscillator $\hat b$, prepared in a coherent state $|\beta\rangle$ with $\beta=|\beta|e^{i\theta}$, $|\beta|\gg1$
- 50:50 mixing at $\theta_{BS}=45°$ from [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md): $\hat c=\dfrac{\hat a+\hat b}{\sqrt2}$, $\hat d=\dfrac{\hat b-\hat a}{\sqrt2}$
- Each output port drives a photodetector whose photocurrent is proportional to the incident photon-number operator: $\hat I_c\propto\hat N_c=\hat c^\dagger\hat c$, $\hat I_d\propto\hat N_d=\hat d^\dagger\hat d$
- The rotated quadrature operator, from [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md): $\hat X_\theta=\hat X\cos\theta+\hat P\sin\theta=\dfrac{1}{\sqrt2}\left(\hat a\,e^{-i\theta}+\hat a^\dagger e^{i\theta}\right)$

## Full Derivation

1. Expand the photon-number operator at output port $c$ in terms of the input operators:

   $$
   \hat N_c=\hat c^\dagger\hat c=\frac12(\hat a^\dagger+\hat b^\dagger)(\hat a+\hat b)=\frac12\left(\hat a^\dagger\hat a+\hat a^\dagger\hat b+\hat b^\dagger\hat a+\hat b^\dagger\hat b\right)
   $$

   This step is taken because everything the detector at port $c$ can possibly register is built from this operator, so the whole derivation starts by writing it out fully in terms of the two beams that were actually mixed.

2. Expand the photon-number operator at output port $d$ the same way:

   $$
   \hat N_d=\hat d^\dagger\hat d=\frac12(\hat b^\dagger-\hat a^\dagger)(\hat b-\hat a)=\frac12\left(\hat b^\dagger\hat b-\hat b^\dagger\hat a-\hat a^\dagger\hat b+\hat a^\dagger\hat a\right)
   $$

   Doing this in parallel with step 1, using the same beamsplitter relations, sets up an exact cancellation in the next step rather than an approximate one.

3. Subtract the two photon-number operators:

   $$
   \Delta\hat N\equiv\hat N_c-\hat N_d=\hat a^\dagger\hat b+\hat b^\dagger\hat a
   $$

   The self-terms $\hat a^\dagger\hat a$ and $\hat b^\dagger\hat b$ cancel exactly, leaving only the cross terms. This is the algebraic reason balanced detection works at all: the (usually enormous) photocurrent carried by the local oscillator alone, and any photocurrent carried by the signal alone, drop out identically, leaving only the interference term between the two beams. No approximation has been made yet — this identity is exact for any two input states.

4. Split the local-oscillator operator into its mean and its fluctuation, $\hat b=\beta+\delta\hat b$ with $\beta=\langle\hat b\rangle=|\beta|e^{i\theta}$, and substitute:

   $$
   \Delta\hat N=\hat a^\dagger\beta+\beta^*\hat a+\left(\hat a^\dagger\delta\hat b+\delta\hat b^\dagger\hat a\right)
   $$

   This step separates the operator into a piece that scales with the large amplitude $|\beta|$ and a piece built only from the two $O(1)$ fluctuation operators $\hat a$ and $\delta\hat b$.

5. Take the strong-local-oscillator limit $|\beta|\to\infty$ at fixed signal. The first group of terms grows linearly in $|\beta|$, while the second group stays $O(1)$, so its relative contribution vanishes as $1/|\beta|$:

   $$
   \Delta\hat N\;\xrightarrow{|\beta|\gg1}\;\beta^*\hat a+\beta\,\hat a^\dagger=|\beta|\left(e^{-i\theta}\hat a+e^{i\theta}\hat a^\dagger\right)
   $$

   Physically, this is the amplification step: the local oscillator is strong enough that its own vacuum-level fluctuations $\delta\hat b$ never matter, while it multiplies the weak signal fluctuations up to a macroscopically measurable size. This is exactly what makes a signal too weak for a bare photon counter to see become detectable at all.

6. Recognize the surviving combination as the rotated quadrature operator from the Starting Point, $\hat X_\theta=\frac{1}{\sqrt2}(\hat a\,e^{-i\theta}+\hat a^\dagger e^{i\theta})$, so that $e^{-i\theta}\hat a+e^{i\theta}\hat a^\dagger=\sqrt2\,\hat X_\theta$, and write $|\beta|=\sqrt{I_{LO}}$ where $I_{LO}\equiv|\beta|^2=\langle\hat b^\dagger\hat b\rangle$ is the local-oscillator intensity:

   $$
   \Delta\hat N=|\beta|\sqrt2\,\hat X_\theta=\sqrt{2I_{LO}}\;\hat X_\theta
   $$

   This is the step where the result becomes physically transparent: the photocurrent difference operator — not just its average, but its full operator content including fluctuations — is nothing but the input quadrature $\hat X_\theta$ rescaled by the local-oscillator amplitude. Because $\theta$ is the phase of the local oscillator, sweeping $\theta$ sweeps which quadrature of the signal the detector reads out.

7. **Pass to the variance.** Because $\sqrt{2I_{LO}}$ is a c-number, not an operator, the identity from step 6 carries straight through to the second moment: subtract $\langle\Delta\hat N\rangle=\sqrt{2I_{LO}}\langle\hat X_\theta\rangle$ from $\Delta\hat N$ itself,

   $$
   \Delta\hat N-\langle\Delta\hat N\rangle=\sqrt{2I_{LO}}\left(\hat X_\theta-\langle\hat X_\theta\rangle\right)
   $$

   then square and take the expectation value of both sides:

   $$
   \Delta^2\hat N\equiv\left\langle\left(\Delta\hat N-\langle\Delta\hat N\rangle\right)^2\right\rangle=2I_{LO}\,\Delta^2\hat X_\theta
   $$

   This is the step that makes homodyne detection a genuine quantum-noise measurement rather than only a mean-field readout: a photon counter can report an average, but only this variance relation says that fluctuations recorded in the photocurrent difference — averaged over many runs at fixed LO phase $\theta$ — are literally the quadrature fluctuations of the signal, rescaled by the known, classical factor $2I_{LO}$. For a signal in vacuum, $\Delta^2\hat X_\theta=\tfrac12$ for every $\theta$ (see [Vacuum Fluctuations](Vacuum%20Fluctuations.md)), giving the ordinary shot-noise floor $\Delta^2\hat N=I_{LO}$; for [squeezed](Squeezed%20States.md) input, $\Delta^2\hat X_\theta$ dips below $\tfrac12$ at the squeezed angle, and the homodyne noise dips below that same shot-noise floor by the identical factor.

## Result

$$
\Delta\hat N=\hat N_c-\hat N_d=\sqrt{2I_{LO}}\;\hat X_\theta,\qquad I_{LO}=|\beta|^2=\langle\hat b^\dagger\hat b\rangle,\qquad \hat X_\theta=\frac{1}{\sqrt2}\left(\hat a\,e^{-i\theta}+\hat a^\dagger e^{i\theta}\right)
$$

$$
\Delta^2\hat N=2I_{LO}\,\Delta^2\hat X_\theta
$$

## Where It's Used

**Concept:** [Homodyne Detection](Homodyne%20Detection.md)

---

## Links

**Related:** [Homodyne Detection](Homodyne%20Detection.md), [Quadrature Operators](Quadrature%20Operators.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Standard Quantum Limit](Standard%20Quantum%20Limit.md)
