---
type: technical-term
title: Three-Dimensional Euclidean Space
aliases:
  - 3D Euclidean Space
  - Euclidean 3-Space
  - Three-Dimensional Euclidean Space
abbreviation: E³
field:
  - Mathematics
  - Geometry
  - Physics
subfield:
  - Euclidean Geometry
  - Linear Algebra
  - Analytic Geometry
status: learning
confidence: 1
created: 2026-10-30
updated: 2026-10-30
tags:
  - technical-term
  - mathematics
  - geometry
  - three-dimensional-space
sources:
  - https://link.springer.com/book/10.1007/978-1-4419-9982-5
projects: []
related:
  - "[[MOC - Three-Dimensional Euclid Space]]"
---
## 1. Identification

> [!abstract] Definition and Identification
> - **Preferred term:** Three-Dimensional Euclidean Space
> - **Abbreviation:** 3D Euclidean Space
> - **Mathematical notation:** $\mathbb{E}^3$, commonly represented by $\mathbb{R}^3$ with the standard Euclidean metric.
> - **Domain:** Mathematics
> - **Subdomains:** Euclidean Geometry, Linear Algebra, Analytic Geometry.
>
> Three-dimensional Euclidean space is a geometric space with three independent spatial dimensions, equipped with an inner product that defines distances, angles, and orthogonality.

## 2. Definition and Core Concept

### 2.1 Formal Definition

> [!abstract] Mathematical Definition
> Three-dimensional Euclidean space is a three-dimensional affine space over the real numbers whose associated vector space is equipped with a positive-definite inner product.
>
> Its standard Cartesian representation is:
>
> $$
> \mathbb{R}^3 =
> \left\{
> (x,y,z)\mid x,y,z\in\mathbb{R}
> \right\}
> $$
>
> Each point is represented by an ordered triple:
>
> $$
> P=(x,y,z)
> $$
>
> where:
> - $x$: coordinate along the $X-axis$.
> - $y$: coordinate along the $Y-axis$.
> - $z$: coordinate along the $Z-axis$.
>
> The three coordinate axes are mutually perpendicular in the standard Cartesian coordinate system.

### 2.2 Geometric Intuition

> [!info] Intuition
> Two-dimensional Euclidean space describes positions on a plane, whereas three-dimensional Euclidean space extends this representation into a third independent spatial direction.
>
> It provides the mathematical framework for describing:
> - The position of objects in physical space.
> - Distances between points.
> - Directions and angles.
> - Geometric shapes and surfaces.
> - Spatial relationships between objects.
>
> For example, the position of a robot operating in a room can be represented by three coordinates corresponding to its location along the $X, Y$, and $Z$ axes.

### 2.3 Fundamental Properties

> [!note] Properties
> 1. **Dimension:** Three.
> 2. **Underlying field:** Real numbers $\mathbb{R}$.
> 3. **Coordinate representation:** Three real-valued coordinates.
> 4. **Metric:** Standard Euclidean metric.
> 5. **Geometry:** Flat Euclidean geometry.
> 6. **Homogeneity:** All points have equivalent geometric structure.
> 7. **Isotropy:** The geometry does not intrinsically prefer any spatial direction.
> 8. **Continuity:** Coordinates can take arbitrary real values.
>
> Euclidean space is not inherently restricted to Cartesian coordinates. Cartesian coordinates are one particular representation of its geometry.

## 3. Technical Representation

### 3.1 Cartesian Coordinate System

> [!abstract] Cartesian Representation
> A point in three-dimensional Euclidean space can be represented by a coordinate vector:
>
> $$
> \mathbf{p}=
> \begin{bmatrix}
> x\\
> y\\
> z
> \end{bmatrix}
> $$
>
> The standard basis vectors are:
>
> $$
> \mathbf{e}_x=
> \begin{bmatrix}
> 1\\0\\0
> \end{bmatrix},
> \quad
> \mathbf{e}_y=
> \begin{bmatrix}
> 0\\1\\0
> \end{bmatrix},
> \quad
> \mathbf{e}_z=
> \begin{bmatrix}
> 0\\0\\1
> \end{bmatrix}
> $$
>
> Therefore:
>
> $$
> \mathbf{p}
> =
> x\mathbf{e}_x+
> y\mathbf{e}_y+
> z\mathbf{e}_z
> $$
>
> The basis vectors are orthonormal:
>
> $$
> \mathbf{e}_i^T\mathbf{e}_j
> =
> \delta_{ij}
> $$
>
> where $\delta_{ij}$ is the Kronecker delta.

### 3.2 Euclidean Distance

