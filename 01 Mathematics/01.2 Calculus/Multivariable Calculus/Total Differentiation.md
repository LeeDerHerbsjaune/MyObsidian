---
type: technical-term
title: "Total Differentiation"
aliases:
  - Total Differential
  - Total Derivative
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
  - multivariable-calculus
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Total Differentiation** describes the complete first-order change of a differentiable multivariable function resulting from simultaneous changes in all its independent variables.
>
> It combines the individual partial derivatives into a linear approximation of the function's local behavior.

## 1. Total Differential

> [!definition] Total Differential
> For a differentiable function:
>
> $$z=f(x_1,x_2,\ldots,x_n)$$
>
> its total differential is:
>
> $$dz=\sum_{i=1}^{n}
> \frac{\partial f}{\partial x_i}dx_i$$
>
> For two variables:
>
> $$dz=f_x\,dx+f_y\,dy$$

## 2. Linear Approximation

> [!important] First-Order Approximation
> If $f$ is differentiable at $(a,b)$, then for small changes $\Delta x$ and $\Delta y$:
>
> $$\Delta f\approx
> f_x(a,b)\Delta x+
> f_y(a,b)\Delta y$$
>
> The corresponding linear approximation is:
>
> $$f(a+\Delta x,b+\Delta y)
> \approx f(a,b)+
> f_x(a,b)\Delta x+
> f_y(a,b)\Delta y$$
>
> The approximation error is of smaller order than the norm of the input perturbation.

## 3. Differentiability

> [!important] Mathematical Condition
> A function is differentiable at a point if its local change can be represented by a linear map plus an error that becomes negligible relative to the input displacement.
>
> For $f:\mathbb{R}^n\rightarrow\mathbb{R}$:
>
> $$f(\mathbf{a}+\mathbf{h})
> =f(\mathbf{a})+
> \nabla f(\mathbf{a})^T\mathbf{h}
> +o(\|\mathbf{h}\|)$$
>
> Existence of partial derivatives alone does not guarantee differentiability.

## 4. Chain Rule

> [!definition] Multivariable Chain Rule
> Suppose $z=f(x,y)$ and $x=x(t)$, $y=y(t)$. Then:
>
> $$\frac{dz}{dt}
> =
> \frac{\partial f}{\partial x}\frac{dx}{dt}
> +
> \frac{\partial f}{\partial y}\frac{dy}{dt}$$
>
> This expresses the rate of change of a composite function through its intermediate variables.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Partial Derivatives:** Supplies the individual first-order derivatives.
- **Limits and Continuity:** Provides the local limiting framework.
- **Linear Algebra:** Provides linear maps and vector representations.

### Downstream Knowledge
- **Gradient:** Represents the coefficients of the total differential as a vector.
- **Jacobian Matrix:** Generalizes total differentiation to vector-valued mappings.
- **Directional Derivatives:** Uses the derivative to calculate change along a direction.