---
type: technical-term
title: Euclidean Space
aliases:
  - Euclidean Geometry Space
abbreviation: ""
field:
  - Mathematics
  - Geometry
  - Robotics
subfield:
  - Linear Algebra
  - Euclidean Geometry
  - Multivariable Calculus
status: learning
confidence: 1
created: 2026-10-31
updated: 2026-10-31
tags:
  - technical-term
  - mathematics
  - geometry
  - robotics
sources:
  - Euclid, Elements
  - Axler, Linear Algebra Done Right
projects: []
related:
  - "[[MOC - Euclidean Space]]"
---


## 1. Identification

> [!abstract] Definition
> **Euclidean space** is a real affine space equipped with a Euclidean inner product on its associated vector space. This structure allows geometric concepts such as distance, angle, length, and orthogonality to be defined consistently.
>
> In an \(n\)-dimensional Euclidean space, points can be represented using \(n\) real coordinates after choosing an origin and an orthonormal basis.

- **Preferred term:** Euclidean Space
- **Aliases:** Euclidean geometric space
- **Domain:** Mathematics, Geometry, Robotics
- **Subdomains:** Linear Algebra, Euclidean Geometry, Multivariable Calculus
- **Common notation:** \(\mathbb{E}^n\), with \(\mathbb{R}^n\) commonly used for its coordinate representation.
- **Dimension:** \(n\)

## 2. Definition and Core Concept

### 2.1 Mathematical Definition

> [!info] Formal definition
> An \(n\)-dimensional Euclidean space is an \(n\)-dimensional real affine space whose associated vector space is equipped with a positive-definite inner product.
>
> The associated vector space is commonly represented as \(\mathbb{R}^n\), with the standard Euclidean inner product:
>
> $$
> \langle \mathbf{u},\mathbf{v}\rangle
> =
> \sum_{i=1}^{n}u_i v_i
> =
> \mathbf{u}^{T}\mathbf{v}
> $$
>
> The inner product induces the Euclidean norm:
>
> $$
> \|\mathbf{u}\|_2
> =
> \sqrt{\langle\mathbf{u},\mathbf{u}\rangle}
> =
> \sqrt{\sum_{i=1}^{n}u_i^2}
> $$
>
> Consequently, the distance between two points \(P\) and \(Q\) is:
>
> $$
> d(P,Q)=\|\overrightarrow{PQ}\|_2
> $$

### 2.2 Geometric Intuition

> [!note] Intuition
> Euclidean space provides the mathematical setting for ordinary geometry.
>
> It allows us to describe:
> - **Points:** Locations in space.
> - **Vectors:** Displacements and directions.
> - **Lengths:** Magnitudes of vectors.
> - **Distances:** Separation between points.
> - **Angles:** Relative orientation between vectors.
> - **Orthogonality:** Perpendicular relationships.
> - **Lines and planes:** Geometric subsets of the space.
>
> The familiar two-dimensional plane and three-dimensional physical space are common examples.

### 2.3 Euclidean Space vs. Coordinate Space

> [!important] Important distinction
> Euclidean space is fundamentally a geometric structure, not merely a collection of coordinate tuples.
>
> A coordinate system assigns numerical coordinates to points after selecting an origin and a basis.
>
> The same geometric point can have different coordinate representations under different coordinate systems, while its geometric properties remain unchanged.
>
> For example, a point may have coordinates \((1,2,3)\) in one Cartesian frame and different coordinates in another frame without representing a different physical location.

## 3. Technical Representation

### 3.1 The Euclidean Vector Space

