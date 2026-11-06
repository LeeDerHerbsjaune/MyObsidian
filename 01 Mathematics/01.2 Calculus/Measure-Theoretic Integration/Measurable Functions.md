---
type: technical-term
title: "Measurable Functions"
aliases:
  - Measurable Mapping
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
  - "Royden & Fitzpatrick (2010), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> A **measurable function** is a function between measurable spaces whose preimages of measurable sets are measurable.
>
> Measurability is the central condition that permits functions to be integrated using measure theory.

## 1. Formal Definition

> [!definition] Measurable Mapping
> Let $(X,\mathcal{F})$ and $(Y,\mathcal{G})$ be measurable spaces.
>
> A function $f:X\rightarrow Y$ is measurable if:
>
> $$f^{-1}(B)\in\mathcal{F}$$
>
> for every $B\in\mathcal{G}$.

## 2. Real-Valued Measurable Functions

> [!important] Equivalent Criterion
> For a real-valued function $f:X\rightarrow\mathbb{R}$, measurability is equivalent to requiring:
>
> $$\{x\in X:f(x)>a\}\in\mathcal{F}$$
>
> for every $a\in\mathbb{R}$.
>
> Equivalent criteria can use strict or non-strict inequalities and rational thresholds.

## 3. Operations on Measurable Functions

> [!important] Closure Properties
> If $f$ and $g$ are real-valued measurable functions, then the following are measurable:
>
> - $f+g$.
> - $fg$.
> - $cf$, for a constant $c$.
> - $\max(f,g)$ and $\min(f,g)$.
> - $|f|$.
> - $\sup_n f_n$ and $\inf_n f_n$ for countable families.
> - $\limsup f_n$ and $\liminf f_n$.
>
> If $g$ is continuous, then $g\circ f$ is measurable whenever the composition is defined.

## 4. Pointwise Limits

> [!theorem] Measurability of Pointwise Limits
> If a sequence of measurable real-valued functions converges pointwise to $f$, then $f$ is measurable.
>
> More generally, pointwise limits of measurable functions are measurable wherever the limit exists, with suitable extended-real conventions.

## 5. Indicator Functions

> [!definition] Indicator Function
> For a measurable set $A$:
>
> $$\mathbf{1}_A(x)=
> \begin{cases}
> 1,&x\in A\\
> 0,&x\notin A
> \end{cases}$$
>
> The indicator function $\mathbf{1}_A$ is measurable if and only if $A$ is measurable.

## 6. Simple and Measurable Functions

> [!important] Approximation Principle
> Every nonnegative measurable function is the pointwise increasing limit of a sequence of nonnegative measurable simple functions.
>
> This approximation is fundamental to the construction of the Lebesgue integral.

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — defines the measurable domain and codomain.
> - **Measurable Sets** — provides the sets whose preimages must be measurable.

> [!note] Downstream Knowledge
> - **Simple Functions** — uses finite-valued measurable functions.
> - **Lebesgue Integral** — requires measurable functions for integration.
> - **Almost-Everywhere Convergence** — studies limits outside null sets.