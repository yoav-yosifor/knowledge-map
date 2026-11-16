---
tags:
  - nanophotonics
  - concept
---
---
## Core Idea

An all-pass ring has two ways to lose the light it stored: some leaks back out through the bus coupler, and some is dissipated inside the loop. **Critical coupling** is the operating point where these two rates are exactly equal ($\kappa=\alpha$). On resonance the light that leaks back out then destructively interferes perfectly with the directly transmitted light, the through port goes completely dark ($T=0$), and the energy stored in the ring is maximal.

## Key Equation

$$
\kappa=\alpha\ \Longrightarrow\ T\big|_{\omega=\omega_0}=0,\qquad
\left|\frac{E_1}{E_{in}}\right|^2_{\omega=\omega_0,\ \kappa=\alpha}=\frac{1}{\kappa}
$$

**Derived From:** setting $\kappa=\alpha$ in the on-resonance all-pass through-transmission $T=\dfrac{\sqrt{1-\kappa}-\sqrt{1-\alpha}}{1-\sqrt{(1-\kappa)(1-\alpha)}}$ (numerator vanishes), and in the on-resonance build-up $\left|E_1/E_{in}\right|^2=\dfrac{\kappa}{\left[1-\sqrt{(1-\kappa)(1-\alpha)}\right]^2}$ (denominator becomes $\kappa^2$).

- $\kappa$ — power coupling coefficient of the bus–ring directional coupler
- $\alpha$ — fractional power loss per round trip inside the ring
- $E_1$ — circulating field just after the coupler; $E_{in}$ — input field in the bus

## Supporting Formulas

- On-resonance through transmission: $$T\big|_{\omega=\omega_0}=\frac{\sqrt{1-\kappa}-\sqrt{1-\alpha}}{1-\sqrt{(1-\kappa)(1-\alpha)}}$$
- **Under-coupled** $\kappa<\alpha$: internal loss dominates, $T>0$, sign of $T$ one way.
- **Over-coupled** $\kappa>\alpha$: coupler leakage dominates, $T>0$ again but with the opposite sign of the numerator; the phase response differs from the under-coupled case even though $|T|$ can match.
- **Critically coupled** $\kappa=\alpha$: $T=0$ exactly on resonance — the notch reaches the floor.
- The circulating intensity can exceed the input intensity ($|E_1|>|E_{in}|$) whenever $$\alpha<\frac{2\sqrt{\kappa}}{1+\sqrt{\kappa}}$$ i.e. when the losses are low enough; at critical coupling the build-up is $1/\kappa$, which is $\gg1$ for weak coupling.

## Derivation Outline

1. Take the all-pass through-transmission $T(\Delta\omega)$ and evaluate it on resonance ($e^{-i\varphi}\to1$).
2. The numerator $\sqrt{1-\kappa}-\sqrt{1-\alpha}$ vanishes iff $\kappa=\alpha$ — this is the critical-coupling condition.
3. Evaluate the build-up $\left|E_1/E_{in}\right|^2$ on resonance; at $\kappa=\alpha$ the bracket $1-\sqrt{(1-\kappa)(1-\alpha)}=\kappa$, so the build-up is $\kappa/\kappa^2=1/\kappa$.
4. Compare $\sqrt{\kappa}$ against $1-\sqrt{(1-\kappa)(1-\alpha)}$ to get the condition $\alpha<2\sqrt{\kappa}/(1+\sqrt{\kappa})$ for $|E_1|>|E_{in}|$.

## Physical Intuition

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Ring Resonator](Ring%20Resonator.md), [Add-Drop Multiplexer](Add-Drop%20Multiplexer.md), [All-Pass Ring Transfer Function Derivation](All-Pass%20Ring%20Transfer%20Function%20Derivation.md), [Directional Coupler](Directional%20Coupler.md)
**Full Derivation:**
