---
type: technical-term
title: "Fractional Integrals and Derivatives of Several Variables"
aliases:
  - Multivariable Fractional Calculus
  - Multidimensional Fractional Calculus
field:
  - Mathematics
subfield:
  - Fractional Calculus
  - Multivariable Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - fractional-calculus
  - multivariable-calculus
sources:
  - "Samko, Kilbas, and Marichev (1993), Fractional Integrals and Derivatives"
  - "Meerschaert and Sikorskii (2012), Stochastic Models for Fractional Calculus"
related: []
projects: []
---

> [!abstract] Definition
> **Fractional integrals and derivatives of several variables** extend fractional-order integration and differentiation to functions defined on multidimensional domains.
>
> They generalize one-dimensional fractional operators to functions such as
>
> $$
> u:\Omega\subseteq\mathbb{R}^n\rightarrow\mathbb{R}
> $$
>
> The construction depends on the chosen multidimensional operator, domain geometry, and boundary conditions.

> [!important] Coordinate-Wise Fractional Operators
> One approach defines fractional derivatives separately with respect to each coordinate.
>
> For a function $u(x_1,\ldots,x_n)$, a coordinate-wise operator may be written as
>
> $$
> D_{x_i}^{\alpha}u
> $$
>
> Each operator differentiates fractionally with respect to one coordinate while treating the remaining coordinates as parameters.
>
> For example, a two-variable function can have separate fractional derivatives:
>
> $$
> D_x^\alpha u(x,y),
> \qquad
> D_y^\beta u(x,y)
> $$
>
> The orders $\alpha$ and $\beta$ need not be equal.

> [!note] Multidimensional Fractional Integrals
> A multidimensional fractional integral can be constructed using product kernels.
>
> For example, a coordinate-wise left-sided fractional integral on a rectangular domain may be expressed as
>
> $$
> \begin{aligned}
> &(I_{a_1+}^{\alpha_1}\cdots
> I_{a_n+}^{\alpha_n}u)(\mathbf{x})\\
> &=
> \prod_{i=1}^{n}\frac{1}{\Gamma(\alpha_i)}
> \int_{a_1}^{x_1}\cdots
> \int_{a_n}^{x_n}
> \left[
> \prod_{i=1}^{n}
> (x_i-t_i)^{\alpha_i-1}
> \right]
> u(\mathbf{t})\,d\mathbf{t}
> \end{aligned}
> $$
>
> where $\alpha_i>0$ are the integration orders along the respective coordinates.
>
> This is one construction, not a universal definition for every multidimensional fractional integral.

> [!important] Fractional Laplacian
> An important multidimensional fractional operator is the fractional Laplacian:
>
> $$
> \mathcal{F}\left[(-\Delta)^s u\right](\boldsymbol{\xi})
> =
> |\boldsymbol{\xi}|^{2s}
> \widehat{u}(\boldsymbol{\xi}),
> \qquad 0<s<1
> $$
>
> Here:
> - $\Delta$ is the ordinary Laplacian.
> - $s$ is the fractional order parameter.
> - $\boldsymbol{\xi}$ is the multidimensional frequency variable.
>
> Unlike coordinate-wise fractional derivatives, the fractional Laplacian is isotropic: its Fourier symbol depends on the magnitude of the frequency vector.

> [!note] Anisotropic and Isotropic Operators
> - **Coordinate-wise operators** can assign different orders to different coordinate directions.
> - **Isotropic operators** treat spatial directions symmetrically.
> - **Anisotropic operators** allow directional differences in the operator's behavior.
>
> These constructions encode different mathematical assumptions and should not be treated as equivalent.

> [!important] Function Spaces and Domains
> Multidimensional fractional operators are often studied using:
> - Fractional Sobolev spaces.
> - Lebesgue spaces.
> - Distribution spaces.
> - Bounded and unbounded spatial domains.
>
> For bounded domains, the definition of the operator must specify how boundary conditions or values outside the domain are handled.

> [!warning] Limitations
> - There is no single universal multidimensional fractional derivative.
> - Coordinate-wise and isotropic operators can produce different results.
> - Boundary conditions are more involved than in one-dimensional problems.
> - Operator equivalence depends on the domain, function space, and boundary assumptions.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Integrals — provides the one-dimensional and iterated integral constructions.
> - Fractional Derivatives — provides the derivative definitions.
> - Multivariable Calculus — provides the multidimensional function and coordinate framework.
> - Fourier Analysis — supports the Fourier definition of isotropic operators.
> - Functional Analysis — provides the function-space framework.
>
> **Downstream Knowledge**
> - Fractional PDEs — applies multidimensional fractional operators to partial differential equations.
> - Fractional Laplacian — develops an important isotropic multidimensional operator.
> - Fractional Sobolev Spaces — provides the natural function spaces for many multidimensional fractional problems.
> - Nonlocal Analysis — studies the broader theory of spatially nonlocal operators.

> [!quote] References
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*.
> - Meerschaert, M. M., and Sikorskii, A. (2012). *Stochastic Models for Fractional Calculus*.