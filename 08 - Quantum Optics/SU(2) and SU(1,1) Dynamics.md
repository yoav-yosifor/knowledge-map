---
tags:
  - quantum-optics
  - concept
---
---
## Core Idea

Every linear optical interaction Hamiltonian, no matter how many modes are involved, reduces to just [phase rotations](Phase-Space%20Rotation%20Operator.md) and [beamsplitter-like](Beam%20Splitter%20Transformation.md) mode-swapping. This is the compact SU(2) group, and it can only ever redistribute photons that are already present. A genuinely non-linear medium is different: its interaction Hamiltonian mixes creation and annihilation operators together, as happens in [parametric down-conversion](Optical%20Parametric%20Amplifier.md). That realizes the non-compact SU(1,1) group, which creates and destroys photons in pairs and is capable of unbounded exponential gain.

## Key Equation

$$
\hat H_\text{linear} = \sum_{ij}h_{ij}\,\hat a_i^\dagger\hat a_j \ \ (\text{SU(2)}), \qquad \hat H_\text{squeezing} = \kappa\hat a^2+\kappa^*\hat a^{\dagger2} \ \ (\text{SU(1,1)})
$$

**Derived From:** writing the general RWA light-matter interaction Hamiltonian $\hat H=-\int d^3r\,P^{(-)}(\vec r)\cdot E^{(+)}(\vec r)+h.c.$ for a linear medium ($P^{(+)}=\chi^{(1)}E^{(+)}$), which yields only number-conserving bilinear terms $\hat a_i^\dagger\hat a_j$; contrasting this with a $\chi^{(2)}$ medium's three-wave-mixing interaction restricted to the degenerate signal-idler case, which instead yields the pair-creating/annihilating terms $\hat a^2,\hat a^{\dagger2}$ — see [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md).

## Supporting Formulas

- Linear-optics unitary, diagonal case ($i=j$): $\hat U^{(ii)}=e^{-i\theta_{ii}\hat a_i^\dagger\hat a_i}$, $\hat U^{(ii)\dagger}\hat a_i\hat U^{(ii)}=e^{-i\theta_{ii}}\hat a_i$ — a pure phase-space rotation; see [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md)
- Linear-optics unitary, off-diagonal case ($i\neq j$): $\hat U^{(ij)}=e^{-i(\theta_{ij}\hat a_i^\dagger\hat a_j+\theta_{ij}^*\hat a_j^\dagger\hat a_i)}$, $\hat U^{(ij)\dagger}\hat a_i\hat U^{(ij)}=\cos\tfrac{\theta_{ij}}{2}\hat a_i+i\sin\tfrac{\theta_{ij}}{2}\hat a_j$ — a beamsplitter-like interaction between same-frequency modes; see [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md)
- Generic Bogoliubov constraint: for any Hamiltonian quadratic in $\hat a,\hat a^\dagger$, the resulting time evolution $\hat a(t)=\mu\hat a(0)-\nu\hat a^\dagger(0)$ satisfies $|\mu|^2-|\nu|^2=1$ regardless of the specific parameters — full derivation in [Squeezing Heisenberg Derivation](Squeezing%20Heisenberg%20Derivation.md)
- SU(2) transformations are represented by ordinary rotations on a sphere — compact and bounded, which is why linear optics alone can never amplify a signal beyond redistributing the photons already present
- SU(1,1) transformations are represented by Lorentz boosts on a hyperbola — non-compact and unbounded, the deep reason squeezing/parametric gain grows exponentially without any inherent ceiling (until pump depletion or other physical limits intervene)

## Derivation Outline

1. Write the general RWA interaction Hamiltonian for a field coupled to a medium's induced polarization.
2. Specialize to a linear medium and show the resulting Hamiltonian only contains number-conserving bilinear terms; split these into same-mode (rotation) and cross-mode (beamsplitter) pieces.
3. Specialize instead to a $\chi^{(2)}$ medium's three-wave-mixing interaction with an undepleted classical pump, and take the degenerate signal-idler limit, showing the resulting Hamiltonian is exactly the squeezing generator.
4. Recognize the two resulting families of transformations as representations of the compact group SU(2) and the non-compact group SU(1,1) respectively.

## Physical Intuition

Any optical element built only from mirrors, lenses, phase plates, and beamsplitters — no matter how elaborate the combination — can only ever reshuffle the photons that go in: rotate their phase, or trade them between different paths and modes. That is the entire content of "linear optics," and it is why no arrangement of purely linear elements can amplify light or create genuinely non-classical states from a classical input — there is a strict conservation law (total photon number) that no amount of cleverness with mirrors can get around. A non-linear medium breaks this constraint completely: instead of a term that just moves a photon from mode $i$ to mode $j$, it can have a term that annihilates two photons of one kind while creating two of another (or, in the degenerate case, that simply creates or destroys pairs of photons in the very same mode). This qualitative difference — conserving photon number versus creating/destroying photons in matched pairs — is exactly what separates the two mathematical structures: SU(2), which behaves like ordinary bounded rotations, and SU(1,1), which behaves like the unbounded boosts of special relativity. That structural difference is the real reason parametric amplification and squeezing can produce exponential gain with no inherent limit, while no combination of beamsplitters and phase shifters ever can.

## Isomorphisms

- SU(1,1) transformations are mathematically the same as Lorentz boosts on a hyperbola — the same non-compact structure that governs relativistic velocity addition — while SU(2) is the same compact rotation-on-a-sphere structure that governs ordinary angular momentum and qubit rotations. See the [Bloch Sphere](../10%20-%20Quantum%20Information/Bloch%20Sphere.md) and the [Isomorphism Log](../00%20-%20Index/Isomorphism%20Log.md).

## Open Questions

- [ ]

---

## Links

**Related:** [Optical Parametric Amplifier](Optical%20Parametric%20Amplifier.md), [SU(1,1) Interferometer](SU(1,1)%20Interferometer.md), [Beam Splitter Transformation](Beam%20Splitter%20Transformation.md), [Phase-Space Rotation Operator](Phase-Space%20Rotation%20Operator.md), [Squeezed States](Squeezed%20States.md)
**Full Derivation:** [Squeezing Heisenberg Derivation](Squeezing%20Heisenberg%20Derivation.md)
