---
type: technical-term
title: "Tonelli's Theorem"
aliases: []
field:
  - Mathematics
subfield:
  - Measure Theory
  - Integration Theory
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - measure-theory
  - product-integration
sources:
  - "Folland (1999), Real Analysis"
  - "Royden & Fitzpatrick (2010), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> **Tonelli's Theorem** states that a nonnegative measurable function on a product measure space can be integrated through iterated integration, and the order of integration can be exchanged.
>
> The theorem does not require the integral to be finite.

## 1. Formal Statement

> [!theorem] Tonelli's Theorem
> Let $(X,\mathcal{F},\mu)$ and $(Y,\mathcal{G},\nu)$ be σ-finite measure spaces.
>
> If $f:X\times Y\rightarrow[0,\infty]$ is measurable with respect to the product σ-algebra, then:
>
> $$\boxed{
> \int_{X\times Y}f\,d(\mu\times\nu)
> =
> \int_X\left(\int_Yf(x,y)\,d\nu(y)\right)d\mu(x)
> }$$
>
> The order of integration may be reversed:
>
> $$=
> \int_Y\left(\int_Xf(x,y)\,d\mu(x)\right)d\nu(y)$$
>
> The common value may be infinite.

## 2. Interpretation

> [!important] Nonnegative Integration
> Tonelli's theorem allows a nonnegative function to be integrated one variable at a time.
>
> Since the integrand is nonnegative, cancellation between positive and negative contributions cannot create an undefined difference of infinities.

## 3. Important Conditions

> [!warning] Hypotheses
> - The factor measure spaces are σ-finite.
> - The function is product-measurable.
> - The function is nonnegative.
>
> The integral need not be finite.

## 4. Relationship to Fubini's Theorem

> [!important] Distinction
> - **Tonelli's Theorem:** nonnegative measurable functions; infinite integrals are allowed.
> - **Fubini's Theorem:** absolutely integrable functions; the integral is finite and iterated integration is valid almost everywhere.
>
> Tonelli's theorem can be used to establish absolute integrability by applying it to $|f|$.

## 5. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Product Measures** — defines the measure on the product space.
> - **Measurable Functions** — provides the measurability condition.
> - **Lebesgue Integral** — defines the integral.

> [!note] Downstream Knowledge
> - **Fubini's Theorem** — extends iterated integration to absolutely integrable functions.
> - **Multiple Integration** — provides a measure-theoretic foundation for repeated integration.
> - **Probability Theory** — supports calculations involving joint distributions.