---
type: technical-term
title: Tensor Calculus
aliases:
  - Tensor Analysis
  - Differential Calculus of Tensors
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Tensor Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - tensor-calculus
  - differential-geometry
sources:
  - Schutz (1980), Geometrical Methods of Mathematical Physics
  - Lee (2018), Introduction to Riemannian Manifolds
related:
  - "[[Tensors]]"
  - "[[Tensor Types and Ranks]]"
  - "[[Tensor Components and Transformation Laws]]"
  - "[[Tensor Product]]"
  - "[[Tensor Contraction]]"
  - "[[Index Notation]]"
  - "[[Index Raising and Lowering]]"
  - "[[Tensor Fields]]"
  - "[[Metric Tensor]]"
  - "[[Christoffel Symbols]]"
  - "[[Covariant Derivatives]]"
  - "[[Parallel Transport]]"
  - "[[Riemann Curvature Tensor]]"
  - "[[Ricci Tensor]]"
  - "[[Scalar Curvature]]"
projects: []
---

> [!abstract] Definition
> **Tensor Calculus** is the mathematical framework for studying tensors and tensor fields, including their coordinate transformations, algebraic operations, differentiation, and geometric properties.
>
> It extends vector and matrix operations to general multilinear objects and provides coordinate-independent mathematical descriptions of geometric and physical quantities.
>
> Tensor calculus is especially important in differential geometry, continuum mechanics, and mathematical physics.

> [!important] Core Concept
> A tensor is a multilinear object that transforms according to a specific law under changes of coordinates.
>
> In a finite-dimensional vector space $V$, a tensor of type $(r,s)$ belongs to
>
> $$
> T\in V^{\otimes r}\otimes(V^*)^{\otimes s}
> $$
>
> where:
> - $V$ is a vector space.
> - $V^*$ is its dual space.
> - $r$ is the contravariant rank.
> - $s$ is the covariant rank.
>
> A tensor's components depend on the chosen basis, but the underlying tensor is independent of that basis.

> [!note] Tensor Components
> A tensor of type $(r,s)$ can be represented using components:
>
> $$
> T^{i_1\cdots i_r}{}_{j_1\cdots j_s}
> $$
>
> Upper indices represent contravariant components, while lower indices represent covariant components.
>
> These index positions encode how the components transform under coordinate changes.

