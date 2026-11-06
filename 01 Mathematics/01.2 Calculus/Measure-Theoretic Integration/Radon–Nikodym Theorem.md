---
type: technical-term
title: "Radon–Nikodym Theorem"
aliases:
  - Radon Nikodym Theorem
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
sources:
  - "Folland (1999), Real Analysis"
  - "Royden & Fitzpatrick (2010), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> The **Radon–Nikodym Theorem** states that a measure absolutely continuous with respect to another σ-finite measure can be represented as integration against a measurable density function.
>
> It establishes a fundamental relationship between measures and integrable functions.

## 1. Absolute Continuity of Measures

> [!definition] Absolute Continuity
> Let $\nu$ and $\mu$ be measures on the same measurable space.
>
> The measure $\nu$ is absolutely continuous with respect to $\mu$ if:
>
> $$\mu(A)=0\implies\nu(A)=0$$
>
> for every measurable set $A$.
>
> This relationship is written:
>
> $$\nu\ll\mu$$

## 2. Formal Statement

> [!theorem] Radon–Nikodym Theorem
> Let $\mu$ and $\nu$ be σ-finite measures on the same measurable space.
>
> If:
>
> $$\nu\ll\mu$$
>
> then there exists a nonnegative measurable function $f$ such that:
>
> $$\boxed{
> \nu(A)=\int_Af\,d\mu
> }$$
>
> for every measurable set $A$.
>
> The function $f$ is unique up to equality almost everywhere.

## 3. Radon–Nikodym Derivative

> [!definition] Density
> The function $f$ is called the Radon–Nikodym derivative of $\nu$ with respect to $\mu$:
>
> $$f=\frac{d\nu}{d\mu}$$
>
> Thus:
>
> $$d\nu=f\,d\mu$$
>
> This notation expresses the measure $\nu$ through a density relative to $\mu$.

## 4. Change of Measure

> [!important] Integration Identity
> If $\nu\ll\mu$ and $f=d\nu/d\mu$, then for every nonnegative measurable function $g$:
>
> $$\int_Xg\,d\nu
> =
> \int_Xgf\,d\mu$$
>
> The identity also holds for integrable functions under the corresponding integrability conditions.

## 5. Examples

> [!example] Probability Density
> If a probability measure on $\mathbb{R}$ is absolutely continuous with respect to Lebesgue measure, then it has a density $p$:
>
> $$P(A)=\int_Ap(x)\,dx$$
>
> The density is the Radon–Nikodym derivative:
>
> $$p=\frac{dP}{dx}$$

## 6. Important Limitations

> [!warning] Absolute Continuity
> Not every measure has a density with respect to Lebesgue measure.
>
> For example, a Dirac measure is concentrated at a single point and is singular with respect to Lebesgue measure.
>
> The Radon–Nikodym theorem requires absolute continuity, not merely that two measures are defined on the same space.

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — provides the underlying measures.
> - **Lebesgue Integral** — provides integration against a measure.
> - **Absolute Continuity of Measures** — supplies the theorem's central hypothesis.

> [!note] Downstream Knowledge
> - **Lebesgue Decomposition Theorem** — decomposes measures into absolutely continuous and singular parts.
> - **Probability Density Functions** — represents absolutely continuous probability measures.
> - **Conditional Expectation** — uses a related Radon–Nikodym construction.