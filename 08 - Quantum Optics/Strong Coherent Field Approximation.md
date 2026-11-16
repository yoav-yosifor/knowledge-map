---
tags:
  - quantum-optics
  - concept
  - technique
---
---
## Core Idea

For a strong [coherent state](Coherent%20States.md), the field annihilation operator can be replaced by a classical complex number, $\hat a\to\alpha$, turning a fully quantum light-matter Hamiltonian into a semiclassical one where only the atom remains an operator. This is not literally claiming an infinite-dimensional matrix equals a scalar — it is the statement that the operator's fluctuation part around its own mean is negligible once the mean photon number is large, so light acts as a classical drive while matter stays quantum.

## Key Equation

$$
\hat a = \alpha\hat I + \delta\hat a, \qquad \alpha\equiv\langle\hat a\rangle,\quad \langle\delta\hat a\rangle=0
$$

**Derived From:** splitting the operator into its mean value (as a number times the identity) plus everything left over, $\delta\hat a\equiv\hat a-\alpha\hat I$; because $\alpha$ is defined as $\langle\hat a\rangle$, the fluctuation operator has zero mean by construction. The approximation itself is the further step of setting $\delta\hat a\approx0$ when $|\alpha|$ is large enough that the residual fluctuations don't affect the observable being computed, giving $\hat a\to\alpha$, $\hat a^\dagger\to\alpha^*$.

## Supporting Formulas

- **Why $|\alpha|$ large makes fluctuations negligible:** a coherent state has Poissonian photon statistics, $\bar n=|\alpha|^2$, $\Delta n=\sqrt{\bar n}$, so the *relative* fluctuation is $\dfrac{\Delta n}{\bar n}=\dfrac{1}{\sqrt{\bar n}}\xrightarrow[\bar n\gg1]{}0$ — the field's fractional quantum noise shrinks as the mean field grows, even though the absolute fluctuation $\Delta n$ itself grows.
- **The exact vs. approximate distinction:** $\hat a|\alpha\rangle=\alpha|\alpha\rangle$ is an *exact* eigenvalue equation for a coherent state — but $\hat a^\dagger|\alpha\rangle\neq\alpha^*|\alpha\rangle$ (a coherent state is an eigenstate of $\hat a$, not of $\hat a^\dagger$). Only the expectation value $\langle\alpha|\hat a^\dagger|\alpha\rangle=\alpha^*$ holds exactly, so the replacement $\hat a^\dagger\to\alpha^*$ is genuinely approximate (mean-field), even where $\hat a\to\alpha$ can be motivated by an exact eigenvalue relation.
- **Recovering the classical sinusoidal field:** writing $\alpha(t)=|\alpha|e^{-i\omega t+i\phi}$, the field operator $\hat E\propto\hat a+\hat a^\dagger$ becomes $E(t)\propto\alpha(t)+\alpha^*(t)=2|\alpha|\cos(\omega t-\phi)$ — an ordinary classical wave, with $|\alpha|$ setting the amplitude and $\phi$ the optical phase.
- **Semiclassical Jaynes-Cummings limit:** applying $\hat a\to\alpha$, $\hat a^\dagger\to\alpha^*$ to $\hat H_\text{JC}=\hbar g(\hat\sigma_+\hat a+\hat\sigma_-\hat a^\dagger)$ gives $\hat H_\text{JC}\to\hbar g(\alpha\hat\sigma_++\alpha^*\hat\sigma_-)$ — a classically-driven two-level atom, the semiclassical Rabi problem, recovered as the strong-field limit of the fully quantized [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md).
- **Linearization refinement (keeping fluctuations to first order):** rather than discarding $\delta\hat a$ entirely, expand $\hat a^\dagger\hat a=(\alpha^*+\delta\hat a^\dagger)(\alpha+\delta\hat a)=|\alpha|^2+\alpha^*\delta\hat a+\alpha\,\delta\hat a^\dagger+\delta\hat a^\dagger\delta\hat a$; when $|\alpha|\gg1$ the terms linear in $\delta\hat a$ dominate over the quadratic term $\delta\hat a^\dagger\delta\hat a$, which is dropped while $\alpha^*\delta\hat a+\alpha\,\delta\hat a^\dagger$ is kept. This is the standard starting point for treating quantum noise on top of a strong coherent drive, e.g. the strong local oscillator in [Homodyne Detection](Homodyne%20Detection.md).

## Derivation Outline

1. Represent $\hat a$ in the Fock basis to see explicitly that it is an infinite-dimensional matrix (off-diagonal, $\hat a|n\rangle=\sqrt n|n-1\rangle$), not a number — so "$\hat a\approx\alpha$" needs justification, not just notation.
2. Note that on a coherent state specifically, $\hat a|\alpha\rangle=\alpha|\alpha\rangle$ holds exactly — the same logic as any eigenvalue equation $\hat A|\psi\rangle=\lambda|\psi\rangle$, which never implies $\hat A=\lambda$ as operators, only that $\hat A$ acts like the number $\lambda$ on that one state.
3. Split $\hat a=\alpha\hat I+\delta\hat a$ with $\alpha\equiv\langle\hat a\rangle$, so $\langle\delta\hat a\rangle=0$ by construction; this step is exact and makes no approximation yet.
4. Use the Poissonian photon-number statistics of a coherent state to show the *relative* number fluctuation $\Delta n/\bar n=1/\sqrt{\bar n}$ vanishes as $\bar n\to\infty$ — this is what licenses neglecting $\delta\hat a$ for a strong field.
5. Substitute $\hat a\to\alpha$, $\hat a^\dagger\to\alpha^*$ into a Hamiltonian containing field operators (e.g. the dipole coupling $\propto\hat\sigma_x(\hat a+\hat a^\dagger)$ or the JC interaction) to obtain a Hamiltonian that acts only on the atomic Hilbert space, with the field entering solely through the c-number $\alpha$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Coherent States](Coherent%20States.md), [Jaynes-Cummings Hamiltonian](Jaynes-Cummings%20Hamiltonian.md), [Homodyne Detection](Homodyne%20Detection.md), [Rabi Oscillations](Rabi%20Oscillations.md)
**Full Derivation:**
