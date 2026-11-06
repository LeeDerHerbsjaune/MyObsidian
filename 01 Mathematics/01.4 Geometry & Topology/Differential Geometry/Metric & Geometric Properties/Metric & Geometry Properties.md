---
type: technical-term
title: Metric and Geometric Properties
aliases:
  - Metric Properties
  - Geometric Invariants
  - Euclidean Geometric Properties
abbreviation: ""
field:
  - Mathematics
  - Geometry
  - Robotics
subfield:
  - Euclidean Geometry
  - Differential Geometry
  - Robot Kinematics
  - Computer Vision
status: learning
confidence: 1
created: 2026-10-31
updated: 2026-10-31
tags:
  - technical-term
  - mathematics
  - geometry
  - metric
  - robotics
  - rigid-body-motion
sources: []
projects: []
related:
  - "[[MOC - Metric & Geometry Properties]]"
---


## 1. Identification

> [!abstract] Definition
> **Metric and geometric properties** describe the mathematical characteristics of points, vectors, curves, surfaces, and spatial objects.
>
> Metric properties concern quantities that can be measured, such as distances, angles, lengths, and areas.
>
> Geometric properties describe broader structural relationships, including incidence, collinearity, parallelism, orthogonality, orientation, and spatial configuration.
>
> In Euclidean geometry, these properties provide the mathematical foundation for describing spatial relationships and determining which characteristics remain invariant under geometric transformations.

- **Domain:** Mathematics and Geometry.
- **Subdomains:** Euclidean Geometry, Linear Algebra, Differential Geometry.
- **Robotics applications:** Spatial modeling, coordinate transformations, localization, mapping, and motion planning.
- **Fundamental mathematical structures:** Inner products, norms, distance functions, and transformation groups.

## 2. Definition and Core Concepts

### 2.1. Metric properties

> [!abstract] Metric properties
> A metric property is a geometric characteristic defined through a measurement or a mathematical metric.
>
> In Euclidean space, important metric properties include:
>
> - Distance between points.
> - Length of vectors and curves.
> - Angles between vectors.
> - Areas and volumes.
> - Perpendicularity and orthogonality.
>
> These properties allow geometric objects to be compared quantitatively.

### 2.2. Geometric properties

> [!abstract] Geometric properties
> Geometric properties describe relationships and structural characteristics of geometric objects.
>
> Examples include:
>
> - Collinearity: Multiple points lie on the same straight line.
> - Coplanarity: Multiple points lie in the same plane.
> - Parallelism: Two lines or directions do not intersect under the relevant geometric assumptions.
> - Perpendicularity: Two directions form a right angle.
> - Incidence: A point belongs to a line, plane, or other geometric object.
> - Orientation: The directional arrangement of a geometric object or coordinate frame.
>
> Some geometric properties are metric-dependent, while others can be described without introducing a distance or angle measurement.

### 2.3. Metric space

> [!info] Metric space
> A metric space is a set equipped with a distance function that measures the separation between any two elements.
>
> Let \(X\) be a nonempty set. A metric is a function:
>
> $$
> d:X\times X\rightarrow\mathbb{R}_{\geq 0}
> $$
>
> satisfying four properties:
>
> **1. Non-negativity**
>
> $$
> d(x,y)\geq 0
> $$
>
> **2. Identity of indiscernibles**
>
> $$
> d(x,y)=0\iff x=y
> $$
>
> **3. Symmetry**
>
> $$
> d(x,y)=d(y,x)
> $$
>
> **4. Triangle inequality**
>
> $$
> d(x,z)\leq d(x,y)+d(y,z)
> $$
>
> These conditions define the mathematical concept of distance independently of any particular coordinate system.

### 2.4. Euclidean metric

> [!important] Euclidean distance
> In three-dimensional Euclidean space, the distance between two points is defined using the Euclidean norm.
>
> Let:
>
> $$
> \mathbf{p}_1=
> \begin{bmatrix}
> x_1\\y_1\\z_1
> \end{bmatrix},
> \qquad
> \mathbf{p}_2=
> \begin{bmatrix}
> x_2\\y_2\\z_2
> \end{bmatrix}
> $$
>
> Their Euclidean distance is:
>
> $$
> \boxed{
> d(\mathbf{p}_1,\mathbf{p}_2)
> =
> \sqrt{
> (x_2-x_1)^2+
> (y_2-y_1)^2+
> (z_2-z_1)^2
> }
> }
> $$
>
> More generally:
>
> $$
> d(\mathbf{p}_1,\mathbf{p}_2)
> =
> \|\mathbf{p}_2-\mathbf{p}_1\|_2
> $$
>
> This distance is invariant under rigid transformations.

