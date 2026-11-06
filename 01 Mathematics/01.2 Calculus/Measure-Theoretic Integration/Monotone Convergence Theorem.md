---
type: technical-term
title: "Monotone Convergence Theorem"
aliases:
  - Beppo Levi Theorem
  - MCT
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
> The **Monotone Convergence Theorem (MCT)** states that the integral of an increasing sequence of nonnegative measurable functions converges to the integral of its pointwise limit.
>
> It is a fundamental theorem that justifies exchanging an increasing limit and a Lebesgue integral.

## 1. Formal Statement

> [!theorem] Monotone Convergence Theorem
> Let $(X,\mathcal{F},\mu)$ be a measure space.
>
> Suppose $(f_n)$ is a sequence of nonnegative measurable functions satisfying:
>
> $$0\leq f_1(x)\leq f_2(x)\leq\cdots$$
>
> and:
>
> $$f_n(x)\rightarrow f(x)$$
>
> Then:
>
> $$\boxed{
> \lim_{n\rightarrow\infty}\int_Xf_n\,d\mu
> =
> \int_Xf\,d\mu
> }$$
>
> Both sides may be infinite.

## 2. Interpretation

> [!important] Increasing Approximation
> Each $f_n$ approximates the limiting function from below.
>
> As the sequence increases, the integrals cannot decrease. The theorem guarantees that their limit equals the integral of the pointwise limit.

## 3. Important Conditions

> [!warning] Hypotheses
> - Each $f_n$ must be measurable.
> - Each $f_n$ must be nonnegative.
> - The sequence must increase pointwise.
> - The pointwise limit must be measurable; this follows from the assumptions.
>
> No finite-measure assumption on $X$ is required.

## 4. Consequences

> [!important] Integration of Increasing Simple Functions
> The Lebesgue integral of a nonnegative measurable function can be constructed through an increasing sequence of simple functions.
>
> The monotone convergence theorem guarantees that the integrals of these approximations converge to the intended integral.

> [!important] Series of Nonnegative Functions
> If $f_n\geq0$, then:
>
> $$\int_X\sum_{n=1}^{\infty}f_n\,d\mu
> =
> \sum_{n=1}^{\infty}\int_Xf_n\,d\mu$$
>
> This follows by applying the theorem to the partial sums.

## 5. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Lebesgue Integral** — defines the integrals being compared.
> - **Measurable Functions** — provides the measurable sequence.
> - **Almost-Everywhere Convergence** — provides a related convergence framework.

> [!note] Downstream Knowledge
> - **Fatou's Lemma** — can be derived using monotone convergence.
> - **Dominated Convergence Theorem** — uses related approximation and convergence arguments.
> - **Integration of Series** — applies the theorem to nonnegative partial sums.