> [!info] Vector representation
> In the standard coordinate representation, an \(n\)-dimensional vector is written as:
>
> $$
> \mathbf{v}
> =
> \begin{bmatrix}
> v_1\\
> v_2\\
> \vdots\\
> v_n
> \end{bmatrix}
> \in\mathbb{R}^n
> $$
>
> Two vectors can be added:
>
> $$
> \mathbf{u}+\mathbf{v}
> =
> \begin{bmatrix}
> u_1+v_1\\
> \vdots\\
> u_n+v_n
> \end{bmatrix}
> $$
>
> A vector can also be multiplied by a real scalar:
>
> $$
> \alpha\mathbf{v}
> =
> \begin{bmatrix}
> \alpha v_1\\
> \vdots\\
> \alpha v_n
> \end{bmatrix}
> $$
>
> These operations define the underlying real vector-space structure.

### 3.2 Euclidean Inner Product

> [!info] Inner product
> The standard Euclidean inner product of two vectors is:
>
> $$
> \langle\mathbf{u},\mathbf{v}\rangle
> =
> \mathbf{u}^{T}\mathbf{v}
> =
> \sum_{i=1}^{n}u_i v_i
> $$
>
> It satisfies:
>
> 1. **Symmetry**
>    $$
>    \langle\mathbf{u},\mathbf{v}\rangle
>    =
>    \langle\mathbf{v},\mathbf{u}\rangle
>    $$
>
> 2. **Linearity**
>    $$
>    \langle a\mathbf{u}+b\mathbf{v},\mathbf{w}\rangle
>    =
>    a\langle\mathbf{u},\mathbf{w}\rangle
>    +
>    b\langle\mathbf{v},\mathbf{w}\rangle
>    $$
>
> 3. **Positive definiteness**
>    $$
>    \langle\mathbf{v},\mathbf{v}\rangle\geq0
>    $$
>    with equality if and only if \(\mathbf{v}=\mathbf{0}\).
>
> The inner product provides the foundation for defining vector lengths and angles.

### 3.3 Euclidean Norm

> [!info] Vector length
> The Euclidean norm, also called the \(L^2\)-norm, is:
>
> $$
> \|\mathbf{v}\|_2
> =
> \sqrt{\sum_{i=1}^{n}v_i^2}
> $$
>
> For a three-dimensional vector:
>
> $$
> \|\mathbf{v}\|_2
> =
> \sqrt{v_x^2+v_y^2+v_z^2}
> $$
>
> The norm measures the magnitude or length of a vector.

### 3.4 Euclidean Distance

> [!info] Distance between points
> Given two points:
>
> $$
> P=(p_1,p_2,\ldots,p_n)
> $$
>
> $$
> Q=(q_1,q_2,\ldots,q_n)
> $$
>
> Their Euclidean distance is:
>
> $$
> d(P,Q)
> =
> \sqrt{\sum_{i=1}^{n}(q_i-p_i)^2}
> $$
>
> In three dimensions:
>
> $$
> d(P,Q)
> =
> \sqrt{
> (q_x-p_x)^2+
> (q_y-p_y)^2+
> (q_z-p_z)^2
> }
> $$

### 3.5 Angle and Orthogonality

> [!info] Angle between vectors
> For two nonzero vectors \(\mathbf{u}\) and \(\mathbf{v}\), the angle between them is:
>
> $$
> \cos\theta
> =
> \frac{\mathbf{u}^{T}\mathbf{v}}
> {\|\mathbf{u}\|_2\|\mathbf{v}\|_2}
> $$
>
> Therefore:
>
> $$
> \theta
> =
> \cos^{-1}
> \left(
> \frac{\mathbf{u}^{T}\mathbf{v}}
> {\|\mathbf{u}\|_2\|\mathbf{v}\|_2}
> \right)
> $$
>
> Two vectors are orthogonal if:
>
> $$
> \mathbf{u}^{T}\mathbf{v}=0
> $$
>
> Orthogonal vectors are perpendicular under the Euclidean inner product.

### 3.6 Orthonormal Basis