## 3. Technical Representation

### 3.1. Vector norm and length

> [!info] Vector norm
> A norm is a mathematical function that assigns a nonnegative magnitude to a vector.
>
> For a vector:
>
> $$
> \mathbf{v}=
> \begin{bmatrix}
> v_1\\v_2\\v_3
> \end{bmatrix}
> $$
>
> Its Euclidean norm, also called the L2 norm, is:
>
> $$
> \boxed{
> \|\mathbf{v}\|_2=
> \sqrt{v_1^2+v_2^2+v_3^2}
> }
> $$
>
> The Euclidean norm satisfies:
>
> 1. Non-negativity:
>
> $$
> \|\mathbf{v}\|\geq 0
> $$
>
> 2. Positive definiteness:
>
> $$
> \|\mathbf{v}\|=0\iff\mathbf{v}=\mathbf{0}
> $$
>
> 3. Absolute homogeneity:
>
> $$
> \|\alpha\mathbf{v}\|
> =
> |\alpha|\|\mathbf{v}\|
> $$
>
> 4. Triangle inequality:
>
> $$
> \|\mathbf{u}+\mathbf{v}\|
> \leq
> \|\mathbf{u}\|+\|\mathbf{v}\|
> $$
>
> The norm provides a mathematical foundation for measuring displacement and velocity magnitudes in robotics.

### 3.2. Inner product and angles

> [!info] Euclidean inner product
> The inner product measures the relationship between two vectors and provides a way to calculate their angle.
>
> For two vectors:
>
> $$
> \mathbf{u}=
> \begin{bmatrix}
> u_1\\u_2\\u_3
> \end{bmatrix},
> \qquad
> \mathbf{v}=
> \begin{bmatrix}
> v_1\\v_2\\v_3
> \end{bmatrix}
> $$
>
> Their Euclidean inner product is:
>
> $$
> \boxed{
> \mathbf{u}\cdot\mathbf{v}
> =
> u_1v_1+u_2v_2+u_3v_3
> }
> $$
>
> Equivalently:
>
> $$
> \mathbf{u}\cdot\mathbf{v}
> =
> \mathbf{u}^T\mathbf{v}
> $$
>
> The angle between two nonzero vectors is:
>
> $$
> \boxed{
> \cos\theta=
> \frac{\mathbf{u}^T\mathbf{v}}
> {\|\mathbf{u}\|_2\|\mathbf{v}\|_2}
> }
> $$
>
> Where:
>
> - \(\theta\): Angle between the vectors.
> - \(\mathbf{u}^T\mathbf{v}\): Inner product.
> - \(\|\mathbf{u}\|_2,\|\mathbf{v}\|_2\): Euclidean magnitudes.
>
> **Orthogonality condition:**
>
> $$
> \boxed{
> \mathbf{u}^T\mathbf{v}=0
> }
> $$
>
> Two nonzero vectors are orthogonal when their angle is \(90^\circ\).

### 3.3. Orthogonality

> [!abstract] Orthogonality
> Orthogonality describes a perpendicular relationship between vectors, directions, or subspaces.
>
> For two nonzero vectors:
>
> $$
> \mathbf{u}\perp\mathbf{v}
> \iff
> \mathbf{u}^T\mathbf{v}=0
> $$
>
> For a matrix \(\mathbf{R}\), orthogonality is defined by:
>
> $$
> \boxed{
> \mathbf{R}^T\mathbf{R}=\mathbf{I}
> }
> $$
>
> This means that the columns and rows of \(\mathbf{R}\) form orthonormal sets.
>
> Orthogonality is fundamental to rotation matrices because rotations preserve inner products, vector lengths, and angles.

### 3.4. Preservation of distances under rigid transformations

