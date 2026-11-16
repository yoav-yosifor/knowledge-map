---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The number of guided modes a slab waveguide supports at a given normalized frequency $V$, for both TE and TM polarization.

## Starting Point

- The normalized characteristic (Key) equations from [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md):
  $$
  \tan^{-1}\sqrt{\tfrac{b}{1-b}} + \tan^{-1}\sqrt{\tfrac{b+a}{1-b}} = V\sqrt{1-b}-N\pi \quad\text{(TE)}
  $$
  $$
  \tan^{-1}\!\left[\Big(\tfrac{n_f}{n_s}\Big)^{2}\sqrt{\tfrac{b}{1-b}}\right] + \tan^{-1}\!\left[\Big(\tfrac{n_f}{n_c}\Big)^{2}\sqrt{\tfrac{b+a}{1-b}}\right] = V\sqrt{1-b}-N\pi \quad\text{(TM)}
  $$
- **Cutoff definition:** a guided mode ceases to be guided at $b=0$, i.e. $\beta=n_sk_0$ — the point where its decay constant into the substrate, $\gamma_s\propto\sqrt b$, vanishes and the mode stops being confined there, becoming a substrate mode instead.

## Full Derivation

1. **Set $b=0$ in the TE Key Equation.**

   $$
   \tan^{-1}(0) + \tan^{-1}\sqrt{a} = V_{c,N}
   $$

   With $b=0$, the first arctan term vanishes and $\sqrt{(b+a)/(1-b)}\to\sqrt a$, so the equation collapses to a single condition on $V$ — this defines the cutoff frequency $V_{c,N}$ of branch $N$.

2. **Solve for the cutoff frequency of branch $N$.**

   $$
   V_{c,N} = N\pi + \tan^{-1}\sqrt{a} \qquad\text{(TE)}
   $$

   Branch $N$ exists as a guided mode only once $V$ exceeds this threshold; below it, that branch has already left the guided-mode window ($b<0$) and become a substrate mode.

3. **Count how many branches $N=0,1,2,\dots$ have $V_{c,N}<V$.**

   $$
   N\pi+\tan^{-1}\sqrt a < V \quad\Longleftrightarrow\quad N < \frac{V-\tan^{-1}\sqrt a}{\pi}
   $$

   The largest integer $N$ satisfying this is $N_{max}=\left\lfloor\frac{V-\tan^{-1}\sqrt a}{\pi}\right\rfloor$ (taking the floor, since $N$ must be a non-negative integer strictly below the bound). The number of guided branches is $N_{max}+1$, since $N$ runs from $0$ to $N_{max}$ inclusive:

   $$
   M_{TE} = \left\lfloor \frac{V-\tan^{-1}\sqrt a}{\pi}\right\rfloor + 1
   $$

4. **Repeat for TM, where the cutoff picks up the extra index-ratio factor from $\bar\gamma_c$.**

   Setting $b=0$ in the TM Key Equation, the first arctan term again vanishes (its argument is $\propto\sqrt b=0$), leaving
   $$
   \tan^{-1}\!\left[\Big(\tfrac{n_f}{n_c}\Big)^{2}\sqrt{a}\right] = V_{c,N} - N\pi
   $$
   the same derivation as steps 1–3 then gives

   $$
   M_{TM} = \left\lfloor \frac{V-\tan^{-1}\!\left[(n_f/n_c)^2\sqrt a\right]}{\pi}\right\rfloor + 1
   $$

   The TM count is always $\le M_{TE}$ (or occasionally equal) since $n_f>n_c$ makes $(n_f/n_c)^2\sqrt a\ge\sqrt a$, so the TM cutoff arctan term is larger, pushing $V_{c,N}$ higher and making each TM branch cut off at a larger $V$ than its TE counterpart.

5. **Equivalent ceiling form and a unified TM shortcut.**

   The floor-based count above can equally be written as a ceiling:

   $$
   N_g = \text{Ceil}\!\left[\frac{V-\tan^{-1}\sqrt a}{\pi}\right]
   $$

   This is identical to $M_{TE}=\lfloor\cdot\rfloor+1$ for all non-integer arguments — the two forms only diverge at the measure-zero case where the argument lands on an exact integer.

   Naming the asymmetry parameter explicitly for each polarization,

   $$
   a_{TE}=\frac{n_s^2-n_c^2}{n_f^2-n_s^2}, \qquad a_{TM}=\left(\frac{n_f}{n_c}\right)^4a_{TE}
   $$

   lets the *same* $N_g$ formula cover both polarizations by swapping which $a$ is substituted, instead of carrying a separate TM cutoff expression — since $(n_f/n_c)^2\sqrt{a_{TE}}=\sqrt{(n_f/n_c)^4a_{TE}}=\sqrt{a_{TM}}$, so $N_g(a_{TM})$ reproduces $M_{TM}$ above exactly.

   A ray-optics cross-check gives the same total: for the asymmetric slab, the total number of guided modes can be read off the TIR picture directly, via $\beta_N=k_0n_f\sin\theta_N$.

## Result

$$
M_{TE} = \left\lfloor \frac{V-\tan^{-1}\sqrt a}{\pi}\right\rfloor + 1, \qquad
M_{TM} = \left\lfloor \frac{V-\tan^{-1}\!\left[(n_f/n_c)^2\sqrt a\right]}{\pi}\right\rfloor + 1
$$

## Where It's Used

**Concept:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md)

---

## Links

**Related:** [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md) (shares the $n_f,n_s,n_c$ notation and the $V,b,a$ normalization used here), [Leaky Waveguide Modes](Leaky%20Waveguide%20Modes.md) (same TIR-picture framing, for angles below cutoff)
