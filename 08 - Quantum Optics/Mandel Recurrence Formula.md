---
tags:
  - quantum-optics
  - derivation
---
---
## Statement of Result

The exact probability $P_m(t,T)$ of observing exactly $m$ photodetection events in a window $[t,t+T]$ for a classical field. The derivation starts from a single probabilistic assumption about the click rate, and shows the result reduces to a [Poisson distribution](Poisson%20Photocount%20Statistics.md) when the intensity is constant.

## Starting Point

- The single founding assumption of semi-classical detection theory: the probability of a click in $(t,t+dt)$ is $p(t)\,dt=\zeta I(t)\,dt$, where $\zeta$ is the detector efficiency
- Boundary conditions $P_{-1}\equiv 0$ and $P_0(t,0)=1$ (no time has passed, so zero counts is certain)

## Full Derivation

1. Extend the counting window by an infinitesimal $dt$ and write $P_m(t,T+dt)$ as the sum of two mutually exclusive ways to reach $m$ counts: either $m-1$ counts were already present in $[t,t+T]$ and one new click occurs in $dt$, or $m$ counts were already present and no new click occurs. Since $dt$ is infinitesimal, no other combination is possible — at most one click can occur in an infinitesimal interval, so this exhausts all the ways of reaching $m$ counts by $T+dt$.

2. Rearrange $P_m(t,T+dt)-P_m(t,T) = p(t+T)\,dt\,[P_{m-1}(t,T)-P_m(t,T)]$ and divide by $dt$, using $p(t+T)=\zeta I(t+T)$, to get the differential recurrence:

   $$
   \frac{dP_m}{dT}=\zeta I(t+T)\,[P_{m-1}(t,T)-P_m(t,T)]
   $$

   Taking the $dt\to0$ limit converts the discrete two-term relation into an ordinary differential equation that ties the growth rate of each count-probability to the difference between it and the probability one level below — this is the Mandel recurrence itself.

3. Solve the $m=0$ case first, where $P_{-1}\equiv0$ makes the recurrence separable:

   $$
   \frac{dP_0}{dT}=-\zeta I(t+T)P_0
   $$

   integrating to:

   $$
   P_0(t,T)=\exp\left(-\zeta\int_t^{t+T}I(t')\,dt'\right)
   $$

   With no lower level to feed into it, $P_0$ obeys pure exponential decay — the probability of seeing zero clicks shrinks as more total energy is collected, exactly as expected for a rare-event process.

4. Solve the general-$m$ case by induction (or via a generating function), defining $x\equiv\zeta\bar I(t,T)\,T$ as the mean number of expected events, to get:

   $$
   P_m(t,T)=\frac{x^m}{m!}e^{-x}
   $$

   Each higher-$m$ probability is fed by the one directly below it through the same recurrence relation, and this cascading ladder structure is precisely what generates the Poisson form — it is not assumed, it falls out of the recurrence.

5. Confirm the interpretation of $x$ by computing the mean and second moment directly:

   $$
   \langle m\rangle=\sum_m m\,P_m = x, \qquad \langle m^2\rangle=x^2+x, \qquad \Delta m^2=\langle m\rangle=x
   $$

   This checks that $x$ is not just a bookkeeping parameter but literally the physically expected count, and that the variance equals the mean — the defining signature of shot noise.

## Result

$$
P_m(t,T) = \frac{x^m}{m!}\,e^{-x}, \qquad x = \zeta\,\bar I(t,T)\cdot T
$$

## Where It's Used

**Concept:** [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md)

---

## Links

**Related:** [Poisson Photocount Statistics](Poisson%20Photocount%20Statistics.md)