> [!abstract] Distance Between Two Points
> Given two points:
>
> $$
> P_1=(x_1,y_1,z_1)
> $$
>
> $$
> P_2=(x_2,y_2,z_2)
> $$
>
> Their Euclidean distance is:
>
> $$
> d(P_1,P_2)=
> \sqrt{
> (x_2-x_1)^2+
> (y_2-y_1)^2+
> (z_2-z_1)^2
> }
> $$
>
> This equation is the three-dimensional extension of the Pythagorean theorem.
>
> The distance is always non-negative and equals zero if and only if the two points coincide.

### 3.3 Euclidean Norm

> [!abstract] Vector Magnitude
> For a vector:
>
> $$
> \mathbf{v}=
> \begin{bmatrix}
> v_x\\v_y\\v_z
> \end{bmatrix}
> $$
>
> Its Euclidean norm, also called the $L_2-norm$, is:
>
> $$
> \|\mathbf{v}\|_2
> =
> \sqrt{v_x^2+v_y^2+v_z^2}
> $$
>
> The norm represents the magnitude or length of a vector.
>
> For two points represented in the same Cartesian coordinate system:
>
> $$
> d(P_1,P_2)=\|\mathbf{p}_2-\mathbf{p}_1\|_2
> $$

### 3.4 Euclidean Inner Product

> [!abstract] Inner Product
> The standard Euclidean inner product between two vectors is:
>
> $$
> \langle\mathbf{u},\mathbf{v}\rangle
> =
> u_xv_x+u_yv_y+u_zv_z
> $$
>
> In matrix notation:
>
> $$
> \langle\mathbf{u},\mathbf{v}\rangle
> =
> \mathbf{u}^T\mathbf{v}
> $$
>
> The inner product allows the calculation of angles and the identification of orthogonal vectors.
>
> The angle between two nonzero vectors is:
>
> $$
> \cos\theta=
> \frac{
> \mathbf{u}^T\mathbf{v}
> }{
> \|\mathbf{u}\|_2\|\mathbf{v}\|_2
> }
> $$
>
> Two vectors are orthogonal if:
>
> $$
> \mathbf{u}^T\mathbf{v}=0
> $$

### 3.5 Euclidean Metric

> [!important] Metric Tensor
> The Euclidean metric defines how distances and angles are measured in space.
>
> In standard Cartesian coordinates, the metric tensor is:
>
> $$
> \mathbf{G}=
> \begin{bmatrix}
> 1&0&0\\
> 0&1&0\\
> 0&0&1
> \end{bmatrix}
> =\mathbf{I}_3
> $$
>
> The squared infinitesimal distance is:
>
> $$
> ds^2=dx^2+dy^2+dz^2
> $$
>
> More generally:
>
> $$
> ds^2=d\mathbf{x}^T
> \mathbf{G}\,d\mathbf{x}
> $$
>
> where:
> - \(ds\): infinitesimal distance.
> - \(d\mathbf{x}\): infinitesimal coordinate displacement.
> - \(\mathbf{G}\): metric tensor.
>
> In Cartesian coordinates, the standard Euclidean metric is represented by the identity matrix.

### 3.6 Vector Operations

> [!info] Fundamental Operations
> Given two vectors:
>
> $$
> \mathbf{u}=
> \begin{bmatrix}
> u_x\\u_y\\u_z
> \end{bmatrix},
> \quad
> \mathbf{v}=
> \begin{bmatrix}
> v_x\\v_y\\v_z
> \end{bmatrix}
> $$
>
> **Vector addition:**
>
> $$
> \mathbf{u}+\mathbf{v}
> =
> \begin{bmatrix}
> u_x+v_x\\
> u_y+v_y\\
> u_z+v_z
> \end{bmatrix}
> $$
>
> **Scalar multiplication:**
>
> $$
> \alpha\mathbf{v}
> =
> \begin{bmatrix}
> \alpha v_x\\
> \alpha v_y\\
> \alpha v_z
> \end{bmatrix}
> $$
>
> **Cross product:**
>
> $$
> \mathbf{u}\times\mathbf{v}
> =
> \begin{bmatrix}
> u_yv_z-u_zv_y\\
> u_zv_x-u_xv_z\\
> u_xv_y-u_yv_x
> \end{bmatrix}
> $$
>
> The cross product produces a vector perpendicular to both input vectors, following the right-hand rule.

## 4. Applications and Examples

### 4.1 Geometric Example

> [!example] Calculating Euclidean Distance
> Consider two points:
>
> $$
> A=(1,2,3)
> $$
>
> $$
> B=(4,6,3)
> $$
>
> Their distance is:
>
> $$
> \begin{aligned}
> d(A,B)
> &=\sqrt{(4-1)^2+(6-2)^2+(3-3)^2}\\
> &=\sqrt{9+16}\\
> &=\sqrt{25}\\
> &=5
> \end{aligned}
> $$
>
> Therefore, the Euclidean distance between \(A\) and \(B\) is \(5\) units.

