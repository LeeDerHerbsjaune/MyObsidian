---
type: technical-term
title: "Constrained Optimization"
aliases:
  - Constrained Extremum
  - Optimization with Constraints
abbreviation: ""
field:
  - Mathematics
subfield:
  - Optimization
  - Calculus
  - Mathematical Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - optimization
  - multivariable-calculus
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Constrained Optimization** studies the maximization or minimization of an objective function subject to restrictions on the allowable decision variables.
>
> In multivariable calculus, it primarily introduces equality-constrained extrema, Lagrange multipliers, and the geometric interpretation of constrained stationary points.

## 1. Mathematical Formulation

> [!definition] Optimization Problem
> A general constrained optimization problem can be written as:
>
> $$\begin{aligned}
> \text{minimize}\quad & f(\mathbf x)\\
> \text{subject to}\quad & g_i(\mathbf x)=0\\
> & h_j(\mathbf x)\leq0
> \end{aligned}$$
>
> where:
> - $f$ is the objective function.
> - $g_i$ are equality constraints.
> - $h_j$ are inequality constraints.
> - $\mathbf x$ is the decision vector.

## 2. Equality Constraints

> [!definition] Equality-Constrained Optimization
> An equality constraint restricts the feasible solutions to a set satisfying:
>
> $$g(\mathbf x)=0$$
>
> The feasible set is the collection of all points satisfying the constraint.

## 3. Lagrange Multipliers

> [!important] Lagrange Multiplier Method
> To find stationary points of $f(\mathbf x)$ subject to:
>
> $$g(\mathbf x)=0$$
>
> define the Lagrangian:
>
> $$\mathcal L(\mathbf x,\lambda)
> =f(\mathbf x)-\lambda g(\mathbf x)$$
>
> The first-order necessary conditions are:
>
> $$\nabla f(\mathbf x)
> =\lambda\nabla g(\mathbf x)$$
>
> $$g(\mathbf x)=0$$
>
> These conditions apply at regular constrained local extrema, where the constraint gradient is nonzero.

<LearningViz type_id="LAGRANGE_GRADIENT_PARALLELISM" initial_values={{"example":"ellipse","angleDegrees":30}}/>

> [!important] Geometric Interpretation
> At a regular constrained extremum, the objective function's gradient is parallel to the constraint gradient.
>
> The objective has no first-order change along feasible tangent directions at that point.

## 4. Multiple Equality Constraints

> [!definition] Multiple Constraints
> For constraints:
>
> $$g_1(\mathbf x)=0,\ldots,g_m(\mathbf x)=0$$
>
> the Lagrangian can be defined as:
>
> $$\mathcal L(\mathbf x,\boldsymbol\lambda)
> =f(\mathbf x)
> -\sum_{i=1}^{m}\lambda_i g_i(\mathbf x)$$
>
> Its stationary conditions are:
>
> $$\nabla f(\mathbf x)
> =\sum_{i=1}^{m}
> \lambda_i\nabla g_i(\mathbf x)$$
>
> together with all equality constraints.

## 5. Inequality Constraints

> [!note] Inequality-Constrained Optimization
> Inequality constraints introduce additional conditions because a constraint may be active or inactive at an optimum.
>
> The broader theory uses the Karush–Kuhn–Tucker (KKT) conditions, which include:
> - Stationarity.
> - Primal feasibility.
> - Dual feasibility.
> - Complementary slackness.
>
> These conditions extend the Lagrange multiplier framework.

## 6. Second-Order Conditions

> [!important] Second-Order Analysis
> First-order stationary conditions alone do not establish whether a point is a maximum or minimum.
>
> Second-order analysis uses the Hessian of the Lagrangian, restricted to feasible tangent directions, to classify constrained extrema.
>
> This requires additional regularity and constraint qualification assumptions.

## 7. Global and Local Extrema

> [!note] Local Optimum
> A local optimum is optimal relative to sufficiently nearby feasible points.

> [!note] Global Optimum
> A global optimum is optimal over the entire feasible set.
>
> A local optimum need not be a global optimum.

## 8. Knowledge Relationships

### Foundation Knowledge
- **Functions of Several Variables:** Defines objective and constraint functions.
- **Partial Derivatives:** Provides derivatives of objective and constraint functions.
- **Gradient:** Establishes first-order stationarity conditions.
- **Hessian Matrix:** Provides second-order curvature information.
- **Linear Algebra:** Provides vector spaces, rank, and linear independence.

### Downstream Knowledge
- **Optimization Theory:** Generalizes constrained optimization into a broader theoretical framework.
- **Numerical Optimization:** Develops algorithms for finding constrained optima.
- **Convex Optimization:** Studies problems with convex objectives and feasible sets.
- **Operations Research:** Applies optimization to decision-making and resource allocation.