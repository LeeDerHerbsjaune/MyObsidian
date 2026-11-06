---
type: technical-term
title: "Change of Variables"
aliases:
  - Variable Transformation
  - Coordinate Transformation in Integration
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Linear Algebra
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
> **Change of Variables** is a mathematical technique that transforms an integral from one coordinate system or set of variables into another.
>
> In multivariable integration, the transformation must account for how the mapping changes area or volume, using the absolute value of the Jacobian determinant.

## 1. General Transformation

> [!definition] Coordinate Mapping
> Consider a differentiable transformation:
>
> $$T:\mathbb R^n\rightarrow\mathbb R^n$$
>
> mapping:
>
> $$\mathbf u\mapsto\mathbf x=T(\mathbf u)$$
>
> The Jacobian matrix describes the local linear transformation, while its determinant describes local volume scaling.

## 2. Change-of-Variables Theorem

> [!important] General Formula
> Under the appropriate assumptions, including a suitable one-to-one differentiable transformation:
>
> $$\int_D f(\mathbf x)\,d\mathbf x
> =
> \int_U f(T(\mathbf u))
> |\det J_T(\mathbf u)|\,d\mathbf u$$
>
> where:
> - $D$ is the original integration domain.
> - $U$ is the transformed domain.
> - $T$ maps $U$ to $D$.
> - $J_T$ is the Jacobian matrix.
>
> The absolute Jacobian determinant corrects for the change in area or volume.

## 3. Two-Dimensional Transformations

> [!note] Area Scaling
> For:
>
> $$x=x(u,v),\qquad y=y(u,v)$$
>
> the Jacobian determinant is:
>
> $$J=
> \frac{\partial(x,y)}{\partial(u,v)}
> =
> \begin{vmatrix}
> \frac{\partial x}{\partial u}&
> \frac{\partial x}{\partial v}\\
> \frac{\partial y}{\partial u}&
> \frac{\partial y}{\partial v}
> \end{vmatrix}$$
>
> The area element transforms as:
>
> $$dx\,dy=|J|\,du\,dv$$

## 4. Common Coordinate Transformations

> [!example] Polar Coordinates
> The transformation is:
>
> $$x=r\cos\theta,\qquad
> y=r\sin\theta$$
>
> Its Jacobian determinant has absolute value $r$:
>
> $$dx\,dy=r\,dr\,d\theta$$

> [!example] Cylindrical Coordinates
> $$x=r\cos\theta,\quad
> y=r\sin\theta,\quad z=z$$
>
> The volume element is:
>
> $$dV=r\,dr\,d\theta\,dz$$

> [!example] Spherical Coordinates
> Using the convention that $\phi$ is measured from the positive $z$-axis:
>
> $$x=\rho\sin\phi\cos\theta$$
>
> $$y=\rho\sin\phi\sin\theta$$
>
> $$z=\rho\cos\phi$$
>
> The volume element is:
>
> $$dV=\rho^2\sin\phi\,
> d\rho\,d\phi\,d\theta$$

## 5. Important Considerations

> [!warning] Transformation Conditions
> - Transform the integration domain, not only the integrand.
> - Include the absolute Jacobian determinant.
> - Check whether the mapping is one-to-one on the chosen region.
> - Account for singularities and coordinate boundaries.
> - Use a consistent coordinate convention.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Multiple Integrals:** Provides the integrals being transformed.
- **Jacobian Matrix:** Provides the local transformation matrix and determinant.
- **Linear Algebra:** Provides determinants and linear transformations.
- **Coordinate Systems:** Provides alternative representations of geometric domains.

### Downstream Knowledge
- **Vector Calculus:** Uses coordinate transformations in multidimensional integration.
- **Differential Geometry:** Generalizes coordinate transformations to manifolds.
- **Probability Theory:** Uses Jacobian determinants when transforming continuous random variables.