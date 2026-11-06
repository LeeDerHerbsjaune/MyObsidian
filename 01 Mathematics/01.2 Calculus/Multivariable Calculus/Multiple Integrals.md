---
type: technical-term
title: "Multiple Integrals"
aliases:
  - Multidimensional Integrals
  - Double and Triple Integrals
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Mathematical Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - multivariable-calculus
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Multiple Integrals** generalize definite integration to functions defined over multidimensional domains.
>
> They calculate accumulated quantities over regions in two or more dimensions.

## 1. Double Integrals

> [!definition] Double Integral
> For a function $f(x,y)$ defined over a region $D\subseteq\mathbb R^2$:
>
> $$\iint_D f(x,y)\,dA$$
>
> A double integral accumulates the function over a two-dimensional domain.

> [!note] Rectangular Regions
> For a rectangular region:
>
> $$D=[a,b]\times[c,d]$$
>
> an iterated integral can be written as:
>
> $$\int_a^b\int_c^d
> f(x,y)\,dy\,dx$$
>
> Under appropriate integrability conditions, the order of integration can be exchanged.

## 2. Triple Integrals

> [!definition] Triple Integral
> For a function defined over a three-dimensional region $E$:
>
> $$\iiint_E f(x,y,z)\,dV$$
>
> It accumulates the function over a volume.

## 3. Fubini's Theorem

> [!important] Fubini's Theorem
> Under appropriate conditions, including integrability on the product domain, a multiple integral can be evaluated as an iterated integral.
>
> For an integrable function on a rectangular domain:
>
> $$\iint_D f(x,y)\,dA
> =
> \int_a^b\left(
> \int_c^d f(x,y)\,dy
> \right)dx$$
>
> The theorem provides the theoretical basis for changing the order of integration.

## 4. Geometric and Physical Interpretations

> [!note] Volume
> If $f(x,y)\geq0$, then:
>
> $$\iint_D f(x,y)\,dA$$
>
> represents the volume under the surface $z=f(x,y)$ over $D$.

> [!note] Mass
> For a lamina with surface density $\rho(x,y)$:
>
> $$m=\iint_D\rho(x,y)\,dA$$

> [!note] Higher-Dimensional Accumulation
> Multiple integrals can represent mass, charge, probability, and other accumulated quantities.

## 5. Integration Domains

> [!note] Type I and Type II Regions
> A planar region may be described using vertically or horizontally bounded intervals.
>
> Type I:
>
> $$a\leq x\leq b,\qquad
> g_1(x)\leq y\leq g_2(x)$$
>
> Type II:
>
> $$c\leq y\leq d,\qquad
> h_1(y)\leq x\leq h_2(y)$$
>
> Choosing a suitable description can simplify integration.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Definite Integrals:** Provides the underlying concept of accumulation.
- **Functions of Several Variables:** Defines the integrands.
- **Limits and Continuity:** Supports integration theory.
- **Coordinate Systems:** Describes multidimensional domains.

### Downstream Knowledge
- **Change of Variables:** Transforms integration coordinates.
- **Vector Calculus:** Develops line, surface, and volume integrals.
- **Probability Theory:** Uses multiple integration for joint probability distributions.