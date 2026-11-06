---
type: moc
title: "Three-Dimensional Euclid Space"
tags:
  - moc
---
## 5. Knowledge Relationships

### 5.1 Conceptual Dependencies

> [!abstract] Related Concepts
>
> | Concept | Relationship |
> |---|---|
> | [[Real Number]] | Underlying scalar field |
> | Vector | Represents displacement and direction |
> | [[Vector Spaces\|Vector Space]] | Provides the associated vector structure |
> | [[Affine Space]] | Provides the geometric structure of points and displacements |
> | Cartesian Coordinate System | Represents spatial positions |
> | Euclidean Distance | Measures separation between points |
> | Inner Product | Defines angles and orthogonality |
> | Orthogonality | Describes perpendicular vectors |
> | Metric Tensor | Defines the distance structure |
> | [[Coordinate Transformation]] | Changes coordinate representations |
> | [[Rigid Transformations & Rotations]] | Represents three-dimensional rotations. |
> | [[Robot Configuration Space]] | Represents robot configurations |

### 5.2 Euclidean Space vs. Vector Space

> [!warning] Important Mathematical Distinction
> Euclidean space and vector space are related but are not identical mathematical structures.
>
> **Vector space:**
> - Contains vectors.
> - Supports vector addition.
> - Supports scalar multiplication.
> - Has a zero vector and a distinguished origin.
>
> **Affine space:**
> - Contains points.
> - Defines displacement vectors between points.
> - Does not inherently have a distinguished origin.
> - Allows points to be translated by vectors.
>
> **Euclidean space:**
> - Is an affine space.
> - Has an associated real vector space.
> - Equipped with a positive-definite inner product.
> - Supports geometric measurements such as distance and angle.
>
> Consequently, points and vectors should not be treated as identical mathematical objects, even though Cartesian coordinates often make them appear similar.

### 5.3 Euclidean Space vs. Configuration Space

> [!note] Distinction in Robotics
> Three-dimensional Euclidean space describes the physical position of points.
>
> Robot configuration space describes the complete set of configurations available to a robot.
>
> For example, the configuration of a free rigid body in three-dimensional space generally requires:
>
> - Three translational degrees of freedom.
> - Three rotational degrees of freedom.
>
> Its configuration space is:
>
> $$
> SE(3)=\mathbb{R}^3\rtimes SO(3)
> $$
>
> Therefore, the position of a robot belongs to a three-dimensional Euclidean space, but its complete rigid-body pose belongs to the six-dimensional configuration manifold \(SE(3)\).

## 10. Knowledge Links and Further Development

> [!tip] Suggested Learning Sequence
> A recommended learning progression is:
>
> 1. [[Real Number]]
> 2. [[Vectors|Vector]]
> 3. [[Vector Spaces|Vector Space]]
> 4. [[Affine Space]]
> 5. [[Euclidean Space]]
> 6. [[Three-Dimensional Coordinate System]]
> 7. [[Coordinate Transformation]]
> 8. [[Robot Configuration Space]]
> 9. Robot Kinematics
>
> **Recommended next topic:** Euclidean Space
>
> Understanding the general mathematical structure of Euclidean space before studying its three-dimensional specialization will make subsequent topics in robotics, geometry, and kinematics easier to understand.

---
