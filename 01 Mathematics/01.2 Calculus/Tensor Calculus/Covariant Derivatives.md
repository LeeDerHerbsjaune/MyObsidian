---
type: technical-term
title: "Covariant Derivatives"
aliases:
  - Covariant Differentiation
  - Covariant Derivative
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Tensor Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - tensor-calculus
sources:
  - "Lee (2018), Introduction to Riemannian Manifolds"
  - "Wald (1984), General Relativity"
related: []
projects: []
---

> [!abstract] Definition
> A **covariant derivative** is a differentiation operation on tensor fields that accounts for the variation of the underlying coordinate basis and preserves tensorial transformation behavior.
>
> It is defined through a connection on the tangent bundle.

> [!important] Vector Field
> For a vector field $V^i$, its covariant derivative is
>
> $$\nabla_jV^i
> =
> \partial_jV^i+\Gamma^i_{jk}V^k$$
>
> The partial derivative differentiates the component functions, while the Christoffel term accounts for the changing basis.

> [!note] Covector Field
> For a covector field $\omega_i$,
>
> $$\nabla_j\omega_i
> =
> \partial_j\omega_i-\Gamma^k_{ji}\omega_k$$
>
> The connection term has the opposite sign for a covariant index.

> [!important] General Tensor Field
> For a tensor of type $(r,s)$,
>
> $$\begin{aligned}
> \nabla_k T^{i_1\cdots i_r}_{j_1\cdots j_s}
> ={}&
> \partial_k T^{i_1\cdots i_r}_{j_1\cdots j_s}\\
> &+\sum_{a=1}^{r}
> \Gamma^{i_a}_{km}
> T^{i_1\cdots m\cdots i_r}_{j_1\cdots j_s}\\
> &-\sum_{b=1}^{s}
> \Gamma^m_{k j_b}
> T^{i_1\cdots i_r}_{j_1\cdots m\cdots j_s}
> \end{aligned}$$
>
> Each upper index contributes a positive connection term, and each lower index contributes a negative connection term.

> [!note] Important Properties
> Covariant differentiation satisfies:
> - Linearity.
> - The Leibniz product rule.
> - Compatibility with tensor contraction.
> - Tensorial transformation behavior.
>
> For a scalar field $f$,
>
> $$\nabla_i f=\partial_i f$$
>
> The covariant derivative of a scalar is its ordinary differential.

> [!note] Metric Compatibility
> For the Levi-Civita connection,
>
> $$\nabla_k g_{ij}=0$$
>
> This means the metric is preserved under parallel differentiation.
>
> The Levi-Civita connection is uniquely determined by metric compatibility and zero torsion.

> [!warning] Covariant Derivative Versus Partial Derivative
> The ordinary partial derivative of tensor components is generally not tensorial.
>
> The covariant derivative includes connection terms to compensate for the coordinate dependence of the basis.
>
> In Cartesian coordinates on Euclidean space, Christoffel symbols vanish, so the expressions may coincide locally.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Tensor Fields — defines the differentiable objects.
> - Christoffel Symbols — provides coordinate connection coefficients.
> - Differential Geometry — supplies connections and tangent bundles.
>
> **Downstream Knowledge**
> - Parallel Transport — defined by vanishing covariant derivative along a curve.
> - Riemann Curvature Tensor — measures the noncommutativity of covariant derivatives.
> - Riemannian Geometry — uses covariant differentiation as a central operation.