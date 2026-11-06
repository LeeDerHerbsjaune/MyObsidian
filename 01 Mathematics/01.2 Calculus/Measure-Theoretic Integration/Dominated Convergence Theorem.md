---
type: technical-term
title: "Dominated Convergence Theorem"
aliases:
  - DCT
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
> The **Dominated Convergence Theorem (DCT)** states that pointwise almost-everywhere convergence allows the limit to pass through the integral when the sequence is dominated by a single integrable function.
>
> It is one of the most frequently used results for exchanging limits and integration.

## 1. Formal Statement

> [!theorem] Dominated Convergence Theorem
> Let $(X,\mathcal{F},\mu)$ be a measure space.
>
> Suppose:
>
> 1. Each $f_n$ is measurable.
> 2. $f_n(x)\rightarrow f(x)$ almost everywhere.
> 3. There exists $g\in L^1(X,\mu)$ such that:
>
> $$|f_n(x)|\leq g(x)$$
>
> almost everywhere for every $n$.
>
> Then $f\in L^1(X,\mu)$ and:
>
> $$\boxed{
> \lim_{n\rightarrow\infty}\int_Xf_n\,d\mu
> =
> \int_Xf\,d\mu
> }$$

## 2. Dominating Function

> [!definition] Integrable Dominator
> The function $g$ is called a dominating function if it bounds the absolute values of every $f_n$ and is integrable:
>
> $$\int_Xg\,d\mu<\infty$$
>
> The same function must dominate the entire sequence, not merely each function separately with unrelated bounds.

## 3. Interpretation

> [!important] Limit and Integration
> Pointwise convergence alone does not generally justify exchanging limits and integrals.
>
> An integrable dominating function prevents excessive concentration or growth from invalidating the exchange.

## 4. Important Conditions

> [!warning] Hypotheses
> - Almost-everywhere convergence is required.
> - A common integrable dominating function is required.
> - The measure space need not have finite total measure.
>
> Uniform convergence is not required.

## 5. Common Applications

> [!example] Parameter-Dependent Integrals
> Suppose $f_n(x)$ converges pointwise to $f(x)$ and all terms satisfy a common integrable bound.
>
> The theorem allows:
>
> $$\lim_{n\rightarrow\infty}\int_Xf_n\,d\mu
> =
> \int_X\lim_{n\rightarrow\infty}f_n\,d\mu$$
>
> This is useful when proving continuity or convergence of parameter-dependent integrals.

## 6. Relationship to Other Theorems

> [!important] Fatou's Lemma
> Fatou's lemma provides the lower-limit inequality used to establish the DCT.

> [!important] Uniform Convergence
> On a finite measure space, uniform convergence of measurable functions with suitable boundedness conditions can imply convergence of integrals.
>
> The DCT is more general because it does not require uniform convergence.

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Lebesgue Integral** — defines the integral.
> - **Integrable Functions** — provides the integrability condition for the dominating function.
> - **Almost-Everywhere Convergence** — provides the convergence hypothesis.
> - **Fatou's Lemma** — supplies a key proof technique.

> [!note] Downstream Knowledge
> - **Parameter-Dependent Integration** — uses domination to exchange limits and integrals.
> - **Fourier Analysis** — uses dominated convergence to justify limiting arguments.
> - **Functional Analysis** — applies convergence theorems to sequences of functions.