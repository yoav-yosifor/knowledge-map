---
tags:
  - nanophotonics
  - derivation
---
---
## Statement of Result

The two independent families of guided-mode solutions — symmetric (even) and antisymmetric (odd), about the slab's center — that the general TE characteristic equation splits into when the slab is symmetric ($n_1=n_3$), plus the even family's explicit field profile and the graphical (V-number) method used to find each family's propagation constants.

## Starting Point

- The general (asymmetric) characteristic equation from [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md):
  $$
  \tan(hd)=\frac{h\cdot(p+q)}{h^2-pq}
  $$
  with $q=\sqrt{\beta^2-n_1^2k_0^2}$, $p=\sqrt{\beta^2-n_3^2k_0^2}$, $h=\sqrt{n_2^2k_0^2-\beta^2}$ (cladding index $n_1$, core index $n_2$, substrate index $n_3$; $x=0$ is the substrate interface, $x=d$ the cladding interface).
- Symmetric-slab condition: $n_1=n_3\Rightarrow p=q$.
- Trigonometric identity: $\tan(2x)=\dfrac{2\tan x}{1-\tan^2x}$.

## Full Derivation

1. **Set $p=q$ in the general characteristic equation.**

   $$
   \tan(hd)=\frac{2ph}{h^2-p^2}
   $$

   This is the general equation from the Starting Point specialized to $p=q$ — still a single equation covering all modes together.

2. **Apply the double-angle identity, treating $hd$ as $2\cdot(hd/2)$.**

   $$
   \tan(hd)=\frac{2\tan(hd/2)}{1-\tan^2(hd/2)}
   $$

   This rewrites the left side purely in terms of $\tan(hd/2)$, so it can be compared term-by-term against the right side of step 1.

3. **Equate the two expressions and simplify by substituting $\tan(hd/2)\to p/h$, then $\to -h/p$.**

   $$
   \frac{2\tan(hd/2)}{1-\tan^2(hd/2)}=\frac{2ph}{h^2-p^2}=\frac{2p/h}{1-(p/h)^2}=-\frac{2h/p}{1-(h/p)^2}
   $$

   Matching numerator-to-numerator and denominator-to-denominator against the two rightmost forms gives two independent ways to satisfy the equation: $\tan(hd/2)=p/h$, or $\tan(hd/2)=-h/p$ (equivalently $\cot(hd/2)=-p/h$). Since $\tan(hd/2)$ can only equal one number at a time, these are two separate solution families, not two conditions to satisfy simultaneously.

4. **State the two families in plotting-friendly form.**

   $$
   \tfrac12hd\cdot\tan(\tfrac12hd)=\tfrac12pd \qquad\text{(family 1)}
   $$

   $$
   \tfrac12hd\cdot\cot(\tfrac12hd)=-\tfrac12pd \qquad\text{(family 2)}
   $$

   Multiplying both sides of $\tan(hd/2)=p/h$ by $\tfrac12hd$ gives family 1; the same step applied to $\cot(hd/2)=-p/h$ gives family 2.

5. **Identify the field profile of family 1.**

   $$
   E_y(x)=\begin{cases}
   ae^{-p(x-d/2)} & x>d\\[2pt]
   ae^{-pd/2}\dfrac{\cos(h(x-d/2))}{\cos(hd/2)} & 0<x<d\\[2pt]
   ae^{p(x-d/2)} & x<0
   \end{cases}
   $$

   This is a symmetric (even) profile centered at $d/2$ — the cosine core profile and matching exponential tails are mirror images of each other about the slab's center.

6. **Identify family 2's profile qualitatively.**

   The second family gives an antisymmetric (odd) profile, also centered at $d/2$: the core field changes sign across the center, with the two exponential tails matching that opposite sign on each side. (No explicit piecewise formula for this profile was given in the source — only the field profile plot.)

7. **Solve each family graphically.**

   Each family can have multiple solutions depending on the specific $n_1,n_2,d,\lambda$. Plotting $pd$ vs. $hd$, both families share a common bounding curve:

   $$
   \left(\tfrac12hd\right)^2+\left(\tfrac12pd\right)^2=\tfrac14d^2k_0^2\left(n_2^2-n_1^2\right)=\left(\tfrac12V\right)^2, \qquad V=k_0d\sqrt{n_{co}^2-n_{cl}^2}
   $$

   Successive mode branches, labeled TE0, TE1, TE2, $\dots$, are the crossings of this curve with family 1 ($\tan$) and family 2 ($\cot$) alternately — TE0 with family 1, TE1 with family 2, TE2 with family 1, and so on.

## Result

$$
\tfrac12hd\cdot\tan(\tfrac12hd)=\tfrac12pd \qquad\text{(even family)}, \qquad
\tfrac12hd\cdot\cot(\tfrac12hd)=-\tfrac12pd \qquad\text{(odd family)}
$$

## Where It's Used

**Concept:** [Slab Waveguide Modes](Slab%20Waveguide%20Modes.md)

---

## Links

**Related:** [Slab Waveguide Mode Derivation](Slab%20Waveguide%20Mode%20Derivation.md) (general asymmetric case this specializes), [Guided Mode Count Derivation](Guided%20Mode%20Count%20Derivation.md)
