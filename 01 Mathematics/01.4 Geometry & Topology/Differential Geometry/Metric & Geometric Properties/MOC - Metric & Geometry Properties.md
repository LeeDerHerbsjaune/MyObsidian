## 5. Knowledge Relationships

### 5.1. Prerequisite concepts

> [!info] Mathematical foundations
>
> - Three-Dimensional Euclidean Space — The space in which Euclidean metric properties are defined.
> - Vector]] — Mathematical representation of magnitude and direction.
> - Linear Algebra]] — Mathematical framework for vectors and matrices.
> - Inner Product — Defines angles and orthogonality.
> - Norm — Measures vector magnitude.
> - Euclidean Distance]] — Measures separation between points.
> - Coordinate Frame]] — Provides a reference system for geometric measurements.

### 5.2. Related concepts

> [!abstract] Knowledge graph
>
> **Metric geometry**
> - Metric Space]]
> - [[Euclidean Metric]]
> - Euclidean Distance]]
> - [[Vector Norm]]
> - Inner Product
> - Orthogonality]]
>
> **Geometric structures**
> - [[Collinearity]]
> - [[Coplanarity]]
> - [[Parallelism]]
> - [[Geometric Invariant]]
> - [[Orientation]]
>
> **Transformation theory**
> - Rigid Transformations and Rotations]]
> - Rotation Matrix]]
> - Special Orthogonal Group]]
> - Special Euclidean Group]]
> - Affine Transformation]]
> - Similarity Transformation]]
>
> **Robotics applications**
> - Point Cloud Registration]]
> - Robot Localization]]
> - Simultaneous Localization and Mapping]]
> - Formation Control]]
> - Collision Detection]]

### 5.3. Relationship with rigid transformations

> [!important] Fundamental relationship
> Metric properties provide the mathematical conditions that characterize rigid transformations.
>
> In Euclidean space, a transformation is an isometry if:
>
> $$
> d(f(\mathbf{p}_1),f(\mathbf{p}_2))
> =
> d(\mathbf{p}_1,\mathbf{p}_2)
> $$
>
> A rigid transformation in three-dimensional Euclidean space has the form:
>
> $$
> f(\mathbf{p})=\mathbf{R}\mathbf{p}+\mathbf{t}
> $$
>
> where:
>
> $$
> \mathbf{R}^T\mathbf{R}=\mathbf{I}
> $$
>
> If orientation preservation is additionally required:
>
> $$
> \det(\mathbf{R})=+1
> $$
>
> The resulting transformations form the group \(SE(3)\).

## 10. Knowledge Links and Further Development

> [!tip] Recommended next notes
>
> **Level 1 — Euclidean geometry**
> - Three-Dimensional Euclidean Space
> - Euclidean Distance]]
> - [[Vector Norm]]
> - Inner Product
> - Orthogonality]]
>
> **Level 2 — Geometric transformations**
> - [[Rigid Transformations and Rotations]]
> - [[Isometry]]
> - [[Geometric Invariant]]
> - [[Rotation Matrix]]
> - [[Special Euclidean Group]]
>
> **Level 3 — Advanced geometry**
> - Metric Tensor]]
> - Metric Space]]
> - Differential Geometry
> - Riemannian Geometry
> - Lie Group]]
>
> **Level 4 — Robotics applications**
> - Point Cloud Registration]]
> - Robot Localization]]
> - Simultaneous Localization and Mapping]]
> - Formation Control]]
> - Geometric Control]]
>
> **Suggested learning sequence:**
>
> Three-Dimensional Euclidean Space
> → Vector Norm
> → Inner Product
> → Euclidean Distance
> → Metric and Geometric Properties
> → Rigid Transformations and Rotations
> → Geometric Invariants
> → Special Euclidean Group
> → Point Cloud Registration.