---
type: technical-term
title: "Signed Measures"
aliases:
  - Signed Measure
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
  - "Rudin (1987), Real and Complex Analysis"
related: []
projects: []
---

> [!abstract] Definition
> A **signed measure** is a countably additive set function that may assign positive, negative, or infinite values to measurable sets.
>
> Unlike a positive measure, a signed measure permits negative values while retaining countable additivity.

## 1. Formal Definition

> [!definition] Signed Measure
> Let $(X,\mathcal{F})$ be a measurable space.
>
> A signed measure is a function:
>
> $$\nu:\mathcal{F}\rightarrow[-\infty,\infty]$$
>
> satisfying:
>
> 1. $\nu(\varnothing)=0$.
> 2. Countable additivity:
>
> $$\nu\left(\bigcup_{n=1}^{\infty}A_n\right)
> =
> \sum_{n=1}^{\infty}\nu(A_n)$$
>
> for pairwise disjoint measurable sets, with the definition excluding the indeterminate expression $\infty-\infty$.
>
> A signed measure cannot take both $+\infty$ and $-\infty$ as values.

## 2. Positive and Negative Sets

> [!definition] Positive Set
> A measurable set $A$ is positive with respect to $\nu$ if:
>
> $$\nu(E)\geq0$$
>
> for every measurable $E\subseteq A$.

> [!definition] Negative Set
> A measurable set $A$ is negative with respect to $\nu$ if:
>
> $$\nu(E)\leq0$$
>
> for every measurable $E\subseteq A$.

## 3. Hahn Decomposition Theorem

> [!theorem] Hahn Decomposition
> Every signed measure $\nu$ admits a decomposition:
>
> $$X=P\cup N$$
>
> where:
> - $P$ is a positive set.
> - $N$ is a negative set.
> - $P\cap N=\varnothing$.
>
> This decomposition separates the space into regions where the signed measure is nonnegative and nonpositive.

## 4. Jordan Decomposition

> [!theorem] Jordan Decomposition
> Every signed measure can be represented uniquely as:
>
> $$\nu=\nu^+-\nu^-$$
>
> where $\nu^+$ and $\nu^-$ are mutually singular positive measures.
>
> Their sum defines the total variation measure:
>
> $$|\nu|=\nu^++\nu^-$$

## 5. Total Variation

> [!definition] Total Variation Measure
> For a measurable set $A$:
>
> $$|\nu|(A)
> =
> \sup_{\{A_i\}}
> \sum_i|\nu(A_i)|$$
>
> where the supremum is taken over finite measurable partitions of $A$.
>
> The total variation measures the overall magnitude of the signed measure without cancellation.

## 6. Integration

> [!important] Integration with Respect to a Signed Measure
> For a suitable measurable function $f$:
>
> $$\int_Xf\,d\nu
> =
> \int_Xf\,d\nu^+
> -
> \int_Xf\,d\nu^-$$
>
> A standard sufficient condition for finite integrability is:
>
> $$\int_X|f|\,d|\nu|<\infty$$

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — provides the measurable space.
> - **Positive Measures** — provides the underlying concept generalized by signed measures.
> - **Lebesgue Integral** — provides the integration framework.

> [!note] Downstream Knowledge
> - **Jordan Decomposition** — separates a signed measure into positive components.
> - **Total Variation** — quantifies the magnitude of a signed measure.
> - **Complex Measures** — extends measure theory to complex-valued set functions.