### 4.2 Applications in Robotics

> [!info] Robotics Applications
> Three-dimensional Euclidean space is fundamental to robotics because physical robots operate and interact within three-dimensional environments.
>
> **1. Robot Position**
>
> The position of a robot can be represented as:
>
> $$
> \mathbf{p}=
> \begin{bmatrix}
> x\\y\\z
> \end{bmatrix}
> $$
>
> **2. Distance Measurement**
>
> Euclidean distance can be used to estimate the separation between robots, obstacles, targets, and neighboring agents.
>
> **3. Motion Planning**
>
> A time-dependent trajectory can be represented as:
>
> $$
> \mathbf{p}(t)=
> \begin{bmatrix}
> x(t)\\y(t)\\z(t)
> \end{bmatrix}
> $$
>
> **4. Coordinate Transformations**
>
> Robotics systems use transformations to express positions between coordinate frames, such as:
> - World frame.
> - Robot frame.
> - Sensor frame.
> - End-effector frame.
>
> **5. Multi-Robot Systems**
>
> In swarm robotics, Euclidean geometry provides a foundation for:
> - Relative-position estimation.
> - Inter-robot distance measurement.
> - Spatial formation control.
> - Collision avoidance.
> - Neighbor detection.
> - Three-dimensional trajectory planning.


## 6. Limitations and Evaluation

> [!warning] Assumptions and Limitations
> Three-dimensional Euclidean space is an ideal mathematical model.
>
> Its standard formulation assumes:
> - Flat geometry.
> - Three independent spatial dimensions.
> - A positive-definite Euclidean metric.
> - Standard Euclidean distance and angle relationships.
>
> It does not inherently model:
> - Curved geometric spaces.
> - Non-Euclidean geometry.
> - Spacetime geometry in general relativity.
> - Measurement uncertainty.
> - Robot orientation as part of its position representation.
>
> In robotics, position alone is insufficient to describe the complete configuration of a rigid body. Orientation must also be represented, typically using rotation matrices, quaternions, or other rotational representations.

## 7. Verification and Evidence

> [!success] Established Mathematical Results
> The following statements are standard mathematical results:
>
> 1. Three-dimensional Cartesian space is represented by \(\mathbb{R}^3\).
> 2. The standard Euclidean inner product is the dot product.
> 3. The standard Cartesian metric tensor is the identity matrix.
> 4. Euclidean distance follows the three-dimensional Pythagorean theorem.
> 5. Orthogonality is characterized by a zero inner product.
> 6. The cross product of two vectors in three dimensions is perpendicular to both vectors, provided the result is nonzero.
>
> **Verification status:** Established mathematical foundations.
>
> **Confidence:** High for the mathematical definitions and equations.

## 8. Personal Notes

> [!question] Learning Questions
> - What is the precise difference between \(\mathbb{R}^3\) and \(\mathbb{E}^3\)?
> - Why is Euclidean space defined as an affine space rather than simply a vector space?
> - How does the Euclidean metric change when using cylindrical or spherical coordinates?
> - How is three-dimensional Euclidean space used to construct a robot's configuration space?
> - Why is robot orientation represented by \(SO(3)\) rather than another copy of \(\mathbb{R}^3\)?
> - How does Euclidean geometry support distributed spatial coordination in swarm robotics?

## 9. References

> [!info] Recommended References
>
> 1. Lee, J. M. (2012). *Introduction to Smooth Manifolds* (2nd ed.). Springer.
>    - URL: https://link.springer.com/book/10.1007/978-1-4419-9982-5
>
> 2. Munkres, J. R. (1991). *Analysis on Manifolds*. Westview Press.
>
> 3. Strang, G. *Introduction to Linear Algebra*. Wellesley-Cambridge Press.
>
> **Note:** These references provide mathematical foundations for Euclidean geometry, linear algebra, inner products, and related geometric structures. Specific edition and publication details should be checked against the edition being used.


## Core Takeaway

> [!summary] Summary
> Three-dimensional Euclidean space is a three-dimensional affine space equipped with a Euclidean inner product. It provides the mathematical foundation for representing spatial positions, distances, directions, angles, and geometric relationships.
>
> In robotics, it is fundamental to coordinate systems, spatial measurements, motion planning, robot localization, and multi-robot coordination.
>
> It should be distinguished from a robot's complete configuration space, which must also account for orientation and other degrees of freedom.