---
type: technical-term
title: Multivariable Calculus
aliases:
  - Calculus of Several Variables
  - Multidimensional Calculus
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
  - multivariable-calculus
sources: []
related:
  - "[[Functions of Several Variables]]"
  - "[[Limits and Continuity of Multivariable Functions]]"
  - "[[Partial Derivatives]]"
  - "[[Total Differentiation]]"
  - "[[Gradient]]"
  - "[[Directional Derivatives]]"
  - "[[Jacobian Matrix]]"
  - "[[Hessian Matrix]]"
  - "[[Multiple Integrals]]"
  - "[[Change of Variables]]"
  - "[[Constrained Optimization]]"
projects: []
---

> [!abstract] Definition
> **Multivariable Calculus** is the branch of calculus that studies functions of several independent variables and their differentiation and integration.
>
> It generalizes single-variable calculus by introducing partial derivatives, gradients, directional derivatives, higher-dimensional integration, and multivariable optimization.

## 1. Core Concepts

> [!important] Fundamental Idea
> A multivariable function maps elements from a multidimensional input space to an output space.
>
> $$f:\mathbb{R}^n\rightarrow\mathbb{R}^m$$
>
> Multivariable calculus investigates:
> - How functions behave near a point.
> - How outputs change when individual inputs vary.
> - How functions change in arbitrary directions.
> - How local derivatives describe multidimensional behavior.
> - How quantities accumulate over multidimensional regions.
> - How functions attain local or global extrema.

## 2. Subject Structure

### 2.1 Multivariable Functions and Continuity

> [!note] Function Foundations
> - **Functions of Several Variables:** Defines functions with multiple independent inputs.
> - **Limits and Continuity of Multivariable Functions:** Establishes limiting behavior and continuity in multidimensional domains.

### 2.2 Multivariable Differentiation

> [!note] First-Order Differentiation
> - **Partial Derivatives:** Measures changes with respect to individual variables.
> - **Total Differentiation:** Describes the complete first-order change of a multivariable function.
> - **Gradient:** Represents the direction and magnitude of the steepest local increase for a differentiable scalar field.
> - **Directional Derivatives:** Measures the rate of change in a specified direction.

### 2.3 Derivative Matrices and Higher-Order Structure

> [!note] Matrix Representations
> - **Jacobian Matrix:** Represents the first-order derivatives of a vector-valued function.
> - **Hessian Matrix:** Represents the second-order partial derivatives of a scalar-valued function.

### 2.4 Multivariable Integration

> [!note] Multiple Integration
> - **Multiple Integrals:** Generalizes definite integration to multidimensional domains.
> - **Change of Variables:** Transforms integrals through coordinate mappings and their Jacobian determinants.

### 2.5 Multivariable Optimization

> [!note] Optimization
> - **Constrained Optimization:** Studies extrema of functions subject to equality or inequality constraints.

## 3. Mathematical Foundations

> [!important] Differentiation
> For a scalar-valued function:
>
> $$f:\mathbb{R}^n\rightarrow\mathbb{R}$$
>
> Its first-order local behavior is described by its derivative:
>
> $$df=\sum_{i=1}^{n}
> \frac{\partial f}{\partial x_i}dx_i$$
>
> The gradient collects the first-order partial derivatives:
>
> $$\nabla f=
> \begin{bmatrix}
> \frac{\partial f}{\partial x_1}\\
> \vdots\\
> \frac{\partial f}{\partial x_n}
> \end{bmatrix}$$

> [!important] Integration
> Multiple integrals accumulate functions over multidimensional domains.
>
> A double integral has the general form:
>
> $$\iint_D f(x,y)\,dA$$
>
> A triple integral has the general form:
>
> $$\iiint_E f(x,y,z)\,dV$$

## 4. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Single-Variable Calculus:** Provides the underlying concepts of limits, derivatives, and integrals.
> - **Functions:** Establishes mappings between mathematical spaces.
> - **Limits and Continuity:** Provides the foundation for multivariable limits and differentiability.
> - **Linear Algebra:** Provides vectors, matrices, linear transformations, and determinants.

> [!info] Relevant
> - **Real Analysis:** Provides rigorous foundations for limits, continuity, and differentiability.
> - **Coordinate Systems:** Supports the representation of multidimensional domains and transformations.
> - **Sequences and Series:** Supports approximation and local function representations.

### Downstream Knowledge

> [!info] Relevant
> - **Vector Calculus:** Develops integration and differentiation of scalar and vector fields.
> - **Differential Geometry:** Uses multivariable differentiation to study curves, surfaces, and manifolds.
> - **Optimization Theory:** Extends constrained and unconstrained optimization.
> - **Differential Equations:** Uses multivariable derivatives in partial differential equations.

> [!info] Advanced
> - **Tensor Calculus:** Generalizes derivative and geometric structures to tensor fields.
> - **Calculus on Manifolds:** Extends differential and integral calculus to differentiable manifolds.
> - **Functional Analysis:** Studies optimization and differentiation in infinite-dimensional spaces.

## 5. Scope and Boundaries

> [!important] Subject Boundary
> Multivariable Calculus focuses on:
> - Functions of several variables.
> - Multivariable limits and continuity.
> - Partial and total differentiation.
> - Gradients and directional derivatives.
> - Jacobian and Hessian matrices.
> - Multiple integration and coordinate transformations.
> - Constrained optimization.
>
> Line integrals, surface integrals, divergence, curl, and the major integral theorems of vector calculus are developed in Vector Calculus.
>
> General tensor fields and differentiation on manifolds belong to more advanced mathematical subjects.

## 6. Further Development

> [!todo] Recommended Study Order
> 1. Functions of Several Variables
> 2. Limits and Continuity of Multivariable Functions
> 3. Partial Derivatives
> 4. Total Differentiation
> 5. Gradient
> 6. Directional Derivatives
> 7. Jacobian Matrix
> 8. Hessian Matrix
> 9. Multiple Integrals
> 10. Change of Variables
> 11. Constrained Optimization
>
> Study the differentiation concepts before their matrix representations. Study multiple integration before coordinate transformations. Constrained optimization builds on gradients and, for second-order analysis, Hessian matrices.