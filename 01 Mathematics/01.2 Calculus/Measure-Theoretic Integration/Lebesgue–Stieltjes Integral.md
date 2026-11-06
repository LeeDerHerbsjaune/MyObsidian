---
type: technical-term
title: "Lebesgue–Stieltjes Integral"
aliases:
  - Lebesgue Stieltjes Integration
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
  - "Billingsley (1995), Probability and Measure"
related: []
projects: []
---

> [!abstract] Definition
> The **Lebesgue–Stieltjes integral** is an integration framework in which integration is performed with respect to a measure induced by a nondecreasing function.
>
> It generalizes integration with respect to ordinary length and provides a mathematical foundation for distribution functions and probability measures on the real line.

## 1. Stieltjes Measures

> [!definition] Lebesgue–Stieltjes Measure
> Let $F:\mathbb{R}\rightarrow\mathbb{R}$ be nondecreasing and right-continuous.
>
> There exists a unique Borel measure $\mu_F$, finite on bounded intervals, satisfying:
>
> $$\mu_F((a,b])=F(b)-F(a)$$
>
> This measure is called the Lebesgue–Stieltjes measure associated with $F$.

## 2. Lebesgue–Stieltjes Integral

> [!definition] Integral with Respect to a Stieltjes Measure
> For a measurable function $f$:
>
> $$\int_{\mathbb{R}}f(x)\,dF(x)
> :=
> \int_{\mathbb{R}}f\,d\mu_F$$
>
> The notation $dF$ represents integration with respect to the measure induced by $F$, not necessarily ordinary differentiation.

## 3. Important Cases

> [!example] Lebesgue Measure
> If $F(x)=x$, then:
>
> $$\mu_F((a,b])=b-a$$
>
> and the integral becomes ordinary Lebesgue integration with respect to length measure.

> [!example] Point Mass
> A jump discontinuity in $F$ creates an atom in the associated measure.
>
> For a unit jump at $x_0$, the corresponding measure includes:
>
> $$\delta_{x_0}$$
>
> Integration against this point mass evaluates a function at $x_0$.

## 4. Integration by Parts

> [!important] Stieltjes Integration by Parts
> Under suitable hypotheses:
>
> $$\int_{(a,b]} f\,dF+\int_{(a,b]}F(x-)\,df(x)
> =
> f(b)F(b)-f(a)F(a)$$
>
> Endpoint conventions and continuity assumptions matter when either function has jumps.

## 5. Applications

> [!info] Distribution Functions
> If $F$ is a cumulative distribution function, it induces a probability measure:
>
> $$P((a,b])=F(b)-F(a)$$
>
> Expectations can then be expressed as:
>
> $$\mathbb{E}[g(X)]=\int_{\mathbb{R}}g(x)\,dF(x)$$
>
> This representation includes both continuous and discrete distributions.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — provides the measure-theoretic framework.
> - **Lebesgue Integral** — provides the general integration construction.
> - **Monotone Functions** — supplies the generating functions for Stieltjes measures.

> [!note] Downstream Knowledge
> - **Probability Theory** — uses distribution functions and expectations.
> - **Random Variables** — uses integration with respect to probability distributions.
> - **Signed Measures** — generalizes beyond nonnegative measures.