> [!important] Distance invariance
> A rigid transformation is defined by:
>
> $$
> \mathbf{p}'=\mathbf{R}\mathbf{p}+\mathbf{t}
> $$
>
> Consider two points:
>
> $$
> \mathbf{p}'_1=\mathbf{R}\mathbf{p}_1+\mathbf{t}
> $$
>
> $$
> \mathbf{p}'_2=\mathbf{R}\mathbf{p}_2+\mathbf{t}
> $$
>
> Their transformed displacement is:
>
> $$
> \mathbf{p}'_2-\mathbf{p}'_1
> =
> \mathbf{R}(\mathbf{p}_2-\mathbf{p}_1)
> $$
>
> Taking the Euclidean norm:
>
> $$
> \|\mathbf{p}'_2-\mathbf{p}'_1\|_2
> =
> \|\mathbf{R}(\mathbf{p}_2-\mathbf{p}_1)\|_2
> $$
>
> Since:
>
> $$
> \mathbf{R}^T\mathbf{R}=\mathbf{I}
> $$
>
> We obtain:
>
> $$
> \begin{aligned}
> \|\mathbf{R}\mathbf{v}\|_2^2
> &= (\mathbf{R}\mathbf{v})^T
> (\mathbf{R}\mathbf{v})\\
> &=\mathbf{v}^T\mathbf{R}^T\mathbf{R}\mathbf{v}\\
> &=\mathbf{v}^T\mathbf{v}\\
> &=\|\mathbf{v}\|_2^2
> \end{aligned}
> $$
>
> Therefore:
>
> $$
> \boxed{
> \|\mathbf{p}'_2-\mathbf{p}'_1\|_2
> =
> \|\mathbf{p}_2-\mathbf{p}_1\|_2
> }
> $$
>
> **Conclusion:** Translation and rotation preserve the Euclidean distance between points.

### 3.5. Preservation of angles

