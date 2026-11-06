---
type: technical-term
title: "Directional Derivatives"
aliases:
  - Directional Differentiation
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
> A **directional derivative** measures the rate of change of a multivariable function at a point in a specified direction.
>
> It generalizes partial derivatives, which measure changes only along coordinate directions.

## 1. Mathematical Formulation

> [!definition] Directional Derivative
> For a function $f:\mathbb{R}^n\rightarrow\mathbb{R}$, the directional derivative at $\mathbf{a}$ in the direction of a unit vector $\mathbf{u}$ is:
>
> $$D_{\mathbf{u}}f(\mathbf{a})
> =
> \lim_{h\to0}
> \frac{f(\mathbf{a}+h\mathbf{u})-f(\mathbf{a})}{h}$$
>
> provided the limit exists.

## 2. Gradient Formula

> [!important] Directional Derivative Formula
> If $f$ is differentiable at $\mathbf{a}$, then:
>
> $$D_{\mathbf{u}}f(\mathbf{a})
> =\nabla f(\mathbf{a})\cdot\mathbf{u}$$
>
> The direction vector must be normalized to unit length when using this formula for a rate of change per unit distance.

## 3. Geometric Interpretation

> [!note] Positive and Negative Values
> - Positive directional derivative: the function increases in that direction.
> - Negative directional derivative: the function decreases in that direction.
> - Zero directional derivative: the first-order rate of change is zero in that direction.

> [!important] Maximum and Minimum Directional Rates
> For unit vectors $\mathbf{u}$:
>
> $$\max_{\|\mathbf{u}\|=1}
> D_{\mathbf{u}}f
> =\|\nabla f\|$$
>
> The maximum occurs in the gradient direction when the gradient is nonzero.
>
> The minimum is $-\|\nabla f\|$, attained in the opposite direction.

## 4. Relationship to Partial Derivatives

> [!note] Coordinate Directions
> Partial derivatives are special cases of directional derivatives along coordinate unit vectors.
>
> For example:
>
> $$D_{\mathbf{e}_1}f=
> \frac{\partial f}{\partial x_1}$$

## 5. Knowledge Relationships

### Foundation Knowledge
- **Partial Derivatives:** Provides coordinate-direction rates of change.
- **Gradient:** Determines directional derivatives through the dot product.
- **Linear Algebra:** Provides vector directions and inner products.

### Downstream Knowledge
- **Optimization:** Uses directional rates to identify improving directions.
- **Vector Calculus:** Develops directional differentiation of scalar and vector fields.