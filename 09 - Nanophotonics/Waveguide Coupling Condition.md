---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

Direct coupling from a free-space beam into a waveguide is impossible: no incidence angle in the free-space medium ($n_3$) can supply a $z$-component of the wavevector large enough to reach the effective index a guided mode requires ($n_3<n_{eff}<n_2$).

## Key Equation

$$
k_{3,z}=n_3k_0\sin\theta_3=n_2k_0\sin\theta_2=n_{eff}k_0
\;\Rightarrow\;
n_{eff}=n_3\sin\theta_3<n_3
$$

**Derived From:** stated directly in the source — phase-matching the $z$-component of the incident free-space wave's $k$-vector to the guided mode's effective index, via Snell's law across the interfaces, with the index ordering $n_2>n_1>n_3=1$.

## Supporting Formulas

- Index ordering: $n_2>n_1>n_3=1$.
- Guided-wave requirement: $n_3<n_{eff}<n_2$.

## Derivation Outline

1. A guided mode requires its effective index to lie strictly between the surrounding media: $n_3<n_{eff}<n_2$.
2. Phase-matching demands the incident free-space wave's $z$-component of $k$-vector equal the guided mode's propagation constant: $k_{3,z}=n_3k_0\sin\theta_3=n_{eff}k_0$.
3. Since $\sin\theta_3\le1$ for any real incidence angle, the achievable $n_{eff}=n_3\sin\theta_3$ is always less than $n_3$ — never high enough to reach the guided-mode range. No incidence angle works; a coupling mechanism that supplies extra momentum is required.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Prism Coupling](Prism%20Coupling.md), [Grating Coupling](Grating%20Coupling.md)
**Full Derivation:**
