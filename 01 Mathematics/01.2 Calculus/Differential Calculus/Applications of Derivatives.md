---
type: technical-term
title: "Applications of Derivatives"
aliases:
  - Applications of Differential Calculus
  - Ứng dụng đạo hàm
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
  - differentiation
  - optimization
sources: []
related: []
projects: []
---

# Applications of Derivatives

> [!abstract] Definition
> Applications of Derivatives is the study of mathematical problems that can be analyzed using derivatives.
>
> Derivatives provide information about function behavior, instantaneous change, extrema, curvature, and local approximation.
>
> These properties form the mathematical foundation of classical differential optimization and function analysis.

## 1. Monotonicity

> [!definition] Increasing and Decreasing Functions
> The first derivative determines whether a differentiable function increases or decreases over an interval.

- If $f'(x)>0$, the function is strictly increasing.
- If $f'(x)<0$, the function is strictly decreasing.
- If $f'(x)=0$ throughout an interval, the function is constant there.

## 2. Critical Points

> [!definition] Definition
> A critical point is an interior point of the domain where the derivative is zero or does not exist.

$$
f'(c)=0
$$

or $f'(c)$ does not exist.

> [!important] Fermat's Theorem
> If a differentiable function has a local maximum or minimum at an interior point, its derivative must be zero there.

## 3. Local Extrema

> [!definition] Local Maximum and Minimum
> A local maximum is a point where the function value is greater than or equal to nearby values.
>
> A local minimum is a point where the function value is less than or equal to nearby values.

### First Derivative Test

> [!info] Sign Change
> - Positive to negative: Local maximum.
> - Negative to positive: Local minimum.
> - No sign change: Neither extremum is established.

### Second Derivative Test

> [!info] Second Derivative Criterion
> If $f'(c)=0$:
>
> - If $f''(c)>0$, there is a local minimum.
> - If $f''(c)<0$, there is a local maximum.
> - If $f''(c)=0$, the test is inconclusive.

## 4. Concavity and Convexity

> [!definition] Concavity
> The second derivative describes the curvature behavior of a twice-differentiable function over an interval.

- $f''(x)>0$: Strictly convex function.
- $f''(x)<0$: Strictly concave function.

## 5. Inflection Points

> [!definition] Definition
> An inflection point is a point at which a function changes concavity.
>
> A point satisfying $f''(x)=0$ is only a candidate and must be checked for a change in concavity.

## 6. Curve Sketching

> [!info] Function Analysis
> Derivatives provide information needed to construct qualitative graphs of functions.

A typical analysis includes:
> 1. Domain.
> 2. Intercepts.
> 3. Critical points.
> 4. Increasing and decreasing intervals.
> 5. Local extrema.
> 6. Concavity.
> 7. Inflection points.
> 8. Asymptotic behavior.

## 7. Optimization

> [!definition] Definition
> Optimization studies the identification of maximum and minimum values of an objective function subject to specified conditions.

### Unconstrained Optimization

For a differentiable function, candidate interior extrema satisfy:

$$
\nabla f(x)=0
$$

For a single-variable function:

$$
f'(x)=0
$$

### Absolute Extrema on Closed Intervals

> [!important] Extreme Value Theorem
> A continuous function on a closed and bounded interval attains both an absolute maximum and an absolute minimum.

For a closed interval $[a,b]$, evaluate:
> - Interior critical points.
> - Endpoints $a$ and $b$.

## 8. Linear Approximation

> [!definition] Definition
> A differentiable function can be approximated locally using its tangent line.

$$
L(x)=f(a)+f'(a)(x-a)
$$

## 9. Differential Approximation

> [!definition] Definition
> The differential approximates small changes in a function using its derivative.

$$
dy=f'(x)\,dx
$$

For sufficiently small changes:

$$
\Delta y\approx dy
$$

## 10. Knowledge Relationships

### Foundation Knowledge
- **Derivatives:** Provides the central mathematical quantity used in these applications.
- **Differentiability:** Establishes the existence of derivatives.
- **Differentiation Rules:** Provides computational methods.
- **Higher-Order Derivatives:** Provides curvature and second-derivative information.

### Downstream Knowledge
- **Optimization Theory:** Generalizes derivative-based optimization into a broader mathematical discipline.
- **Numerical Optimization:** Develops computational algorithms for finding extrema.
- **Multivariable Calculus:** Extends derivative-based analysis to functions of several variables.
- **Convex Analysis:** Develops a rigorous theory of convex functions and optimization.
- **Operations Research:** Applies optimization methods to decision and resource-allocation problems.

## 11. References

- Apostol, Tom M. (1967). *Calculus, Volume 1*. Wiley.
- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.
- Spivak, Michael (2008). *Calculus*. 4th Edition.