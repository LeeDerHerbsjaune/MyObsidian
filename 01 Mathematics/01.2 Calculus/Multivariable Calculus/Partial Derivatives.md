---
type: technical-term
title: "Partial Derivatives"
aliases:
  - Partial Differentiation
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
> A **partial derivative** measures the rate of change of a multivariable function with respect to one input variable while holding the other variables constant.

## 1. Mathematical Formulation

> [!definition] First-Order Partial Derivative
> For $f(x_1,\ldots,x_n)$, the partial derivative with respect to $x_i$ is:
>
> $$\frac{\partial f}{\partial x_i}
> =
> \lim_{h\to0}
> \frac{
> f(x_1,\ldots,x_i+h,\ldots,x_n)
> -f(x_1,\ldots,x_i,\ldots,x_n)
> }{h}$$
>
> provided the limit exists.

## 2. Notation

> [!note] Common Notations
> For $f(x,y)$:
>
> $$f_x=\frac{\partial f}{\partial x}$$
>
> $$f_y=\frac{\partial f}{\partial y}$$
>
> Both represent derivatives with respect to one variable while holding the other constant.

## 3. Higher-Order Partial Derivatives

> [!definition] Second-Order Partial Derivatives
> Partial derivatives can be differentiated again:
>
> $$f_{xx}=\frac{\partial^2f}{\partial x^2}$$
>
> $$f_{yy}=\frac{\partial^2f}{\partial y^2}$$
>
> Mixed partial derivatives are:
>
> $$f_{xy}=
> \frac{\partial^2f}{\partial y\,\partial x}$$
>
> $$f_{yx}=
> \frac{\partial^2f}{\partial x\,\partial y}$$
>
> The notation follows the order of differentiation convention used in the expression.

## 4. Equality of Mixed Partials

> [!important] Clairaut's Theorem
> If the relevant second-order mixed partial derivatives are continuous in a neighborhood of a point, then:
>
> $$f_{xy}=f_{yx}$$
>
> This equality is guaranteed under the theorem's continuity assumptions, not for every function without qualification.

## 5. Geometric Interpretation

> [!note] Surface Interpretation
> For a surface $z=f(x,y)$:
> - $f_x$ describes the slope in the $x$ direction.
> - $f_y$ describes the slope in the $y$ direction.
>
> These are slopes of the corresponding coordinate-direction cross-sections, with the other coordinate held fixed.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Functions of Several Variables:** Defines the functions being differentiated.
- **Limits and Continuity:** Provides the limiting definition of derivatives.
- **Single-Variable Differentiation:** Supplies the basic differentiation rules.

### Downstream Knowledge
- **Total Differentiation:** Combines partial derivatives into a complete first-order differential.
- **Gradient:** Collects first-order partial derivatives into a vector.
- **Hessian Matrix:** Organizes second-order partial derivatives into a matrix.
- **Jacobian Matrix:** Generalizes first-order partial derivatives to vector-valued functions.