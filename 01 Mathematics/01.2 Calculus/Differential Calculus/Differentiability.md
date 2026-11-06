---
type: technical-term
title: "Differentiability"
aliases:
  - Differentiable Function
  - Tính khả vi
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Differential Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - differential-calculus
sources: []
related: []
projects: []
---

# Differentiability

> [!abstract] Definition
> Differentiability is a mathematical property describing whether a function possesses a finite derivative at a given point or throughout a specified domain.
>
> It characterizes the local behavior of functions and establishes the conditions under which a function admits a linear approximation.

## 1. Differentiability at a Point

> [!definition] Definition
> A function $f$ is differentiable at $x=a$ if the following limit exists and is finite:

$$
f'(a)=
\lim_{h\to0}
\frac{f(a+h)-f(a)}{h}
$$

## 2. Differentiability on an Interval

> [!info] Definition
> A function is differentiable on an interval if it is differentiable at every interior point of that interval.
>
> Differentiability at endpoints is evaluated using the corresponding one-sided derivative when appropriate.

## 3. Relationship Between Differentiability and Continuity

> [!important] Fundamental Theorem
> If a function is differentiable at a point, it must be continuous at that point.

$$
f \text{ differentiable at } a
\implies
f \text{ continuous at } a
$$

> [!warning] Converse Does Not Hold
> Continuity does not guarantee differentiability.

Examples of non-differentiability include:
> - Sharp corners.
> - Cusps.
> - Vertical tangents.
> - Discontinuities.

## 4. Local Linear Approximation

> [!definition] Linear Approximation
> A function differentiable at $a$ can be approximated locally by its tangent line.

$$
f(a+h)=f(a)+f'(a)h+o(h)
$$

Here, $o(h)$ represents an error term that becomes negligible relative to $h$ as $h\to0$.

## 5. One-Sided Differentiability

> [!info] One-Sided Conditions
> A function may possess a left derivative and a right derivative independently.
>
> A two-sided derivative exists when both are finite and equal.

$$
f'_-(a)=f'_+(a)
$$

## 6. Differentiability and Smoothness

> [!note] Higher Regularity
> Differentiability can be extended into stronger regularity conditions:
>
> - $C^0$: Continuous functions.
> - $C^1$: Continuously differentiable functions.
> - $C^2$: Functions with continuous derivatives up to order two.
> - $C^k$: Functions with continuous derivatives up to order $k$.
> - $C^\infty$: Infinitely continuously differentiable functions.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Limits:** Defines the limiting behavior required for derivatives.
- **Continuity:** Establishes the relationship between continuity and differentiability.
- **Derivatives:** Provides the mathematical object whose existence is studied.

### Downstream Knowledge
- **Higher-Order Derivatives:** Extends differentiability to repeated derivatives.
- **Taylor Approximation:** Uses derivative information to construct local polynomial approximations.
- **Differential Calculus:** Uses differentiability as a central theoretical property.

## 8. References

- Apostol, Tom M. (1967). *Calculus, Volume 1*. Wiley.
- Rudin, Walter (1976). *Principles of Mathematical Analysis*. 3rd Edition. McGraw-Hill.