---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

The rigorous quantum [second-order coherence function](Second-Order%20Coherence%20Function.md) is a normal-ordered intensity correlator — literally the probability a pair of photodetectors clicks together. Its deviation from the Poissonian value is quantified by the Mandel Q-parameter. Because a classical field can never produce a Q below zero, this is a clean, calculable test for non-classical light.

## Key Equation

$$
G^{(2)}(\tau) = \left\langle:\hat I(\vec x_2)\hat I(\vec x_1):\right\rangle, \qquad Q = \frac{\langle:\hat n^2:\rangle-\langle\hat n\rangle^2}{\langle\hat n\rangle} = \frac{\Delta n^2-\langle\hat n\rangle}{\langle\hat n\rangle}
$$

**Derived From:** the actual two-photodetector coincidence probability computed from first-order perturbation theory of the detector-field interaction — full derivation in [Two-Photon Coincidence Probability Derivation](Two-Photon%20Coincidence%20Probability%20Derivation.md); normal ordering (all $\hat E^{(-)}$ to the left of all $\hat E^{(+)}$) is not a convention but a consequence of that derivation, since it is exactly what an ideal photon-counting detector measures.

## Supporting Formulas

- Single-mode, zero-delay form: $G^{(2)}(0)=\langle:\hat n^2:\rangle=\langle\hat a^\dagger\hat a^\dagger\hat a\hat a\rangle=\langle\hat n^2\rangle-\langle\hat n\rangle$, and $g^{(2)}(0)=\langle:\hat n^2:\rangle/\langle\hat n\rangle^2=1+Q/\langle\hat n\rangle$
- General $n$-fold coherence: $G^{(n)}=\langle:\hat I(\vec x_n)\cdots\hat I(\vec x_1):\rangle$; for a coherent state every order factorizes exactly into the classical result, $g^{(n)}=1\ \forall n$ — a state whose coherence functions fully factorize is called "coherent," meaning its detection events are statistically uncorrelated
- $Q>0$: super-Poissonian; $Q=0$: Poissonian (e.g. any coherent state); $Q<0$: sub-Poissonian, a signature impossible for any classical field
- Classical light is always super- or exactly Poissonian: for $\hat\rho=\int d^2\alpha\,P(\alpha)|\alpha\rangle\langle\alpha|$ with $P(\alpha)$ a genuine probability distribution, $\Delta n^2-\langle\hat n\rangle=(\Delta|\alpha|^2)^2\geq0$ always — so $Q<0$ can only occur when $P(\alpha)$ fails to be a legitimate probability distribution (negative or more singular than a delta function), the Glauber-Sudarshan non-classicality test
- Photon bunching (classical, $g^{(2)}(\tau)\leq g^{(2)}(0)$: correlations always peak at zero delay) versus photon antibunching (a genuinely quantum violation of that bound, a dip rather than a peak at $\tau=0$)
- Quantum operator (normal-ordered) form of the general field correlator: $g^{(1)}(\tau)=\langle\hat E^{(-)}(t)\hat E^{(+)}(t+\tau)\rangle/\langle\hat E^{(-)}(t)\hat E^{(+)}(t)\rangle$ — the quantum generalization of the classical [First-Order Coherence Function](First-Order%20Coherence%20Function.md); first-order coherence alone cannot reveal any distinctly quantum property of light, since (by the [Wiener-Khinchin Theorem](Wiener-Khinchin%20Theorem.md)) $g^{(1)}$ depends only on the mean energy per mode
- First- and second-order coherence probe genuinely different physics — a state can be fully first-order coherent while still being second-order non-classical (sub-Poissonian), and $g^{(1)}$, $g^{(2)}$ together still do not uniquely fix the quantum state
- Single photon at a beamsplitter: $G^{(2)}(0)=0$ exactly — a purely particle-like, quantum signature; see [Quantum Beamsplitter](Quantum%20Beamsplitter.md)

## Derivation Outline

1. Compute the probability that two photodetectors click within a given time window as a first-order perturbative transition rate driven by the field operator, summed over all possible final field states.
2. Use completeness of the final field states to collapse the sum into a single expectation value in the initial field state, which is automatically normal-ordered because the detector interaction Hamiltonian only couples via the positive-frequency (annihilation-type) field operator.
3. Identify this normal-ordered expectation value as $G^{(2)}$, generalizing naturally to $G^{(n)}$ for $n$-fold coincidence detection.
4. Specialize to a single mode to get the Mandel $Q$-parameter form, and use the coherent-state expansion of a general classical (P-representable) density matrix to prove classical light is always super-Poissonian.

## Physical Intuition

The classical second-order coherence function is a reasonable-sounding guess — just correlate the intensity with itself at two times — but it turns out not to be exactly what a real experiment measures. A pair of photodetectors doesn't measure "intensity times intensity" in the naive sense; each detector fires by absorbing a photon, and the *order* in which the field operators act matters. Once this is derived properly from how a detector actually interacts with the field, normal ordering falls out automatically, and $G^{(2)}$ becomes precisely the coincidence rate of two photon-counting detectors. The payoff is a genuinely useful non-classicality test: the Mandel $Q$-parameter measures whether the photon-number fluctuations are wider than (super-Poissonian), equal to (Poissonian), or narrower than (sub-Poissonian) what a purely random, classical process could ever produce. Classical light — however cleverly you shape its noise — can only ever broaden the count distribution, never narrow it, because classical intensity fluctuations only add extra randomness on top of ordinary shot noise. A negative $Q$ is therefore a clean, unambiguous fingerprint that the light source cannot be described by any classical probability distribution over field amplitudes — it requires the light to be made of discrete quantum emitters behaving like particles that "avoid" bunching together.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Second-Order Coherence Function](Second-Order%20Coherence%20Function.md), [First-Order Coherence Function](First-Order%20Coherence%20Function.md), [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md), [Hong-Ou-Mandel Effect](Hong-Ou-Mandel%20Effect.md), [Quantum Beamsplitter](Quantum%20Beamsplitter.md)
**Full Derivation:** [Two-Photon Coincidence Probability Derivation](Two-Photon%20Coincidence%20Probability%20Derivation.md)
