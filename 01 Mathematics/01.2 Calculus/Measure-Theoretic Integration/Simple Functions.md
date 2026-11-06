---
type: technical-term
title: "Simple Functions"
aliases:
  - Measurable Simple Functions
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
  - "Stein & Shakarchi (2005), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> A **simple function** is a measurable function that takes only finitely many distinct values.
>
> Simple functions form the elementary building blocks used to construct the Lebesgue integral.

## 1. Formal Definition

> [!definition] Nonnegative Simple Function
> A nonnegative simple function can be represented as:
>
> $$\phi(x)=\sum_{i=1}^{n}a_i\mathbf{1}_{A_i}(x)$$
>
> where:
> - $a_i\geq0$ are constants.
> - $A_i$ are measurable sets.
> - $\mathbf{1}_{A_i}$ are indicator functions.
>
> The sets can be chosen pairwise disjoint.

## 2. Integration of Simple Functions

> [!definition] Simple-Function Integral
> For pairwise disjoint measurable sets:
>
> $$\int_X\phi\,d\mu
> =
> \sum_{i=1}^{n}a_i\mu(A_i)$$
>
> The integral is a finite weighted sum of the measures of the sets on which the function is constant.

## 3. Properties

> [!important] Basic Properties
> - Linearity holds for finite linear combinations.
> - If $0\leq\phi\leq\psi$, then $\int\phi\,d\mu\leq\int\psi\,d\mu$.
> - If $\phi_n\uparrow\phi$, then the integrals converge increasingly under the monotone convergence framework.
> - A nonnegative measurable function can be approximated from below by simple functions.

## 4. Approximation of Measurable Functions

> [!theorem] Simple-Function Approximation
> If $f:X\rightarrow[0,\infty]$ is measurable, there exists a sequence of nonnegative simple functions $\phi_n$ such that:
>
> $$0\leq\phi_1\leq\phi_2\leq\cdots\leq f$$
>
> and:
>
> $$\phi_n(x)\rightarrow f(x)$$
>
> for every $x\in X$.
>
> This result makes it possible to define the integral of general nonnegative measurable functions.

## 5. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measurable Sets** — defines the measurable subsets used in indicator functions.
> - **Measurable Functions** — establishes the measurability required of simple functions.
> - **Measure Spaces** — provides the measure used in integration.

> [!note] Downstream Knowledge
> - **Lebesgue Integral** — extends integration from simple functions to general measurable functions.