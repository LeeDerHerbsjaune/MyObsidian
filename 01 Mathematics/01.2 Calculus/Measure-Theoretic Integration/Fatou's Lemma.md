---
type: technical-term
title: "Fatou's Lemma"
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
  - convergence-theorems
sources:
  - "Folland (1999), Real Analysis"
  - "Royden & Fitzpatrick (2010), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> **Fatou's Lemma** provides an inequality relating the integral of the pointwise lower limit of a sequence of nonnegative measurable functions to the lower limit of their integrals.
>
> It is a fundamental tool in proving convergence results in measure theory.

## 1. Formal Statement

> [!theorem] Fatou's Lemma
> Let $(f_n)$ be a sequence of nonnegative measurable functions on a measure space $(X,\mathcal{F},\mu)$.
>
> Then:
>
> $$\boxed{
> \int_X\liminf_{n\rightarrow\infty}f_n\,d\mu
> \leq
> \liminf_{n\rightarrow\infty}
> \int_Xf_n\,d\mu
> }$$

## 2. Pointwise Lower Limit

> [!definition] Limit Inferior
> The pointwise limit inferior is:
>
> $$\liminf_{n\rightarrow\infty}f_n(x)
> =
> \sup_{n\geq1}\inf_{k\geq n}f_k(x)$$
>
> It describes the eventual lower behavior of the sequence at each point.

## 3. Interpretation

> [!important] Integral Inequality
> The integral of the limiting lower envelope cannot exceed the lower limit of the sequence of integrals.
>
> Equality is not guaranteed.

## 4. Important Conditions

> [!warning] Hypotheses
> - Each $f_n$ must be measurable.
> - Each $f_n$ must be nonnegative.
> - The measure space need not have finite total measure.
>
> The theorem also applies to functions bounded below by a common integrable function after subtracting that lower bound.

## 5. Relationship to Other Theorems

> [!important] Monotone Convergence
> Fatou's lemma can be derived from the Monotone Convergence Theorem by considering the increasing sequence:
>
> $$g_n=\inf_{k\geq n}f_k$$

> [!important] Dominated Convergence
> Fatou's lemma is a key ingredient in the proof of the Dominated Convergence Theorem.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Lebesgue Integral** — provides the integral operation.
> - **Measurable Functions** — supplies the measurable sequence.
> - **Monotone Convergence Theorem** — provides a central result used in its proof.

> [!note] Downstream Knowledge
> - **Dominated Convergence Theorem** — uses Fatou's lemma in its proof.
> - **Lower Semicontinuity of Integral Functionals** — uses related lower-limit inequalities.