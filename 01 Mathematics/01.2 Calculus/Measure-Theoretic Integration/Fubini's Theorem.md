---
type: technical-term
title: "Fubini's Theorem"
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
  - product-integration
sources:
  - "Folland (1999), Real Analysis"
  - "Rudin (1987), Real and Complex Analysis"
related: []
projects: []
---

> [!abstract] Definition
> **Fubini's Theorem** states that an absolutely integrable function on a product measure space can be integrated through iterated integration, with the order of integration interchangeable.
>
> It provides the rigorous foundation for evaluating multiple integrals by repeated one-dimensional integration.

## 1. Formal Statement

> [!theorem] Fubini's Theorem
> Let $(X,\mathcal{F},\mu)$ and $(Y,\mathcal{G},\nu)$ be σ-finite measure spaces.
>
> Suppose $f:X\times Y\rightarrow\mathbb{R}$ or $\mathbb{C}$ is product-measurable and:
>
> $$\int_{X\times Y}|f|\,d(\mu\times\nu)<\infty$$
>
> Then:
>
> $$\boxed{
> \int_{X\times Y}f\,d(\mu\times\nu)
> =
> \int_X\left(\int_Yf(x,y)\,d\nu(y)\right)d\mu(x)
> }$$
>
> The order of integration can be reversed, and the corresponding sections are integrable almost everywhere.

## 2. Absolute Integrability

> [!definition] Absolute Integrability Condition
> The essential condition is:
>
> $$f\in L^1(X\times Y,\mu\times\nu)$$
>
> Equivalently:
>
> $$\int_{X\times Y}|f|\,d(\mu\times\nu)<\infty$$
>
> This condition prevents ambiguity caused by separately infinite positive and negative contributions.

## 3. Interpretation

> [!important] Iterated Integration
> A multiple integral can be evaluated by integrating with respect to one variable first and then integrating the result with respect to the remaining variable.
>
> Under the theorem's hypotheses, changing the order does not change the result.

## 4. Important Conditions

> [!warning] Hypotheses
> - The factor measure spaces are σ-finite.
> - The function is product-measurable.
> - The function is absolutely integrable.
>
> Without absolute integrability, exchanging the order of integration may fail or produce undefined expressions.

## 5. Relationship to Tonelli's Theorem

> [!important] Tonelli–Fubini Relationship
> Tonelli's theorem applies to nonnegative measurable functions, even if the integral is infinite.
>
> Fubini's theorem applies to absolutely integrable functions, including signed and complex-valued functions.
>
> Applying Tonelli's theorem to $|f|$ is a standard way to verify the absolute-integrability condition needed for Fubini's theorem.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Product Measures** — supplies the product measure.
> - **Lebesgue Integral** — supplies the integration framework.
> - **Integrable Functions** — provides the absolute-integrability condition.
> - **Tonelli's Theorem** — provides the nonnegative integration result.

> [!note] Downstream Knowledge
> - **Multiple Integrals** — uses iterated integration.
> - **Probability Theory** — supports integration over joint distributions.
> - **Functional Analysis** — uses product-space integration in function-space theory.