---
type: technical-term
title: "Constraints"
aliases:
  - Variational Constraints
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus of Variations
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - constrained-optimization
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Constraints** in the calculus of variations are restrictions imposed on admissible functions or their derivatives.
>
> They restrict the set of candidate functions over which a functional is optimized.

## 2. Types of Constraints

> [!note] Boundary Constraints
> Boundary constraints prescribe function values or derivative values at the boundary:
>
> $$y(a)=A,\qquad y(b)=B$$
>
> These conditions restrict the admissible function class.

> [!note] Integral Constraints
> Integral constraints impose conditions on an integral involving the unknown function.
>
> A typical isoperimetric constraint is:
>
> $$K[y]=\int_a^b G(x,y,y')\,dx=C$$

> [!note] Pointwise Constraints
> Pointwise constraints restrict the value of a function at every point:
>
> $$g(x,y(x))=0$$
>
> Inequality constraints may take the form:
>
> $$g(x,y(x))\leq 0$$

## 3. Constrained Variational Optimization

> [!important] Integral Constraint and Lagrange Multiplier
> Consider minimizing:
>
> $$J[y]=\int_a^b L(x,y,y')\,dx$$
>
> subject to:
>
> $$K[y]=\int_a^b G(x,y,y')\,dx=C$$
>
> Under suitable regularity and constraint qualifications, introduce a multiplier $\lambda$ and construct:
>
> $$\widetilde{J}[y]
> =
> \int_a^b
> \left[
> L(x,y,y')+\lambda G(x,y,y')
> \right]dx$$
>
> The stationary function satisfies the Euler–Lagrange equation for the augmented Lagrangian:
>
> $$\frac{\partial (L+\lambda G)}{\partial y}
> -
> \frac{d}{dx}
> \left(
> \frac{\partial (L+\lambda G)}{\partial y'}
> \right)=0$$
>
> The original constraint must also be satisfied.

## 4. Isoperimetric Problems

> [!note] Isoperimetric Variational Problem
> An isoperimetric problem optimizes one functional subject to an integral constraint.
>
> A classical example is finding a closed curve enclosing the largest possible area for a fixed perimeter.
>
> Such problems are important examples of constrained variational optimization.

## 5. Interpretation and Limitations

> [!warning] Important Considerations
> - The multiplier method requires suitable regularity and constraint qualifications.
> - A stationary solution of the augmented functional is not automatically an optimizer.
> - Inequality constraints may require complementary-slackness conditions and more general optimality systems.
> - Boundary restrictions and interior constraints must be treated consistently.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Admissible Functions:** Constraints define the admissible class.
> - **Functionals:** The constrained objective is a functional.
> - **First Variation:** Provides the stationarity condition.
> - **Lagrange Multipliers:** Supply a method for handling equality constraints.
>
> [!note] Downstream Knowledge
> - **Isoperimetric Problems:** A major class of integral-constrained variational problems.
> - **Optimal Control Theory:** Develops constrained optimization of dynamical systems.
> - **Karush–Kuhn–Tucker Conditions:** Extend multiplier-based optimality conditions to inequality constraints in appropriate optimization settings.

## 7. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Liberzon, D. (2012). *Calculus of Variations and Optimal Control Theory*. Princeton University Press.