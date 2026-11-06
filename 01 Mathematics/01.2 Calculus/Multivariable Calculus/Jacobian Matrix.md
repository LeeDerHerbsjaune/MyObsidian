---
type: technical-term
title: "Jacobian Matrix"
aliases:
  - Jacobian
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
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
  - linear-algebra
sources: []
related: []
projects: []
---

> [!abstract] Definition
> The **Jacobian Matrix** is a matrix containing the first-order partial derivatives of a vector-valued function.
>
> It represents the linear transformation that best approximates the function locally near a differentiable point.

## 1. Mathematical Formulation

> [!definition] Jacobian Matrix
> Consider a vector-valued function:
>
> $$\mathbf{F}:\mathbb{R}^n\rightarrow\mathbb{R}^m$$
>
> where:
>
> $$\mathbf{F}(\mathbf{x})=
> \begin{bmatrix}
> f_1(\mathbf{x})\\
> f_2(\mathbf{x})\\
> \vdots\\
> f_m(\mathbf{x})
> \end{bmatrix}$$
>
> Its Jacobian matrix is:
>
> $$J_{\mathbf F}=
> \begin{bmatrix}
> \frac{\partial f_1}{\partial x_1}&\cdots&
> \frac{\partial f_1}{\partial x_n}\\
> \vdots&\ddots&\vdots\\
> \frac{\partial f_m}{\partial x_1}&\cdots&
> \frac{\partial f_m}{\partial x_n}
> \end{bmatrix}$$
>
> Its dimensions are $m\times n$.

## 2. Local Linear Approximation

> [!important] First-Order Approximation
> If $\mathbf F$ is differentiable at $\mathbf a$, then:
>
> $$\mathbf F(\mathbf a+\mathbf h)
> =
> \mathbf F(\mathbf a)
> +J_{\mathbf F}(\mathbf a)\mathbf h
> +o(\|\mathbf h\|)$$
>
> The Jacobian matrix is therefore the matrix representation of the derivative of a vector-valued function.

## 3. Jacobian Determinant

> [!definition] Jacobian Determinant
> For a square Jacobian matrix, its determinant is:
>
> $$\det(J_{\mathbf F})$$
>
> It describes the local signed volume-scaling factor of the transformation.
>
> The absolute value:
>
> $$|\det(J_{\mathbf F})|$$
>
> gives the local volume-scaling factor.

> [!important] Local Invertibility
> If a continuously differentiable mapping has a nonsingular Jacobian matrix at a point, the inverse function theorem guarantees a locally differentiable inverse near that point.

## 4. Chain Rule

> [!important] Matrix Form
> Suppose:
>
> $$\mathbf F:\mathbb R^n\to\mathbb R^m$$
>
> and:
>
> $$\mathbf G:\mathbb R^m\to\mathbb R^p$$
>
> Then:
>
> $$J_{\mathbf{G}\circ\mathbf F}(\mathbf x)
> =
> J_{\mathbf G}(\mathbf F(\mathbf x))
> J_{\mathbf F}(\mathbf x)$$
>
> The matrix multiplication order follows the composition of the mappings.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Partial Derivatives:** Supplies the matrix entries.
- **Total Differentiation:** Provides the linear approximation represented by the Jacobian.
- **Linear Algebra:** Provides matrix multiplication, rank, and determinants.

### Downstream Knowledge
- **Change of Variables:** Uses the Jacobian determinant to transform integration measures.
- **Inverse Function Theorem:** Uses Jacobian nonsingularity to establish local invertibility.
- **Differential Geometry:** Uses Jacobians to describe coordinate mappings and local transformations.