---
type: technical-term
title: Infinite Sequences and Series
aliases:
  - Sequences and Series
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Mathematical Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - calculus
  - mathematical-analysis
sources: []
related:
  - "[[Sequences]]"
  - "[[Series]]"
  - "[[Convergence and Divergence]]"
  - "[[Tests for Convergence]]"
  - "[[Power Series]]"
  - "[[Taylor Series]]"
  - "[[Maclaurin Series]]"
projects: []
---

> [!abstract] Definition
> **Infinite Sequences and Series** is the subject concerned with ordered infinite collections of numbers, infinite sums, their convergence properties, and the representation of functions through infinite series.
>
> It provides the mathematical framework for studying limiting behavior, infinite accumulation, approximation, and analytic representations of functions.

## 1. Core Concepts

> [!important] Fundamental Distinction
> A **sequence** is an ordered list of terms indexed by the natural numbers:
>
> $$a_1,a_2,a_3,\ldots$$
>
> A **series** is the formal sum of the terms of a sequence:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> A sequence is studied through the behavior of its terms, whereas a series is studied through the behavior of its partial sums.

## 2. Subject Structure

### 2.1 Sequences and Series

> [!note] Basic Objects
> - **Sequences:** Ordered collections of terms indexed by integers.
> - **Series:** Sums formed from the terms of sequences.

### 2.2 Convergence Theory

> [!note] Limiting Behavior
> - **Convergence and Divergence:** Studies whether sequences and series approach finite limits.
> - **Tests for Convergence:** Provides mathematical criteria for determining whether infinite series converge or diverge.

### 2.3 Power Series and Function Representation

> [!note] Infinite Polynomial Representations
> - **Power Series:** Infinite series whose terms contain powers of a variable.
> - **Taylor Series:** Represents a sufficiently differentiable function through its derivatives at a specified center.
> - **Maclaurin Series:** The special case of a Taylor series centered at zero.

## 3. Mathematical Foundations

> [!important] Central Mathematical Mechanism
> Convergence is defined through limits.
>
> For a sequence:
>
> $$\lim_{n\to\infty}a_n=L$$
>
> For a series, define its partial sums:
>
> $$S_N=\sum_{n=1}^{N}a_n$$
>
> The series converges if:
>
> $$\lim_{N\to\infty}S_N=S$$
>
> Therefore, series convergence is fundamentally a question about the limiting behavior of a sequence of partial sums.

## 4. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Sequences and Limits:** Limits provide the formal definition of sequence convergence.
> - **Real Numbers:** The completeness properties of the real numbers underpin important convergence theorems.
> - **Functions:** Required for understanding power series as function representations.

> [!info] Relevant
> - **Continuity:** Helps establish convergence and function behavior.
> - **Differentiation:** Required for constructing Taylor and Maclaurin series.
> - **Integration:** Provides methods for deriving and manipulating certain infinite series.

### Downstream Knowledge

> [!info] Relevant
> - **Real Analysis:** Develops rigorous convergence theory and the properties of infinite sequences and series.
> - **Approximation Theory:** Uses polynomial and series representations to approximate functions.
> - **Differential Equations:** Uses power series to construct solutions to certain differential equations.
> - **Numerical Analysis:** Uses truncated series and convergence estimates in numerical computation.

> [!info] Advanced
> - **Uniform Convergence:** Studies convergence of sequences and series of functions under stronger conditions.
> - **Fourier Analysis:** Develops function representations using trigonometric series.
> - **Complex Analysis:** Extends power series theory to complex functions and analytic functions.

## 5. Scope and Boundaries

> [!important] Subject Boundary
> This subject focuses on:
> - Infinite numerical sequences.
> - Infinite numerical series.
> - Convergence and divergence.
> - Convergence tests.
> - Power series.
> - Taylor and Maclaurin expansions.
>
> Fourier series, measure-theoretic convergence, and the broader theory of function spaces belong to their respective subjects. They may use the foundations developed here but should not be treated as ordinary power-series topics.

## 6. Further Development

> [!todo] Recommended Study Order
> 1. Sequences
> 2. Series
> 3. Convergence and Divergence
> 4. Tests for Convergence
> 5. Power Series
> 6. Taylor Series
> 7. Maclaurin Series
>
> Study the convergence of sequences and numerical series before moving to power series and function expansions.