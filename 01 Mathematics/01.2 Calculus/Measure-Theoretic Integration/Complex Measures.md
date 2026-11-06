---
type: technical-term
title: "Complex Measures"
aliases:
  - Complex Measure
field:
  - Mathematics
subfield:
  - Measure Theory
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - measure-theory
sources:
  - "Folland (1999), Real Analysis"
  - "Rudin (1987), Real and Complex Analysis"
related: []
projects: []
---

> [!abstract] Definition
> A **complex measure** is a countably additive set function whose values are complex numbers.
>
> It generalizes positive and signed measures and provides a measure-theoretic framework for complex-valued integration.

## 1. Formal Definition

> [!definition] Complex Measure
> Let $(X,\mathcal{F})$ be a measurable space.
>
> A complex measure is a function:
>
> $$\nu:\mathcal{F}\rightarrow\mathbb{C}$$
>
> satisfying:
>
> $$\nu\left(\bigcup_{n=1}^{\infty}A_n\right)
> =
> \sum_{n=1}^{\infty}\nu(A_n)$$
>
> for pairwise disjoint measurable sets $A_n$, where the series converges appropriately.
>
> In the standard theory of finite complex measures, the associated total variation is finite.

## 2. Real and Imaginary Components

> [!important] Decomposition
> Every complex measure can be expressed as:
>
> $$\nu=\nu_1+i\nu_2$$
>
> where:
> - $\nu_1$ is a finite signed measure.
> - $\nu_2$ is a finite signed measure.
>
> Thus, complex measure theory extends signed measure theory through complex-valued combinations.

## 3. Total Variation

> [!definition] Total Variation
> For $A\in\mathcal{F}$:
>
> $$|\nu|(A)
> =
> \sup_{\{A_i\}}
> \sum_i|\nu(A_i)|$$
>
> where the supremum is taken over finite measurable partitions of $A$.
>
> A complex measure is finite if:
>
> $$|\nu|(X)<\infty$$

## 4. Integration

> [!definition] Complex-Valued Integral
> If $f$ is integrable with respect to the total variation measure, define:
>
> $$\int_Xf\,d\nu
> =
> \int_Xf\,d\nu_1
> +
> i\int_Xf\,d\nu_2$$
>
> A sufficient and standard condition is:
>
> $$\int_X|f|\,d|\nu|<\infty$$

## 5. Integral Inequality

> [!important] Variation Bound
> For integrable $f$:
>
> $$\left|\int_Xf\,d\nu\right|
> \leq\int_X|f|\,d|\nu|$$
>
> This inequality generalizes the absolute-value bound for integration with respect to positive measures.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — supplies the measurable domain.
> - **Signed Measures** — provides the real-valued generalization.
> - **Lebesgue Integral** — supplies the integration framework.

> [!note] Downstream Knowledge
> - **Complex Analysis** — uses integration of complex-valued functions.
> - **Fourier Analysis** — uses complex measures in generalized transform theory.
> - **Spectral Theory** — uses complex measures in spectral representations.