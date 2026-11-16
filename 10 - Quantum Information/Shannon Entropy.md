---
tags:
  - quantum-information
  - concept
---
---
## Core Idea

Shannon entropy quantifies the average information content of a classical random process — equivalently, its uncertainty, or the minimal number of bits needed to describe its outcomes. It is maximized for a uniform distribution.

## Key Equation

$$
H(X) = -\sum_i p_i \log p_i
$$

**Derived From:** the requirement that a measure of "surprise" of an outcome with probability $p_i$ be additive over independent events, giving $-\log p_i$ per outcome, averaged over the distribution.

## Supporting Formulas

- $H(X)\ge0$; for a binary variable with probabilities $(p,1-p)$, entropy is maximal at $p=\tfrac12$

## Derivation Outline

1. Require a measure of "surprise" for an outcome of probability $p_i$ that is additive over independent events.
2. That requirement forces the per-outcome surprise to be $-\log p_i$.
3. Average $-\log p_i$ over the distribution, weighted by $p_i$: $H(X)=-\sum_i p_i\log p_i$.
4. Check limiting behavior: $H=0$ for a certain outcome, maximal for the uniform distribution ($p=1/2$ in the binary case).

## Physical Intuition

Suppose someone is about to tell you the outcome of some random process, and you want a single number that captures how surprised you should expect to be. An outcome that almost never happens is very informative when it does happen — learning it tells you a lot — while an outcome you were already nearly certain of tells you almost nothing new. Shannon entropy is what you get when you weight each outcome's "surprise" by how often that outcome actually occurs and add it all up: it's the average amount of new information you receive per outcome, and equivalently, it's the fewest number of yes/no questions, or bits, you'd need on average to pin down which outcome occurred if you were guessing optimally. A process that's completely predictable — the same outcome every time — carries zero entropy, because there's genuinely nothing to learn from watching it. At the other extreme, spreading the probability out as evenly as possible across all the outcomes maximizes the entropy, because no outcome is favored over any other, so every individual result is maximally surprising and you can't shortcut your guessing strategy with any bias at all. That's why, for something as simple as a single coin that can only come up one of two ways, the uncertainty is highest exactly when the coin is completely fair.

## Isomorphisms

-

## Open Questions

- [ ]

---

## Links

**Related:** [Von Neumann Entropy](Von%20Neumann%20Entropy.md), [Holevo Bound](Holevo%20Bound.md)
**Full Derivation:**
