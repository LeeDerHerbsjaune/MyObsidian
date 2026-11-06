---
type: technical-term
title: "Product Measures"
aliases:
  - Product Measure
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
> A **product measure** is a measure constructed on the product of measurable spaces. It generalizes the concept of area and volume by combining measures defined on separate spaces.
>
> Product measures provide the foundation for integrating functions of several variables in measure theory.

## 1. Product Measurable Space

> [!definition] Product σ-Algebra
> Let $(X,\mathcal{F})$ and $(Y,\mathcal{G})$ be measurable spaces.
>
> Their product σ-algebra is:
>
> $$\mathcal{F}\otimes\mathcal{G}
> =
> \sigma\left(
> \{A\times B:A\in\mathcal{F},B\in\mathcal{G}\}
> \right)$$
>
> It is the smallest σ-algebra containing all measurable rectangles.

## 2. Product Measure

> [!definition] Product Measure
> Given σ-finite measure spaces $(X,\mathcal{F},\mu)$ and $(Y,\mathcal{G},\nu)$, there exists a unique measure $\mu\times\nu$ on $\mathcal{F}\otimes\mathcal{G}$ satisfying:
>
> $$ (\mu\times\nu)(A\times B)=\mu(A)\nu(B) $$
>
> for measurable rectangles $A\times B$.

## 3. Properties

> [!important] Rectangle Measure
> The measure of a measurable rectangle is the product of the measures of its sides.
>
> $$\mu\times\nu(A\times B)=\mu(A)\nu(B)$$

> [!important] σ-Finiteness
> The standard product-measure existence and uniqueness theorem uses σ-finiteness of the factor measures.

## 4. Examples

> [!example] Euclidean Product Measure
> The product of Lebesgue measures on $\mathbb{R}^m$ and $\mathbb{R}^n$ is Lebesgue measure on $\mathbb{R}^{m+n}$.

> [!example] Product Probability Measure
> If $\mu$ and $\nu$ are probability measures, their product describes independent coordinate distributions on the product space.

## 5. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Measure Spaces** — provides the individual measure spaces.
> - **Measurable Sets** — provides the measurable rectangles.
> - **Lebesgue Integral** — provides the integration framework.

> [!note] Downstream Knowledge
> - **Tonelli's Theorem** — establishes iterated integration for nonnegative functions.
> - **Fubini's Theorem** — establishes iterated integration for integrable functions.
> - **Product Probability Spaces** — constructs joint distributions of independent random variables.