---
type: technical-term
title: "Definite Integrals"
aliases:
  - Definite Integration
  - Tích phân xác định
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Integral Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - integral-calculus
sources: []
related: []
projects: []
---

# Definite Integrals

> [!abstract] Definition
> A definite integral is a mathematical quantity representing the accumulated signed contribution of a function over a specified interval.
>
> It is defined through the limit of finite sums and provides the mathematical foundation for continuous accumulation and area calculations.

## 1. Mathematical Definition

> [!definition] Definite Integral

$$
\int_a^b f(x)\,dx
$$

where:

- $f(x)$: Integrand.
- $a$: Lower integration limit.
- $b$: Upper integration limit.
- $dx$: Integration variable.

## 2. Riemann Sum Representation

> [!important] Limit of Riemann Sums
> A definite integral can be constructed as the limit of sums of function values multiplied by subinterval widths.

$$
\int_a^b f(x)\,dx
=
\lim_{n\to\infty}
\sum_{i=1}^{n}
f(x_i^*)\Delta x_i
$$

provided the limit exists.

For an equal partition:

$$
\Delta x=\frac{b-a}{n}
$$

## 3. Geometric Interpretation

> [!info] Signed Area
> A definite integral represents signed area between a function and the horizontal axis.

- Regions above the axis contribute positively.
- Regions below the axis contribute negatively.

> [!warning] Signed Area vs. Geometric Area
> The definite integral is not necessarily equal to the total geometric area.

The total geometric area is:

$$
A=\int_a^b|f(x)|\,dx
$$

## 4. Fundamental Properties

> [!info] Linearity

$$
\int_a^b[af(x)+bg(x)]\,dx
=
a\int_a^b f(x)\,dx
+
b\int_a^b g(x)\,dx
$$

> [!info] Additivity

$$
\int_a^b f(x)\,dx
=
\int_a^c f(x)\,dx
+
\int_c^b f(x)\,dx
$$

> [!info] Reversal of Limits

$$
\int_a^b f(x)\,dx
=
-\int_b^a f(x)\,dx
$$

> [!info] Equal Limits

$$
\int_a^a f(x)\,dx=0
$$

## 5. Integral Bounds

> [!important] Comparison Property
> If $f(x)\leq g(x)$ on $[a,b]$, then:

$$
\int_a^b f(x)\,dx
\leq
\int_a^b g(x)\,dx
$$

## 6. Applications

- Area calculations.
- Accumulated displacement.
- Total accumulated quantities.
- Work and energy calculations.
- Probability distributions.
- Continuous mathematical modeling.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Functions:** Defines the integrand.
- **Limits:** Provides the mathematical basis of integration.
- **Riemann Integrals:** Establishes the rigorous construction of definite integrals.
- **Sequences and Series:** Supports the limiting processes used in integration.

### Downstream Knowledge
- **Fundamental Theorem of Calculus:** Connects definite integrals with antiderivatives.
- **Improper Integrals:** Extends integration to unbounded intervals and certain unbounded integrands.
- **Applications of Integration:** Uses definite integrals to calculate accumulated quantities.
- **Multiple Integrals:** Generalizes definite integration to multidimensional domains.

## 8. References

- Apostol, Tom M. (1969). *Calculus, Volume 2*. Wiley.
- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.