> [!info] Basis representation
> An orthonormal basis consists of basis vectors that are mutually orthogonal and individually have unit length.
>
> For basis vectors \(\mathbf{e}_1,\ldots,\mathbf{e}_n\):
>
> $$
> \mathbf{e}_i^T\mathbf{e}_j
> =
> \delta_{ij}
> $$
>
> where \(\delta_{ij}\) is the Kronecker delta:
>
> $$
> \delta_{ij}
> =
> \begin{cases}
> 1 & i=j\\
> 0 & i\neq j
> \end{cases}
> $$
>
> Every vector can be expressed as:
>
> $$
> \mathbf{v}
> =
> \sum_{i=1}^{n}v_i\mathbf{e}_i
> $$
>
> An orthonormal basis makes coordinate calculations especially convenient.

### 3.7 The Euclidean Metric

> [!info] Metric structure
> The Euclidean distance defines a metric:
>
> $$
> d:\mathbb{E}^n\times\mathbb{E}^n
> \rightarrow\mathbb{R}_{\geq0}
> $$
>
> It satisfies four properties:
>
> 1. Non-negativity:
>    \(d(P,Q)\geq0\)
> 2. Identity of indiscernibles:
>    \(d(P,Q)=0\iff P=Q\)
> 3. Symmetry:
>    \(d(P,Q)=d(Q,P)\)
> 4. Triangle inequality:
>    \(d(P,R)\leq d(P,Q)+d(Q,R)\)
>
> Thus, Euclidean space is also a metric space.

## 4. Applications and Examples

### 4.1 Two-Dimensional Euclidean Space

> [!example] The Euclidean plane
> The two-dimensional Euclidean space is denoted by \(\mathbb{E}^2\).
>
> Its standard coordinate representation is \(\mathbb{R}^2\).
>
> For two points:
>
> $$
> P=(1,2),\qquad Q=(4,6)
> $$
>
> The distance is:
>
> $$
> d(P,Q)
> =
> \sqrt{(4-1)^2+(6-2)^2}
> =5
> $$

### 4.2 Three-Dimensional Euclidean Space

> [!example] Three-dimensional geometry
> Three-dimensional Euclidean space is denoted by \(\mathbb{E}^3\).
>
> Its standard coordinate representation is \(\mathbb{R}^3\).
>
> A point is represented by:
>
> $$
> P=(x,y,z)
> $$
>
> A displacement vector is:
>
> $$
> \mathbf{v}
> =
> \begin{bmatrix}
> v_x\\v_y\\v_z
> \end{bmatrix}
> $$
>
> Its Euclidean length is:
>
> $$
> \|\mathbf{v}\|_2
> =
> \sqrt{v_x^2+v_y^2+v_z^2}
> $$
>
> See Three-Dimensional Euclidean Space for the detailed three-dimensional formulation.

### 4.3 Robotics and Geometric Modeling

> [!example] Robotics applications
> Euclidean space is fundamental to robot modeling and spatial computation.
>
> Common applications include:
>
> - **Robot localization:** Representing robot positions in a geometric environment.
> - **Motion planning:** Computing distances between configurations or spatial locations.
> - **Obstacle avoidance:** Measuring separation between robot geometry and obstacles.
> - **Point-cloud processing:** Computing distances between 3D points.
> - **Formation control:** Maintaining desired distances between robots.
> - **Multi-robot coordination:** Representing relative positions between agents.
>
> For two robots \(i\) and \(j\), their Euclidean separation is:
>
> $$
> d_{ij}
> =
> \|\mathbf{p}_i-\mathbf{p}_j\|_2
> $$
>
> where \(\mathbf{p}_i,\mathbf{p}_j\in\mathbb{R}^3\) represent their positions in the same coordinate frame.

### 4.4 Coordinate Transformations

