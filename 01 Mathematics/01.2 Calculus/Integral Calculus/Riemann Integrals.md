---
type: technical-term
title: "Riemann Integrals"
aliases:
  - Riemann Integration
  - Riemann Integral
  - Tích phân Riemann
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

# Riemann Integrals

> [!abstract] Definition
> The Riemann Integral is a mathematical construction that defines the integral of a bounded function over a closed and bounded interval through limits of finite sums.
>
> It formalizes the idea of approximating accumulated quantities using increasingly fine partitions of an interval.

## 1. Partition of an Interval

> [!definition] Definition
> A partition divides an interval $[a,b]$ into finitely many subintervals.

$$
P=\{a=x_0<x_1<\cdots<x_n=b\}
$$

The width of each subinterval is:

$$
\Delta x_i=x_i-x_{i-1}
$$

The mesh of the partition is:

$$
\|P\|=\max_i\Delta x_i
$$

## 2. Riemann Sum

> [!definition] Definition
> A Riemann sum approximates the integral by evaluating a function at selected sample points within each subinterval and multiplying by the corresponding interval widths.

$$
S(P,f)=
\sum_{i=1}^{n}
f(x_i^*)\Delta x_i
$$

where $x_i^*$ belongs to the corresponding subinterval.

## 3. Riemann Integrability

> [!important] Definition
> A bounded function $f$ is Riemann integrable on $[a,b]$ if its Riemann sums converge to the same finite value as the partition mesh approaches zero, independently of the choice of sample points.

$$
\int_a^b f(x)\,dx
=
\lim_{\|P\|\to0}S(P,f)
$$

## 4. Darboux Sums

> [!definition] Lower and Upper Sums
> Darboux sums provide an equivalent characterization of Riemann integrability.

For each subinterval $[x_{i-1},x_i]$:

$$
m_i=\inf f(x)
$$

$$
M_i=\sup f(x)
$$

The lower sum is:

$$
L(P,f)=
\sum_{i=1}^{n}m_i\Delta x_i
$$

The upper sum is:

$$
U(P,f)=
\sum_{i=1}^{n}M_i\Delta x_i
$$

> [!important] Integrability Criterion
> A bounded function is Riemann integrable if and only if:

$$
\sup_P L(P,f)=\inf_P U(P,f)
$$

## 5. Conditions for Integrability

> [!info] Sufficient Conditions
> A bounded function on a closed and bounded interval is Riemann integrable if it is:
>
> - Continuous.
> - Monotonic.
> - Piecewise continuous with finitely many discontinuities.

> [!note] Lebesgue Criterion
> A bounded function on a closed interval is Riemann integrable if and only if its set of discontinuities has Lebesgue measure zero.

## 6. Properties

- Linearity.
- Additivity over adjacent intervals.
- Monotonicity.
- Compatibility with continuous functions.
- Existence for bounded monotonic functions.

## 7. Limitations

> [!warning] Limitations
> - Classical Riemann integration is defined for bounded functions on compact intervals.
> - Some unbounded functions are not Riemann integrable in the ordinary sense.
> - Functions with sufficiently large or complicated sets of discontinuities may fail to be Riemann integrable.
> - Lebesgue integration provides a broader integration framework.

## 8. Knowledge Relationships

### Foundation Knowledge
- **Real Numbers:** Establishes the underlying numerical system.
- **Functions:** Provides the objects being integrated.
- **Limits:** Provides the convergence framework.
- **Sequences and Series:** Supports the analysis of approximating sums.

### Downstream Knowledge
- **Definite Integrals:** Uses Riemann integration to define accumulated quantities.
- **Improper Integrals:** Extends integration through limiting processes.
- **Measure Theory:** Provides the mathematical foundation for a more general theory of integration.
- **Lebesgue Integration:** Generalizes integration beyond the classical Riemann framework.

## 9. References

- Apostol, Tom M. (1969). *Calculus, Volume 2*. Wiley.
- Rudin, Walter (1976). *Principles of Mathematical Analysis*. 3rd Edition.
- Bartle, Robert G. and Sherbert, Donald R. (2011). *Introduction to Real Analysis*. 4th Edition.