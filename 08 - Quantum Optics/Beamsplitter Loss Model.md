---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Optical loss is physically equivalent to a [beamsplitter](Quantum%20Beamsplitter.md) that mixes the signal with an unavoidable vacuum mode entering the unused port. This is because [vacuum fluctuations](Vacuum%20Fluctuations.md) cannot themselves be attenuated, so any lossy channel necessarily injects extra vacuum noise into its output. That's why [squeezing](Squeezed%20States.md) and other non-classical noise reduction always degrade with loss.

## Key Equation

$$
\hat a_{out} = \eta\,\hat a_{in} + \sqrt{1-|\eta|^2}\,\hat b_{in}
$$

**Derived From:** the requirement that the output mode still satisfy the bosonic commutation relation $[\hat a_{out},\hat a_{out}^\dagger]=1$, which a bare rescaling $\hat a\to\eta\hat a$ alone would violate — the missing commutator must be supplied by mixing in a second, vacuum-populated mode entering the unused port.

## Supporting Formulas

- $\hat X_{\theta,out}=\eta\,\hat X_{\theta,in}+\sqrt{1-|\eta|^2}\,\hat X_{\theta,vac}$ — the loss transformation carried through to any quadrature
- $\Delta X_{\theta,out}^2=|\eta|^2\,\Delta X_{\theta,in}^2+\tfrac12(1-|\eta|^2)$ — variances add in quadrature since the input and the injected vacuum are uncorrelated
- $\eta=1$: lossless, output reproduces the input exactly; $\eta\to0$: output approaches pure vacuum, all signal lost

## Derivation Outline

1. Note that a bare rescaling $\hat a\to\eta\hat a$ cannot be the complete transformation, since it would break the bosonic commutator $[\hat a,\hat a^\dagger]=1$.
2. Introduce a second, vacuum-populated mode $\hat b_{in}$ entering the unused port of an effective beamsplitter to restore the commutator, which fixes the coefficient $\sqrt{1-|\eta|^2}$.
3. Propagate the same linear transformation to the quadrature operators and add variances in quadrature, since the signal and the injected vacuum are statistically independent.

## Physical Intuition

It's tempting to think that "losing" some of a light beam just means multiplying its amplitude by some number less than one — but quantum mechanically that can't be the whole story, because a bare rescaling would let you shrink the field's inherent quantum noise along with its signal, which the uncertainty principle forbids. The fix is that any real lossy element — a partially reflecting mirror, an absorbing filter, a lossy fiber — is secretly a beamsplitter: part of your beam is preserved, but the "missing" part isn't simply discarded, it's replaced by vacuum leaking in from the unused side of that beamsplitter. That vacuum contribution can never be removed, so every lossy element you send a quantum state through adds back a fixed amount of vacuum-level noise to the output. This is exactly why squeezed light — whose whole value comes from being quieter than the vacuum in one quadrature — is so fragile: even a little loss mixes ordinary vacuum noise back in and erodes the squeezing, which is why low-loss optics are essential wherever squeezed light is used.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Vacuum Fluctuations](Vacuum%20Fluctuations.md), [Squeezed States](Squeezed%20States.md), [Standard Quantum Limit](Standard%20Quantum%20Limit.md), [Quantum Beamsplitter](Quantum%20Beamsplitter.md)
**Full Derivation:** [Beamsplitter Loss Derivation](Beamsplitter%20Loss%20Derivation.md)
