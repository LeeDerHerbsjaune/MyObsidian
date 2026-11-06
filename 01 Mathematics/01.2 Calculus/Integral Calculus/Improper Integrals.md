---
type: technical-term
title: "Improper Integrals"
aliases:
  - Improper Integration
  - Tích phân suy rộng
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Integral Calculus
  - Real Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - integral-calculus
  - real-analysis
sources: []
related: []
projects: []
---

# Improper Integrals

> [!abstract] Definition
> An Improper Integral is an extension of definite integration used when the integration interval is unbounded or when the integrand becomes unbounded within the interval.
>
> Improper integrals are defined through limits of proper definite integrals.

## 1. Improper Integrals with Infinite Intervals

> [!definition] Infinite Upper Bound

$$
\int_a^\infty f(x)\,dx
=
\lim_{b\to\infty}
\int_a^b f(x)\,dx
$$

> [!definition] Infinite Lower Bound

$$
\int_{-\infty}^b f(x)\,dx
=
\lim_{a\to-\infty}
\int_a^b f(x)\,dx
$$

> [!definition] Entire Real Line
> The integral over the entire real line must be split at a finite point $c$:

$$
\int_{-\infty}^{\infty}f(x)\,dx
=
\int_{-\infty}^{c}f(x)\,dx
+
\int_c^\infty f(x)\,dx
$$

Both component integrals must converge.

## 2. Improper Integrals with Unbounded Integrands

> [!definition] Singular Endpoint
> If the integrand is unbounded near the upper endpoint:

$$
\int_a^b f(x)\,dx
=
\lim_{t\to b^-}
\int_a^t f(x)\,dx
$$

For an unbounded lower endpoint:

$$
\int_a^b f(x)\,dx
=
\lim_{t\to a^+}
\int_t^b f(x)\,dx
$$

## 3. Interior Singularities

> [!important] Splitting at a Singular Point
> If the integrand is unbounded at an interior point $c$, split the integral:

$$
\int_a^b f(x)\,dx
=
\int_a^c f(x)\,dx
+
\int_c^b f(x)\,dx
$$

Both one-sided improper integrals must converge independently.

## 4. Convergence and Divergence

> [!definition] Convergence
> An improper integral converges if its defining limit exists and is finite.

> [!definition] Divergence
> An improper integral diverges if the defining limit does not exist or is infinite.

## 5. Comparison Tests

> [!info] Direct Comparison Test
> For nonnegative functions $f$ and $g$:
>
> If $0\leq f(x)\leq g(x)$ and the integral of $g$ converges, then the integral of $f$ converges.
>
> If $0\leq g(x)\leq f(x)$ and the integral of $g$ diverges, then the integral of $f$ diverges.

> [!info] Limit Comparison Test
> For positive functions, if:

$$
\lim_{x\to\infty}
\frac{f(x)}{g(x)}=L
$$

where $0<L<\infty$, their improper integrals have the same convergence behavior, under the corresponding comparison conditions.

## 6. The p-Integral

> [!important] Infinite Interval

$$
\int_1^\infty\frac{1}{x^p}\,dx
$$

- Converges if $p>1$.
- Diverges if $p\leq1$.

> [!important] Singular Endpoint

$$
\int_0^1\frac{1}{x^p}\,dx
$$

- Converges if $p<1$.
- Diverges if $p\geq1$.

## 7. Absolute and Conditional Convergence

> [!definition] Absolute Convergence
> An improper integral converges absolutely if:

$$
\int_a^\infty |f(x)|\,dx
$$

converges.

> [!definition] Conditional Convergence
> An improper integral converges conditionally if it converges, but its absolute-value integral diverges.

## 8. Cauchy Principal Value

> [!note] Principal Value
> The Cauchy Principal Value is a symmetric limiting procedure used to assign a value to certain singular or unbounded integrals.
>
> It is not equivalent to ordinary improper-integral convergence.

For a singularity at zero:

$$
\operatorname{PV}
\int_{-1}^{1}\frac{1}{x}\,dx
=
\lim_{\varepsilon\to0^+}
\left(
\int_{-1}^{-\varepsilon}\frac{1}{x}\,dx
+
\int_{\varepsilon}^{1}\frac{1}{x}\,dx
\right)
$$

This principal value is zero, although the ordinary improper integral diverges.

## 9. Knowledge Relationships

### Foundation Knowledge
- **Definite Integrals:** Provides the underlying bounded integration framework.
- **Limits:** Defines improper integration through limiting processes.
- **Riemann Integrals:** Establishes the classical theory of proper integration.
- **Sequences and Series:** Supports convergence analysis.

### Downstream Knowledge
- **Real Analysis:** Develops rigorous convergence and integration theory.
- **Lebesgue Integration:** Generalizes integration and convergence concepts.
- **Probability Theory:** Uses improper integrals for continuous distributions over unbounded domains.
- **Fourier Analysis:** Uses improper integration in the study of transforms and oscillatory functions.

## 10. References

- Apostol, Tom M. (1969). *Calculus, Volume 2*. Wiley.
- Rudin, Walter (1976). *Principles of Mathematical Analysis*. 3rd Edition.
- Bartle, Robert G. and Sherbert, Donald R. (2011). *Introduction to Real Analysis*. 4th Edition.