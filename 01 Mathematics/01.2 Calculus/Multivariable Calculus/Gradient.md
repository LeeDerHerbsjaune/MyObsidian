---
type: technical-term
title: "Gradient"
aliases:
  - Gradient Vector
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Vector Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - multivariable-calculus
sources: []
related: []
projects: []
---

> [!abstract] Definition
> The **gradient** of a differentiable scalar-valued function is a vector containing its first-order partial derivatives.
>
> It describes the direction of steepest local increase and the corresponding maximum directional rate of change under the Euclidean inner product.

## 1. Mathematical Formulation

> [!definition] Gradient
> For:
>
> $$f:\mathbb{R}^n\rightarrow\mathbb{R}$$
>
> the gradient is:
>
> $$\nabla f=
> \begin{bmatrix}
> \frac{\partial f}{\partial x_1}\\
> \frac{\partial f}{\partial x_2}\\
> \vdots\\
> \frac{\partial f}{\partial x_n}
> \end{bmatrix}$$
>
> For a function of two variables:
>
> $$\nabla f(x,y)=
> \begin{bmatrix}
> f_x\\
> f_y
> \end{bmatrix}$$

## 2. Geometric Interpretation

> [!important] Direction of Steepest Increase
> At a point where the gradient is nonzero, the gradient points in the direction of the steepest local increase of the function.
>
> Its magnitude gives the maximum rate of increase over unit directions:
>
> $$\|\nabla f\|$$

> [!note] Level-Set Orthogonality
> At regular points, the gradient is perpendicular to the level set:
>
> $$f(x_1,\ldots,x_n)=c$$
>
> This follows because the function does not change along tangent directions to the level set.

## 3. Gradient and Total Differential

> [!important] Relationship
> The total differential can be expressed using the gradient:
>
> $$df=\nabla f\cdot d\mathbf{x}$$
>
> where:
>
> $$d\mathbf{x}=
> \begin{bmatrix}
> dx_1\\
> \vdots\\
> dx_n
> \end{bmatrix}$$

## 4. Critical Points

> [!definition] Critical Point
> A point in the domain where all first-order partial derivatives vanish is a stationary point:
>
> $$\nabla f(\mathbf{x})=\mathbf{0}$$
>
> More generally, critical points also include points where the derivative does not exist, depending on the function's domain and definition.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Partial Derivatives:** Provides the components of the gradient.
- **Total Differentiation:** Connects the gradient to local linear change.
- **Linear Algebra:** Provides vector operations and inner products.

### Downstream Knowledge
- **Directional Derivatives:** Computes rates of change in specified directions.
- **Hessian Matrix:** Extends first-order derivatives to second-order structure.
- **Constrained Optimization:** Uses gradient conditions to characterize constrained extrema.
- **Vector Calculus:** Develops gradient fields and related differential operators.