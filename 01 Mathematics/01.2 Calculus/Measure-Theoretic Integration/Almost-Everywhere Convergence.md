---
type: technical-term
title: "Almost-Everywhere Convergence"
aliases:
  - Almost Everywhere Convergence
  - a.e. Convergence
field:
  - Mathematics
subfield:
  - Measure Theory
  - Real Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - measure-theory
  - convergence
sources:
  - "Folland (1999), Real Analysis"
  - "Royden & Fitzpatrick (2010), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> **Almost-everywhere convergence** is pointwise convergence of a sequence of measurable functions outside a set of measure zero.
>
> It allows exceptional points where convergence fails, provided those points form a null set.

## 1. Formal Definition

> [!definition] Almost-Everywhere Convergence
> Let $(X,\mathcal{F},\mu)$ be a measure space and let $f_n:X\rightarrow\mathbb{R}$ be measurable.
>
> The sequence $(f_n)$ converges almost everywhere to $f$ if:
>
> $$f_n(x)\rightarrow f(x)$$
>
> for every $x$ outside some measurable null set $N$:
>
> $$\mu(N)=0$$
>
> This is written:
>
> $$f_n\xrightarrow{\mathrm{a.e.}}f$$

## 2. Exceptional Sets

> [!important] Null Exceptional Set
> Define the failure set:
>
> $$N=\{x\in X:f_n(x)\not\rightarrow f(x)\}$$
>
> Almost-everywhere convergence means that this set is contained in a measurable set of measure zero.
>
> The convergence may fail at individual points or even at infinitely many points.

## 3. Relationship to Other Convergence Modes

> [!important] Pointwise Convergence
> Almost-everywhere convergence is pointwise convergence except on a null set.
>
> Pointwise convergence everywhere implies almost-everywhere convergence.

> [!important] Almost-Uniform Convergence
> On a finite measure space, Egorov's theorem states that almost-everywhere convergence implies uniform convergence outside a measurable set of arbitrarily small measure, provided the limit is finite almost everywhere.

> [!important] Convergence in Measure
> On a finite measure space, almost-everywhere convergence implies convergence in measure.
>
> The converse is not generally true for the full sequence, but convergence in measure admits an almost-everywhere convergent subsequence.

## 4. Egorov's Theorem

> [!theorem] Egorov's Theorem
> Let $\mu(X)<\infty$ and suppose $f_n\rightarrow f$ almost everywhere, with $f$ finite almost everywhere.
>
> For every $\varepsilon>0$, there exists a measurable set $E$ such that:
>
> $$\mu(E)<\varepsilon$$
>
> and $f_n\rightarrow f$ uniformly on $X\setminus E$.

## 5. Subsequence Principle

> [!theorem] Subsequence Characterization
> If $f_n\rightarrow f$ in measure, then there exists a subsequence $(f_{n_k})$ such that:
>
> $$f_{n_k}\rightarrow f\quad\text{almost everywhere}$$
>
> This result assumes the usual measure-space setting and finite-valued measurable functions.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — defines null sets and measure.
> - **Measurable Functions** — provides the measurable sequences being studied.
> - **Pointwise Convergence** — provides the underlying convergence concept.

> [!note] Downstream Knowledge
> - **Dominated Convergence Theorem** — uses almost-everywhere convergence as a hypothesis.
> - **Fatou's Lemma** — relates almost-everywhere limits to integrals.
> - **Egorov's Theorem** — strengthens almost-everywhere convergence to uniform convergence outside a small set.