> [!example] Changing coordinate representations
> A point represented in one orthonormal Cartesian frame can be represented in another frame through a rigid transformation:
>
> $$
> \mathbf{p}'
> =
> \mathbf{R}\mathbf{p}+\mathbf{t}
> $$
>
> where:
>
> - \(\mathbf{p}\): Original point coordinates.
> - \(\mathbf{p}'\): Transformed point coordinates.
> - \(\mathbf{R}\): Rotation matrix.
> - \(\mathbf{t}\): Translation vector.
>
> A rigid transformation preserves Euclidean distances:
>
> $$
> \|\mathbf{p}'_1-\mathbf{p}'_2\|_2
> =
> \|\mathbf{p}_1-\mathbf{p}_2\|_2
> $$
>
> This property is essential in robotics, computer vision, and geometric reconstruction.


## 6. Limitations and Evaluation

### 6.1 Assumptions

> [!important] Mathematical assumptions
> Standard Euclidean geometry assumes:
>
> - The underlying scalar field is \(\mathbb{R}\).
> - The associated vector space is finite-dimensional.
> - The inner product is positive-definite.
> - The geometry is flat, with zero intrinsic curvature.
>
> These assumptions are appropriate for ordinary rigid-body geometry and many robotics applications.

### 6.2 Limitations

> [!warning] Limitations
> Euclidean space does not directly represent every possible geometric environment.
>
> - **Curved spaces:** A sphere's surface is not globally equivalent to a flat Euclidean plane under its intrinsic geometry.
> - **Non-Euclidean geometry:** Hyperbolic and spherical geometries use different geometric structures.
> - **Configuration spaces:** A robot's configuration space may combine Euclidean, circular, and other manifold structures.
> - **Physical spacetime:** Relativistic spacetime is not described by ordinary Euclidean geometry.
>
> In robotics, a position may lie in \(\mathbb{R}^3\), while an orientation belongs to the rotation group \(SO(3)\). Therefore, a robot's full pose is naturally represented in the rigid-motion group \(SE(3)\), rather than treated as an ordinary vector in \(\mathbb{R}^6\) with standard Euclidean geometry.

### 6.3 Evaluation

> [!success] When to use Euclidean space
> Euclidean space is appropriate when:
>
> - Spatial distances are measured using ordinary straight-line distance.
> - The environment can be approximated as flat.
> - Cartesian coordinates are suitable.
> - Geometric relationships must remain invariant under rigid transformations.
>
> For curved environments, non-Euclidean geometry, or constrained robot configurations, more general geometric structures may be necessary.

## 7. Verification and Evidence

> [!abstract] Established mathematical facts
> The following properties follow from the Euclidean inner-product structure:
>
> - The Euclidean norm is induced by the inner product.
> - The Euclidean distance is induced by the norm of point displacement.
> - The inner product determines angles and orthogonality.
> - Orthonormal coordinate transformations preserve inner products and Euclidean distances.
> - Euclidean space is a special case of a metric space.
>
> **Verification status:** The definitions and equations above are standard mathematical formulations.
>
> **Confidence:** 1/5 — initial learning-stage familiarity. This is a personal learning indicator, not a measure of mathematical validity.

## 8. Personal Notes

> [!question] Questions for further study
> - What is the precise distinction between a Euclidean vector space and a Euclidean affine space?
> - How does the Euclidean metric relate to the metric tensor?
> - Why is \(SE(3)\) a manifold and a Lie group rather than an ordinary Euclidean vector space?
> - How does Euclidean geometry differ from Riemannian geometry?
> - How are distances defined in robot configuration spaces?

## 9. References

1. Euclid. *Elements*. A foundational work on classical Euclidean geometry.
2. Axler, Sheldon. *Linear Algebra Done Right*. Springer. A modern treatment of finite-dimensional vector spaces and inner products.
3. Lee, John M. *Introduction to Smooth Manifolds*. Springer. Relevant to the distinction between Euclidean spaces, manifolds, and more general geometric structures.
4. do Carmo, Manfredo P. *Riemannian Geometry*. Birkhäuser. Relevant to the generalization of Euclidean geometry to curved spaces.

