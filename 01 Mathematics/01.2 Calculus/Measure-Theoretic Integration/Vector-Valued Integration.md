---
type: technical-term
title: "Vector-Valued Integration"
aliases:
  - Integration of Vector-Valued Functions
  - Bochner Integration
field:
  - Mathematics
subfield:
  - Measure Theory
  - Functional Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - measure-theory
  - functional-analysis
sources:
  - "Diestel & Uhl (1977), Vector Measures"
  - "Brezis (2011), Functional Analysis, Sobolev Spaces and Partial Differential Equations"
  - "Folland (1999), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> **Vector-Valued Integration** studies the integration of functions whose values belong to a vector space, particularly a Banach space.
>
> It generalizes scalar Lebesgue integration and provides a foundation for integration in functional analysis.

## 1. Vector-Valued Functions

> [!definition] Vector-Valued Function
> Let $(X,\mathcal{F},\mu)$ be a measure space and $B$ a Banach space.
>
> A vector-valued function is a mapping:
>
> $$f:X\rightarrow B$$
>
> Unlike scalar integration, the function values are vectors or elements of a potentially infinite-dimensional space.

## 2. Strong Measurability

> [!definition] Strong Measurability
> A function $f:X\rightarrow B$ is strongly measurable if it is the almost-everywhere pointwise limit of a sequence of measurable simple $B$-valued functions.
>
> This condition ensures that the function can be approximated using finite-valued vector functions.

## 3. Bochner Integral

> [!definition] Bochner Integrability
> A strongly measurable function $f:X\rightarrow B$ is Bochner integrable if:
>
> $$\int_X\|f(x)\|_B\,d\mu(x)<\infty$$
>
> Its integral is constructed as the limit of integrals of approximating simple functions.

> [!important] Bochner Integral
> For a simple vector-valued function:
>
> $$\phi(x)=\sum_{i=1}^{n}b_i\mathbf{1}_{A_i}(x)$$
>
> its integral is:
>
> $$\int_X\phi\,d\mu
> =
> \sum_{i=1}^{n}b_i\mu(A_i)$$
>
> For a general Bochner-integrable function, the integral is defined by approximation in the norm of $B$.

## 4. Fundamental Properties

> [!important] Linearity
> $$\int_X(af+bg)\,d\mu
> =
> a\int_Xf\,d\mu+b\int_Xg\,d\mu$$

> [!important] Norm Inequality
> $$\left\|\int_Xf\,d\mu\right\|_B
> \leq\int_X\|f(x)\|_B\,d\mu(x)$$

> [!important] Bounded Linear Operators
> If $T:B\rightarrow C$ is a bounded linear operator between Banach spaces, then:
>
> $$T\left(\int_Xf\,d\mu\right)
> =
> \int_XT(f(x))\,d\mu(x)$$
>
> whenever $f$ is Bochner integrable.

## 5. Bochner and Pettis Integration

> [!important] Distinction
> - **Bochner Integration:** requires strong measurability and integrability of the norm.
> - **Pettis Integration:** uses weak measurability and the existence of suitable scalar integrals against continuous linear functionals.
>
> Pettis integrability is generally weaker than Bochner integrability.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Lebesgue Integral** — provides the scalar integration framework.
> - **Measure Spaces** — provides the underlying measure.
> - **Banach Spaces** — supplies the complete normed vector spaces in which integration takes place.
> - **Strong Measurability** — provides the approximation condition for Bochner integration.

> [!note] Downstream Knowledge
> - **Functional Analysis** — studies vector-valued function spaces and bounded operators.
> - **Vector Measures** — develops measure theory with vector-valued set functions.
> - **Evolution Equations** — uses vector-valued integrals in infinite-dimensional solution frameworks.
> - **Stochastic Integration** — develops integration of stochastic processes, including infinite-dimensional settings.