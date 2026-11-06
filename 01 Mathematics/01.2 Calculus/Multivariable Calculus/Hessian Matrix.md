---
type: technical-term
title: "Hessian Matrix"
aliases:
  - Hessian
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Calculus
  - Optimization
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - multivariable-calculus
  - optimization
sources: []
related: []
projects: []
---

> [!abstract] Definition
> The **Hessian Matrix** is a square matrix containing all second-order partial derivatives of a scalar-valued function.
>
> It describes the local second-order behavior of a function and is fundamental to curvature analysis and multivariable optimization.

## 1. Mathematical Formulation

> [!definition] Hessian Matrix
> For:
>
> $$f:\mathbb R^n\rightarrow\mathbb R$$
>
> the Hessian matrix is:
>
> $$H_f(\mathbf x)=
> \begin{bmatrix}
> \frac{\partial^2 f}{\partial x_1^2}
> &\cdots&
> \frac{\partial^2 f}{\partial x_1\partial x_n}\\
> \vdots&\ddots&\vdots\\
> \frac{\partial^2 f}{\partial x_n\partial x_1}
> &\cdots&
> \frac{\partial^2 f}{\partial x_n^2}
> \end{bmatrix}$$

## 2. Second-Order Taylor Approximation

> [!important] Quadratic Approximation
> If $f$ is twice differentiable near $\mathbf a$, its second-order Taylor approximation is:
>
> $$f(\mathbf a+\mathbf h)\approx
> f(\mathbf a)+
> \nabla f(\mathbf a)^T\mathbf h+
> \frac12\mathbf h^T H_f(\mathbf a)\mathbf h$$
>
> The Hessian determines the quadratic component of the local approximation.

## 3. Symmetry

> [!important] Hessian Symmetry
> If the second-order mixed partial derivatives are continuous near a point, then:
>
> $$H_f=H_f^T$$
>
> The Hessian is therefore symmetric under these regularity conditions.

## 4. Second-Order Classification

> [!definition] Positive Definiteness
> A symmetric Hessian is positive definite if:
>
> $$\mathbf v^T H_f\mathbf v>0$$
>
> for every nonzero vector $\mathbf v$.

> [!definition] Negative Definiteness
> A symmetric Hessian is negative definite if:
>
> $$\mathbf v^T H_f\mathbf v<0$$
>
> for every nonzero vector $\mathbf v$.

> [!important] Second-Order Test
> At a stationary point where $\nabla f(\mathbf a)=0$:
>
> - Positive definite Hessian: strict local minimum.
> - Negative definite Hessian: strict local maximum.
> - Indefinite Hessian: saddle point.
> - Positive semidefinite or negative semidefinite Hessian: generally inconclusive.
>
> These classifications assume the required second-order regularity.

## 5. Eigenvalue Interpretation

> [!note] Curvature Directions
> For a symmetric Hessian, its eigenvalues describe the second-order curvature along corresponding eigenvector directions.
>
> - All eigenvalues positive: positive definite.
> - All eigenvalues negative: negative definite.
> - Both positive and negative eigenvalues: indefinite.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Partial Derivatives:** Supplies second-order derivatives.
- **Gradient:** Defines the first-order stationary-point condition.
- **Linear Algebra:** Provides eigenvalues, eigenvectors, and definiteness.

### Downstream Knowledge
- **Constrained Optimization:** Uses second-order information to classify constrained extrema.
- **Numerical Optimization:** Uses Hessian information in second-order optimization algorithms.
- **Optimization Theory:** Develops curvature-based optimality conditions.