> [!important] Angle invariance
> Rigid transformations preserve angles between vectors.
>
> Let:
>
> $$
> \mathbf{u}'=\mathbf{R}\mathbf{u}
> $$
>
> $$
> \mathbf{v}'=\mathbf{R}\mathbf{v}
> $$
>
> Their transformed inner product is:
>
> $$
> \begin{aligned}
> {\mathbf{u}'}^T\mathbf{v}'
> &=
> (\mathbf{R}\mathbf{u})^T
> (\mathbf{R}\mathbf{v})\\
> &=
> \mathbf{u}^T\mathbf{R}^T
> \mathbf{R}\mathbf{v}\\
> &=
> \mathbf{u}^T\mathbf{v}
> \end{aligned}
> $$
>
> Since vector magnitudes are also preserved:
>
> $$
> \boxed{
> \cos\theta'=\cos\theta
> }
> $$
>
> Consequently:
>
> $$
> \boxed{
> \theta'=\theta
> }
> $$
>
> for the usual angle convention between vectors, \(0\leq\theta\leq\pi\).

### 3.6. Area and volume preservation

> [!info] Area preservation
> A rotation preserves the area of geometric figures.
>
> For a planar parallelogram spanned by vectors \(\mathbf{u}\) and \(\mathbf{v}\), its area is:
>
> $$
> A=\|\mathbf{u}\times\mathbf{v}\|
> $$
>
> Since proper rotations preserve lengths and angles:
>
> $$
> \boxed{A'=A}
> $$
>
> **Volume preservation**
>
> A linear transformation changes volume according to the absolute determinant of its matrix:
>
> $$
> V'=|\det(\mathbf{R})|V
> $$
>
> For a proper rotation:
>
> $$
> \det(\mathbf{R})=1
> $$
>
> Therefore:
>
> $$
> \boxed{V'=V}
> $$
>
> Translation also preserves area and volume because it does not change relative geometric configurations.

### 3.7. Orientation and handedness

> [!important] Orientation preservation
> The determinant of an orthogonal matrix distinguishes proper rotations from reflections.
>
> For any orthogonal matrix:
>
> $$
> \mathbf{R}^T\mathbf{R}=\mathbf{I}
> $$
>
> Its determinant must satisfy:
>
> $$
> \det(\mathbf{R})=\pm1
> $$
>
> **Proper rotation:**
>
> $$
> \det(\mathbf{R})=+1
> $$
>
> Preserves orientation and handedness.
>
> **Improper orthogonal transformation:**
>
> $$
> \det(\mathbf{R})=-1
> $$
>
> Reverses orientation, as in a reflection or a rotation combined with a reflection.
>
> Therefore, a proper rigid-body transformation belongs to \(SE(3)\), whereas a reflection is not an element of \(SE(3)\).

### 3.8. Geometric invariants

> [!abstract] Geometric invariants
> A geometric invariant is a property that remains unchanged under a specified class of transformations.
>
> Under rigid transformations, important invariants include:
>
> | Property | Preserved? |
> |---|---|
> | Point-to-point distance | Yes |
> | Vector length | Yes |
> | Angle between vectors | Yes |
> | Collinearity | Yes |
> | Coplanarity | Yes |
> | Parallelism | Yes |
> | Perpendicularity | Yes |
> | Area | Yes |
> | Volume | Yes |
> | Orientation | Yes, for proper rotations |
> | Absolute position | No |
> | Absolute orientation | No |
>
> These invariants allow geometric relationships to be studied independently of the coordinate frame.

### 3.9. Euclidean transformations and similarity transformations

> [!note] Distinction between transformation classes
>
> **Rigid transformation**
>
> $$
> \mathbf{p}'=\mathbf{R}\mathbf{p}+\mathbf{t}
> $$
>
> Preserves distances and angles.
>
> **Similarity transformation**
>
> $$
> \mathbf{p}'=s\mathbf{R}\mathbf{p}+\mathbf{t}
> $$
>
> Where \(s>0\) is a uniform scale factor.
>
> It preserves angles and relative proportions, but distances are multiplied by \(s\).
>
> **Affine transformation**
>
> $$
> \mathbf{p}'=\mathbf{A}\mathbf{p}+\mathbf{t}
> $$
>
> Where \(\mathbf{A}\) is a general linear transformation.
>
> It preserves collinearity and ratios along a line, but does not generally preserve distances or angles.
>
> **Projective transformation**
>
> Describes geometric mappings in projective space, where collinearity is preserved but parallelism and Euclidean distances are not generally preserved.

## 4. Applications and Examples

### 4.1. Example: Distance preservation

> [!example] Verifying distance invariance
>
> Consider two points:
>
> $$
> \mathbf{p}_1=
> \begin{bmatrix}
> 1\\2\\0
> \end{bmatrix},
> \qquad
> \mathbf{p}_2=
> \begin{bmatrix}
> 4\\6\\0
> \end{bmatrix}
> $$
>
> Their original distance is:
>
> $$
> d=
> \sqrt{(4-1)^2+(6-2)^2}
> $$
>
> $$
> d=\sqrt{9+16}=5
> $$
>
> Now apply a rotation around Z by \(90^\circ\):
>
> $$
> \mathbf{R}_z(90^\circ)=
> \begin{bmatrix}
> 0&-1&0\\
> 1&0&0\\
> 0&0&1
> \end{bmatrix}
> $$
>
> The transformed points are:
>
> $$
> \mathbf{p}'_1=
> \begin{bmatrix}
> -2\\1\\0
> \end{bmatrix}
> $$
>
> $$
> \mathbf{p}'_2=
> \begin{bmatrix}
> -6\\4\\0
> \end{bmatrix}
> $$
>
> Their new distance is:
>
> $$
> d'=\sqrt{(-6+2)^2+(4-1)^2}
> $$
>
> $$
> d'=\sqrt{16+9}=5
> $$
>
> Therefore:
>
> $$
> \boxed{d'=d=5}
> $$
>
> This demonstrates the preservation of Euclidean distance under rotation.

### 4.2. Example: Orthogonality preservation

> [!example] Perpendicular vectors
>
> Consider:
>
> $$
> \mathbf{u}=
> \begin{bmatrix}
> 1\\0\\0
> \end{bmatrix},
> \qquad
> \mathbf{v}=
> \begin{bmatrix}
> 0\\1\\0
> \end{bmatrix}
> $$
>
> Their inner product is:
>
> $$
> \mathbf{u}^T\mathbf{v}=0
> $$
>
> Therefore, they are perpendicular.
>
> After applying the same rotation \(\mathbf{R}\):
>
> $$
> \mathbf{u}'=\mathbf{R}\mathbf{u}
> $$
>
> $$
> \mathbf{v}'=\mathbf{R}\mathbf{v}
> $$
>
> Their new inner product remains:
>
> $$
> {\mathbf{u}'}^T\mathbf{v}'
> =
> \mathbf{u}^T\mathbf{R}^T
> \mathbf{R}\mathbf{v}
> =
> 0
> $$
>
> Therefore, rigid transformations preserve perpendicularity.

### 4.3. Applications in robotics

> [!info] Robotics applications
>
> Metric and geometric properties are essential in:
>
> **1. Robot localization**
>
> Estimating robot positions while maintaining consistent geometric relationships between landmarks.
>
> **2. Mapping and SLAM**
>
> Matching geometric features between different sensor observations and coordinate frames.
>
> **3. Point-cloud registration**
>
> Aligning two point clouds by estimating a rigid transformation that minimizes geometric discrepancies.
>
> **4. Motion planning**
>
> Calculating distances, angles, clearances, and collision relationships.
>
> **5. Manipulator kinematics**
>
> Preserving link lengths and joint geometry during coordinate-frame transformations.
>
> **6. Formation control**
>
> Maintaining desired inter-robot distances and geometric configurations.
>
> In multi-robot systems, the distance between robots \(i\) and \(j\) can be expressed as:
>
> $$
> d_{ij}=
> \|\mathbf{p}_i-\mathbf{p}_j\|_2
> $$
>
> This quantity is invariant under a common rigid transformation applied to all robot positions.


## 6. Limitations and Evaluation

> [!warning] Important distinctions
>
> 1. **Metric versus geometric:** Not every geometric property is a metric property. Collinearity, for example, does not require a distance measurement.
>
> 2. **Coordinate dependence:** Numerical coordinates depend on the selected reference frame, even though Euclidean distances and angles remain invariant under rigid coordinate transformations.
>
> 3. **Measurement uncertainty:** Real robotic sensors introduce noise, so measured distances and angles may differ from their true geometric values.
>
> 4. **Non-Euclidean geometry:** Euclidean distance and angle definitions do not directly describe every geometric space. Curved spaces may require different metrics.
>
> 5. **Reflections:** Reflections preserve distances and angles but reverse orientation. Therefore, they are isometries but are not proper rigid-body motions in \(SE(3)\).
>
> 6. **Non-rigid transformations:** Scaling, shear, and deformation generally do not preserve all Euclidean metric properties.

> [!tip] Important distinction for robotics
> When transforming geometric measurements between robot coordinate frames, use the same rigid transformation for all points belonging to the same coordinate-frame relationship.
>
> Applying inconsistent transformations can destroy the geometric relationships required for localization, mapping, and point-cloud registration.

## 7. Verification and Evidence

> [!success] Established mathematical properties
>
> The following statements are established results in Euclidean geometry and linear algebra:
>
> - Euclidean distance is generated by the Euclidean norm.
> - The inner product determines vector angles and orthogonality.
> - Orthogonal matrices preserve Euclidean norms and inner products.
> - Proper rotations preserve orientation.
> - Rigid transformations preserve distances, angles, areas, and volumes.
> - Reflections preserve metric properties but reverse orientation.
>
> **Confidence:** 1/5 — Initial familiarity level; this does not indicate scientific uncertainty.
>
> **Further verification:** Study isometric mappings, metric tensors, and transformation groups for a deeper mathematical understanding.

## 8. Personal Notes

> [!question] Questions for further study
>
> - What is the difference between a metric space and a Euclidean space?
> - Why does the inner product define both vector length and angle?
> - How does an orthogonal matrix preserve geometric measurements?
> - Why are reflections isometries but not proper rotations?
> - How do metric invariants support point-cloud registration?
> - How are geometric invariants used in distributed multi-robot localization?
> - What changes when Euclidean geometry is replaced by Riemannian geometry?

## 9. References

1. Lee, J. M. (2018). *Introduction to Riemannian Manifolds* (2nd ed.). Springer.
   - Mathematical foundations of metrics, geometric structures, and distance.

2. Do Carmo, M. P. (1976). *Differential Geometry of Curves and Surfaces*. Prentice-Hall.
   - Classical treatment of geometric properties and differential geometry.

3. Murray, R. M., Li, Z., & Sastry, S. S. (1994). *A Mathematical Introduction to Robotic Manipulation*. CRC Press.
   - https://www.cds.caltech.edu/~murray/mlswiki/
   - Rigid-body transformations and geometric foundations of robotics.

4. Lynch, K. M., & Park, F. C. (2017). *Modern Robotics: Mechanics, Planning, and Control*. Cambridge University Press.
   - https://modernrobotics.northwestern.edu/
   - Euclidean geometry, rigid-body motion, and robot kinematics.

5. Barfoot, T. D. (2017). *State Estimation for Robotics*. Cambridge University Press.
   - https://asrl.utias.utoronto.ca/~tdb/
   - Geometric estimation, coordinate transformations, and uncertainty in robotics.