> [!important] Tensor Transformation Law
> Under a coordinate transformation from $x^i$ to $x'^i$, a tensor transforms according to
>
> $$
> \begin{aligned}
> T'^{i_1\cdots i_r}{}_{j_1\cdots j_s}
> &=
> \frac{\partial x'^{i_1}}{\partial x^{k_1}}
> \cdots
> \frac{\partial x'^{i_r}}{\partial x^{k_r}}\\
> &\quad\times
> \frac{\partial x^{l_1}}{\partial x'^{j_1}}
> \cdots
> \frac{\partial x^{l_s}}{\partial x'^{j_s}}
> T^{k_1\cdots k_r}{}_{l_1\cdots l_s}
> \end{aligned}
> $$
>
> Every contravariant index transforms with the Jacobian of the new coordinates with respect to the old coordinates.
>
> Every covariant index transforms with the inverse Jacobian.

> [!note] Tensor Rank and Type
> The type $(r,s)$ specifies the number of contravariant and covariant indices.
>
> Examples:
> - Scalar: type $(0,0)$.
> - Vector: type $(1,0)$.
> - Covector: type $(0,1)$.
> - Linear operator represented as a bilinear tensor: type $(1,1)$.
> - Metric tensor: type $(0,2)$.
>
> The total rank is $r+s$.

> [!important] Fundamental Operations
> Tensor calculus includes several fundamental operations:
>
> - **Tensor Addition:** Adds tensors of the same type.
> - **Scalar Multiplication:** Multiplies a tensor by a scalar.
> - **Tensor Product:** Combines tensors to produce a tensor of higher rank.
> - **Contraction:** Pairs one contravariant and one covariant index, reducing tensor rank by two.
> - **Index Raising and Lowering:** Uses the metric tensor and its inverse to change index positions.
> - **Symmetrization and Antisymmetrization:** Extracts symmetric or antisymmetric components.

> [!important] Einstein Summation Convention
> Repeated indices appearing once in an upper position and once in a lower position imply summation.
>
> For example:
>
> $$
> a^i b_i=\sum_{i=1}^{n}a^i b_i
> $$
>
> This convention simplifies tensor expressions and is widely used in differential geometry and mathematical physics.

> [!important] Metric Tensor
> A metric tensor defines an inner product on tangent spaces.
>
> Its components are written as
>
> $$
> g_{ij}
> $$
>
> The squared infinitesimal distance is
>
> $$
> ds^2=g_{ij}\,dx^i dx^j
> $$
>
> The inverse metric $g^{ij}$ satisfies
>
> $$
> g^{ik}g_{kj}=\delta^i_j
> $$
>
> The metric enables index raising and lowering:
>
> $$
> v_i=g_{ij}v^j
> $$
>
> $$
> v^i=g^{ij}v_j
> $$

> [!important] Tensor Fields
> A tensor field assigns a tensor to each point of a differentiable manifold.
>
> For example:
> - A vector field assigns a tangent vector to every point.
> - A covector field assigns a cotangent vector to every point.
> - A metric tensor field assigns an inner product to every tangent space.
>
> Tensor fields provide the objects on which differential tensor calculus operates.

> [!important] Covariant Differentiation
> Ordinary partial derivatives of tensor components do not generally transform as tensor components under arbitrary coordinate transformations.
>
> Covariant differentiation corrects this problem by incorporating connection coefficients.
>
> For a contravariant vector field:
>
> $$
> \nabla_j V^i
> =
> \partial_j V^i
> +
> \Gamma^i_{jk}V^k
> $$
>
> For a covariant vector field:
>
> $$
> \nabla_j V_i
> =
> \partial_j V_i
> -
> \Gamma^k_{ji}V_k
> $$
>
> Here, $\Gamma^i_{jk}$ are the connection coefficients.

> [!note] Curvature and Geometry
> Covariant differentiation allows the construction of curvature tensors.
>
> The Riemann curvature tensor measures the failure of covariant derivatives to commute:
>
> $$
> (\nabla_k\nabla_l-\nabla_l\nabla_k)V^i
> =
> R^i{}_{jkl}V^j
> $$
>
> The Riemann curvature tensor, Ricci tensor, and scalar curvature describe important geometric properties of a manifold.

> [!note] Tensor Calculus on Manifolds
> On differentiable manifolds, tensors are defined intrinsically on tangent and cotangent spaces.
>
> Coordinate systems provide local component representations, while the underlying tensor objects remain geometrically well-defined.
>
> This distinction allows tensor calculus to operate beyond ordinary Euclidean coordinate spaces.

> [!warning] Important Distinctions
> - A tensor is not merely an array of numbers; its transformation law is essential.
> - Tensor components are coordinate-dependent, but the tensor itself is coordinate-independent.
> - Partial derivatives of tensor components are not generally tensors.
> - Covariant differentiation requires a connection.
> - A metric is an additional geometric structure, not a requirement for defining every tensor.
> - Curvature depends on the connection; metric curvature specifically involves a metric-compatible connection such as the Levi-Civita connection.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Linear Algebra — provides vector spaces, dual spaces, multilinear maps, and tensor products.
> - Multivariable Calculus — provides partial derivatives, Jacobians, and coordinate transformations.
> - Differential Geometry — provides manifolds, tangent spaces, and cotangent spaces.
> - Real Analysis — supports rigorous treatment of differentiability and continuity.

> **Downstream Knowledge**
> - Tensor Fields — studies tensor-valued fields on manifolds.
> - Covariant Derivatives — develops differentiation of tensor fields.
> - Riemannian Geometry — studies manifolds equipped with metric tensors.
> - Riemann Curvature Tensor — develops curvature through covariant differentiation.
> - Differential Forms — develops antisymmetric covariant tensor fields and exterior calculus.
> - Continuum Mechanics — applies tensor operations to stress, strain, and deformation.
> - General Relativity — uses spacetime tensors to formulate gravitational geometry.

> [!quote] References
> - Schutz, B. F. (1980). *Geometrical Methods of Mathematical Physics*.
> - Lee, J. M. (2018). *Introduction to Riemannian Manifolds*, 2nd edition.
> - Bishop, R. L., and Goldberg, S. I. (1968). *Tensor Analysis on Manifolds*.
> - Wald, R. M. (1984). *General Relativity*.