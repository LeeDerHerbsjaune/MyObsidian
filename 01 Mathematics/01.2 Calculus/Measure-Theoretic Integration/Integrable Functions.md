---
type: technical-term
title: "Integrable Functions"
aliases:
  - Lebesgue Integrable Functions
  - Absolutely Integrable Functions
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
related: []
projects: []
---

> [!abstract] Definition
> An **integrable function** is a measurable function whose absolute value has a finite Lebesgue integral.
>
> Integrability ensures that the function has a finite, well-defined integral and is the central membership condition for the space $L^1$.

## 1. Formal Definition

> [!definition] Lebesgue Integrability
> Let $f:X\rightarrow\mathbb{R}$ be measurable on a measure space $(X,\mathcal{F},\mu)$.
>
> The function $f$ is integrable if:
>
> $$\int_X|f|\,d\mu<\infty$$
>
> The space of integrable functions is denoted:
>
> $$L^1(X,\mu)$$
>
> Strictly, $L^1(X,\mu)$ consists of equivalence classes of integrable functions, where functions equal almost everywhere are identified.

## 2. Positive and Negative Parts

> [!definition] Decomposition
> Define:
>
> $$f^+=\max(f,0),\qquad f^-=\max(-f,0)$$
>
> Then:
>
> $$f=f^+-f^-$$
>
> $$|f|=f^++f^-$$
>
> A measurable function is integrable precisely when both positive and negative parts have finite integrals.

## 3. Fundamental Properties

> [!important] Algebraic Closure
> If $f,g\in L^1(X,\mu)$ and $a,b\in\mathbb{R}$, then:
>
> $$af+bg\in L^1(X,\mu)$$

> [!important] Integral Inequality
> $$\left|\int_Xf\,d\mu\right|
> \leq\int_X|f|\,d\mu$$

> [!important] Almost-Everywhere Equivalence
> If $f=g$ almost everywhere, then:
>
> $$\int_Xf\,d\mu=\int_Xg\,d\mu$$
>
> Thus, integrability and the integral depend only on the almost-everywhere equivalence class.

## 4. Integrability and $L^p$ Spaces

> [!definition] $L^p$ Integrability
> For $1\leq p<\infty$:
>
> $$L^p(X,\mu)=
> \left\{
> f:\int_X|f|^p\,d\mu<\infty
> \right\}$$
>
> Functions are identified when equal almost everywhere.
>
> The corresponding norm is:
>
> $$\|f\|_p=
> \left(\int_X|f|^p\,d\mu\right)^{1/p}$$
>
> For $p=\infty$, essential boundedness defines $L^\infty$.

## 5. Important Integrability Theorems

> [!theorem] Hölder's Inequality
> If $1<p,q<\infty$ and $1/p+1/q=1$, then:
>
> $$\int_X|fg|\,d\mu
> \leq\|f\|_p\|g\|_q$$

> [!theorem] Minkowski's Inequality
> For $p\geq1$:
>
> $$\|f+g\|_p\leq\|f\|_p+\|g\|_p$$

> [!theorem] Cauchy–Schwarz Inequality
> For square-integrable functions:
>
> $$\left|\int_Xfg\,d\mu\right|
> \leq
> \left(\int_X|f|^2d\mu\right)^{1/2}
> \left(\int_X|g|^2d\mu\right)^{1/2}$$

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Lebesgue Integral** — defines the integral used to determine integrability.
> - **Measurable Functions** — provides the required measurability condition.
> - **Measure Spaces** — provides the underlying measure.

> [!note] Downstream Knowledge
> - **$L^p$ Spaces** — develops integrable functions into normed function spaces.
> - **Functional Analysis** — studies the structure and operators of these spaces.
> - **Fourier Analysis** — uses integrability conditions to define and study transforms.