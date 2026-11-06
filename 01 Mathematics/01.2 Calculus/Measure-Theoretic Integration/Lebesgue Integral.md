---
type: technical-term
title: "Lebesgue Integral"
aliases:
  - Lebesgue Integration
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
  - integration
sources:
  - "Folland (1999), Real Analysis"
  - "Royden & Fitzpatrick (2010), Real Analysis"
  - "Stein & Shakarchi (2005), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> The **Lebesgue integral** is an integral defined using measure theory. It extends the classical Riemann integral by integrating measurable functions over measurable spaces.
>
> Its construction proceeds from simple functions and uses supremums, positive and negative parts, and measure-theoretic convergence.

## 1. Integral of Nonnegative Functions

> [!definition] Lebesgue Integral
> Let $f:X\rightarrow[0,\infty]$ be measurable on $(X,\mathcal{F},\mu)$.
>
> Define:
>
> $$\int_X f\,d\mu
> =
> \sup_{\substack{0\leq\phi\leq f\\\phi\text{ simple}}}
> \int_X\phi\,d\mu$$
>
> The integral may be infinite.

## 2. Integral of General Functions

> [!definition] Positive and Negative Parts
> For a measurable real-valued function:
>
> $$f^+=\max(f,0),\qquad f^-=\max(-f,0)$$
>
> Thus:
>
> $$f=f^+-f^-$$
>
> If at least one of $\int f^+\,d\mu$ and $\int f^-\,d\mu$ is finite, the integral can be defined as an extended real number.
>
> If both are finite, $f$ is integrable and:
>
> $$\int_Xf\,d\mu
> =
> \int_Xf^+\,d\mu-\int_Xf^-\,d\mu$$
>
> If both are infinite, the expression is undefined.

## 3. Absolute Integrability

> [!definition] Lebesgue Integrability
> A measurable real-valued function is integrable if:
>
> $$\int_X|f|\,d\mu<\infty$$
>
> Equivalently:
>
> $$\int_Xf^+\,d\mu<\infty,\qquad
> \int_Xf^-\,d\mu<\infty$$

## 4. Fundamental Properties

> [!important] Linearity
> $$\int_X(af+bg)\,d\mu
> =a\int_Xf\,d\mu+b\int_Xg\,d\mu$$
>
> for integrable $f,g$ and scalars $a,b$.

> [!important] Monotonicity
> If $f\leq g$ almost everywhere and both functions are integrable, then:
>
> $$\int_Xf\,d\mu\leq\int_Xg\,d\mu$$

> [!important] Absolute Value Inequality
> $$\left|\int_Xf\,d\mu\right|
> \leq\int_X|f|\,d\mu$$

> [!important] Almost-Everywhere Invariance
> If $f=g$ almost everywhere, then their integrals are equal whenever defined.

## 5. Integration over Measurable Subsets

> [!definition] Integral over a Set
> For a measurable set $A$:
>
> $$\int_Af\,d\mu
> =
> \int_Xf\mathbf{1}_A\,d\mu$$

## 6. Relationship to Riemann Integration

> [!important] Comparison
> If $f$ is bounded on a compact interval, then it is Riemann integrable if and only if its set of discontinuities has Lebesgue measure zero.
>
> In this case, the Riemann and Lebesgue integrals agree.
>
> Lebesgue integration also accommodates many unbounded functions and functions with discontinuities too irregular for Riemann integration.

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — provides the integration domain and measure.
> - **Measurable Functions** — supplies the admissible functions.
> - **Simple Functions** — provides the construction from which the integral is defined.

> [!note] Downstream Knowledge
> - **Integrable Functions** — studies the class of functions with finite absolute integral.
> - **Convergence Theorems** — establishes conditions for exchanging limits and integrals.
> - **Product Measures** — extends integration to product spaces.
> - **$L^p$ Spaces** — uses Lebesgue integration to define function-space norms.