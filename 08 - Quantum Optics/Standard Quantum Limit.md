---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

In a phase-sensitive interferometric measurement operated at its most sensitive point, the achievable signal-to-noise ratio grows only as the square root of the photon flux when ordinary (vacuum) light enters the unused port. That's because [vacuum fluctuations](Vacuum%20Fluctuations.md) entering the unused port set an irreducible noise floor. This limit can be beaten by injecting [squeezed vacuum](Squeezed%20States.md) there instead.

## Key Equation

$$
SNR \approx \delta\phi\,\sqrt{\langle\hat n^a_{in}\rangle}
$$

**Derived From:** expanding the interferometer's output photocurrent-difference operator $\hat I_{out}=\hat n^a_{out}-\hat n^b_{out}$ for a coherent-state input in port $a$ and vacuum in the unused port $b$, then linearizing near the dark fringe $\phi=\pi/2-\delta\phi$ with $\delta\phi\ll1$.

## Supporting Formulas

- $\hat I_{out}=\cos\phi\,(\hat n^a_{in}-\hat n^b_{in})+\sin\phi\,(\hat a_{in}^\dagger\hat b_{in}+\hat b_{in}^\dagger\hat a_{in})$ — output photocurrent-difference operator of the effective interferometer beamsplitter
- $\langle\hat I_{out}\rangle=\cos\phi\,\langle\hat n^a_{in}\rangle$; $\langle\Delta\hat I_{out}^2\rangle=\cos^2\phi\,\langle(\Delta\hat n^a_{in})^2\rangle+\sin^2\phi\,\langle\hat n^a_{in}\rangle$ — the second noise term arises entirely from vacuum fluctuations entering the unused port $b$
- Caves' squeezed-light enhancement: injecting squeezed vacuum $|0_r\rangle=\hat S(r)|0\rangle$ into the unused port instead of ordinary vacuum improves the SNR to $SNR\approx e^{r/2}\,\delta\phi\,\sqrt{\langle\hat n^a_{in}\rangle}$ — an improvement by the factor $e^{r/2}$ over the standard quantum limit
- This squeezed-vacuum injection scheme (C. M. Caves, *Phys. Rev. D* **23**, 1693, 1981) is exactly the technique used in current-generation LIGO to push gravitational-wave sensitivity below the standard quantum limit

## Derivation Outline

1. Model the interferometer as an effective single beamsplitter with transmission/reflection amplitudes $\cos(\phi/2),\sin(\phi/2)$, where $\phi$ is the imprinted phase difference between the two arms.
2. Expand the output photocurrent-difference operator in terms of the input mode operators.
3. Take the mean and variance of this operator for a coherent-state signal plus vacuum (or squeezed-vacuum) input at the unused port.
4. Linearize near the dark fringe $\phi=\pi/2$ to express the SNR in terms of the small phase deviation $\delta\phi$ to be measured.

## Physical Intuition

An interferometer designed to detect a tiny phase shift — like the one a passing gravitational wave imprints on light — is usually operated at its "dark fringe," the operating point where the output signal is most sensitive to small phase changes. But even with a perfect light source and perfect optics, the measurement isn't noiseless: the port of the interferometer you're *not* sending light into is not simply empty — it still has vacuum fluctuations leaking in, and those fluctuations directly add noise to the output. The only way to beat this "standard quantum limit" with ordinary light is to use more photons, and sensitivity only improves as the square root of that photon number — a slow, expensive way to gain sensitivity. Caves' insight was that you don't have to accept ordinary vacuum noise at that unused port: if you deliberately inject squeezed vacuum there instead — quieter than ordinary vacuum in exactly the quadrature that matters for this measurement — you suppress that noise contribution and improve the sensitivity beyond what more photons alone could buy you. This is precisely the trick modern gravitational-wave detectors use to see fainter signals than the vacuum noise floor would otherwise allow.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Beamsplitter Loss Model](Beamsplitter%20Loss%20Model.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Squeezed States](Squeezed%20States.md), [Homodyne Detection](Homodyne%20Detection.md)
**Full Derivation:**
