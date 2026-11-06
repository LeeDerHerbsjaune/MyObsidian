---
type: technical-term
title: Rigid Transformations and Rotations
aliases:
  - Rigid Body Transformations
  - Rigid Motions
  - Euclidean Transformations
  - 3D Rigid Transformations
abbreviation: SE(3)
field:
  - Mathematics
  - Robotics
  - Computer Science
subfield:
  - Linear Algebra
  - Geometry
  - Robot Kinematics
  - Computer Vision
status: learning
confidence: 1
created: 2026-10-31
updated: 2026-10-31
tags:
  - technical-term
  - robotics
  - rigid-transformation
  - rotation
  - coordinate-frame
  - linear-algebra
  - geometry
sources: []
projects: []
related:
  - "[[MOC - Rigid Transformations & Rotations]]"
---
## 1. Identification

> [!abstract] Definition
> A **rigid transformation** is a geometric transformation that preserves distances and angles between points. It describes the change in position and orientation of a rigid body without changing its shape or size.
>
> In three-dimensional robotics, a rigid transformation consists of:
>
> - **Translation:** A change in position.
> - **Rotation:** A change in orientation.
>
> These transformations are mathematically represented using rotation matrices, translation vectors, and homogeneous transformation matrices.
>
> The mathematical group describing three-dimensional rigid transformations is the **Special Euclidean Group**, denoted by \(SE(3)\).

- **Domain:** Mathematics, Robotics, Computer Science.
- **Subdomains:** Euclidean Geometry, Linear Algebra, Robot Kinematics, Computer Vision.
- **Primary mathematical structures:** \(SO(3)\) and \(SE(3)\).
- **Primary applications:** Coordinate-frame transformations, robot pose representation, motion planning, and spatial geometry.

## 2. Definition and Core Concept

### 2.1. Rigid transformation

> [!info] Core concept
> A rigid transformation maps points from one configuration to another while preserving the Euclidean distance between every pair of points.
>
> Let two points be represented by:
>
> $$
> \mathbf{p}_1,\mathbf{p}_2\in\mathbb{R}^3
> $$
>
> After applying a rigid transformation, their corresponding positions are:
>
> $$
> \mathbf{p}'_1,\mathbf{p}'_2
> $$
>
> Distance preservation requires:
>
> $$
> \boxed{
> \|\mathbf{p}'_1-\mathbf{p}'_2\|
> =
> \|\mathbf{p}_1-\mathbf{p}_2\|
> }
> $$
>
> This property ensures that the relative geometric structure of a rigid body remains unchanged.

### 2.2. Translation

> [!info] Translation
> Translation changes the position of an object without changing its orientation.
>
> A point \(\mathbf{p}\) translated by vector \(\mathbf{t}\) becomes:
>
> $$
> \boxed{
> \mathbf{p}'=\mathbf{p}+\mathbf{t}
> }
> $$
>
> Where:
>
> - \(\mathbf{p}\in\mathbb{R}^3\): Original point.
> - \(\mathbf{p}'\in\mathbb{R}^3\): Translated point.
> - \(\mathbf{t}\in\mathbb{R}^3\): Translation vector.
>
> Explicitly:
>
> $$
> \mathbf{t}=
> \begin{bmatrix}
> t_x\\
> t_y\\
> t_z
> \end{bmatrix}
> $$
>
> Therefore:
>
> $$
> \begin{bmatrix}
> x'\\y'\\z'
> \end{bmatrix}
> =
> \begin{bmatrix}
> x\\y\\z
> \end{bmatrix}
> +
> \begin{bmatrix}
> t_x\\t_y\\t_z
> \end{bmatrix}
> $$

### 2.3. Rotation

> [!info] Rotation
> Rotation changes the orientation of an object around an axis while preserving distances and angles.
>
> In three-dimensional space, a rotation is represented by a \(3\times3\) rotation matrix:
>
> $$
> \boxed{
> \mathbf{p}'=\mathbf{R}\mathbf{p}
> }
> $$
>
> Where:
>
> - \(\mathbf{p}\): Original position vector.
> - \(\mathbf{p}'\): Rotated position vector.
> - \(\mathbf{R}\in\mathbb{R}^{3\times3}\): Rotation matrix.
>
> A valid rotation matrix satisfies:
>
> $$
> \mathbf{R}^T\mathbf{R}=\mathbf{I}
> $$
>
> and:
>
> $$
> \det(\mathbf{R})=+1
> $$

### 2.4. Combined rigid transformation

> [!important] Fundamental equation
> A general rigid transformation combines rotation and translation:
>
> $$
> \boxed{
> \mathbf{p}'=\mathbf{R}\mathbf{p}+\mathbf{t}
> }
> $$
>
> This equation is fundamental in robotics because a robot link or coordinate frame can change both its position and orientation.
>
> The transformation has six independent parameters:
>
> - Three translational parameters.
> - Three rotational parameters.
>
> Thus:
>
> $$
> \dim(SE(3))=6
> $$

## 3. Technical Representation

### 3.1. Rotation matrices

> [!abstract] Rotation matrix
> A rotation matrix is an orthogonal matrix with determinant \(+1\). It represents a proper rotation in Euclidean space.
>
> In three dimensions:
>
> $$
> \mathbf{R}\in SO(3)
> $$
>
> The special orthogonal group is defined as:
>
> $$
> \boxed{
> SO(3)=
> \left\{
> \mathbf{R}\in\mathbb{R}^{3\times3}
> \mid
> \mathbf{R}^T\mathbf{R}=\mathbf{I},
> \det(\mathbf{R})=1
> \right\}
> $$
>
> The columns of \(\mathbf{R}\) can be interpreted as the coordinate axes of a rotated frame, expressed in the original frame.

### 3.2. Elementary rotations

> [!info] Rotation about the X-axis
>
> A rotation by angle \(\theta\) around the X-axis is:
>
> $$
> \mathbf{R}_x(\theta)=
> \begin{bmatrix}
> 1&0&0\\
> 0&\cos\theta&-\sin\theta\\
> 0&\sin\theta&\cos\theta
> \end{bmatrix}
> $$

> [!info] Rotation about the Y-axis
>
> $$
> \mathbf{R}_y(\theta)=
> \begin{bmatrix}
> \cos\theta&0&\sin\theta\\
> 0&1&0\\
> -\sin\theta&0&\cos\theta
> \end{bmatrix}
> $$

> [!info] Rotation about the Z-axis
>
> $$
> \mathbf{R}_z(\theta)=
> \begin{bmatrix}
> \cos\theta&-\sin\theta&0\\
> \sin\theta&\cos\theta&0\\
> 0&0&1
> \end{bmatrix}
> $$

> [!important] Rotation convention
> These matrices assume:
>
> - A right-handed coordinate system.
> - Positive angles following the right-hand rule.
> - Active rotations of column vectors.
>
> The rotation angle is expressed in radians unless otherwise specified.
>
> Different conventions, particularly passive coordinate transformations and row-vector representations, may produce transposed matrices or reversed multiplication order.

### 3.3. Composition of rotations

> [!info] Rotation composition
> Multiple rotations can be combined through matrix multiplication.
>
> For example:
>
> $$
> \mathbf{R}
> =
> \mathbf{R}_z(\gamma)
> \mathbf{R}_y(\beta)
> \mathbf{R}_x(\alpha)
> $$
>
> For column vectors, the rightmost matrix acts first.
>
> Therefore, the above expression applies:
>
> 1. Rotation around X by \(\alpha\).
> 2. Rotation around Y by \(\beta\).
> 3. Rotation around Z by \(\gamma\).
>
> **Important properties:**
>
> $$
> \mathbf{R}_1\mathbf{R}_2
> \neq
> \mathbf{R}_2\mathbf{R}_1
> $$
>
> in general.
>
> Consequently, three-dimensional rotations are noncommutative.

### 3.4. Euler angles

> [!abstract] Euler-angle representation
> Euler angles represent a three-dimensional orientation using three successive rotations about specified axes.
>
> One common convention is ZYX:
>
> $$
> \mathbf{R}
> =
> \mathbf{R}_z(\psi)
> \mathbf{R}_y(\theta)
> \mathbf{R}_x(\phi)
> $$
>
> Where:
>
> - \(\phi\): Roll.
> - \(\theta\): Pitch.
> - \(\psi\): Yaw.
>
> The resulting matrix is:
>
> $$
> \mathbf{R}=
> \begin{bmatrix}
> c_\psi c_\theta &
> c_\psi s_\theta s_\phi-s_\psi c_\phi &
> c_\psi s_\theta c_\phi+s_\psi s_\phi\\
>
> s_\psi c_\theta &
> s_\psi s_\theta s_\phi+c_\psi c_\phi &
> s_\psi s_\theta c_\phi-c_\psi s_\phi\\
>
> -s_\theta &
> c_\theta s_\phi &
> c_\theta c_\phi
> \end{bmatrix}
> $$
>
> Here:
>
> - \(c_\alpha=\cos\alpha\).
> - \(s_\alpha=\sin\alpha\).
>
> **Limitation:**
>
> Euler-angle representations can encounter gimbal lock, a singularity in which two rotational degrees of freedom become aligned.

### 3.5. Axis-angle representation

> [!info] Axis-angle representation
> A rotation can also be represented by:
>
> - A unit rotation axis \(\hat{\mathbf{u}}\).
> - A rotation angle \(\theta\).
>
> Where:
>
> $$
> \|\hat{\mathbf{u}}\|=1
> $$
>
> Using Rodrigues' rotation formula:
>
> $$
> \boxed{
> \mathbf{R}
> =
> \mathbf{I}
> +
> \sin\theta[\hat{\mathbf{u}}]_\times
> +
> (1-\cos\theta)[\hat{\mathbf{u}}]_\times^2
> }
> $$
>
> The skew-symmetric matrix is:
>
> $$
> [\hat{\mathbf{u}}]_\times=
> \begin{bmatrix}
> 0&-u_z&u_y\\
> u_z&0&-u_x\\
> -u_y&u_x&0
> \end{bmatrix}
> $$
>
> It satisfies:
>
> $$
> [\hat{\mathbf{u}}]_\times\mathbf{v}
> =
> \hat{\mathbf{u}}\times\mathbf{v}
> $$
>
> Axis-angle representation is particularly useful for geometric reasoning and rotation interpolation.

### 3.6. Homogeneous transformation matrix

> [!important] Homogeneous coordinates
> Rotation and translation can be combined into a single \(4\times4\) matrix using homogeneous coordinates.
>
> The homogeneous transformation matrix is:
>
> $$
> \boxed{
> \mathbf{T}=
> \begin{bmatrix}
> \mathbf{R}&\mathbf{t}\\
> \mathbf{0}^T&1
> \end{bmatrix}
> }
> $$
>
> Expanded:
>
> $$
> \mathbf{T}=
> \begin{bmatrix}
> r_{11}&r_{12}&r_{13}&t_x\\
> r_{21}&r_{22}&r_{23}&t_y\\
> r_{31}&r_{32}&r_{33}&t_z\\
> 0&0&0&1
> \end{bmatrix}
> $$
>
> A point in homogeneous coordinates is:
>
> $$
> \tilde{\mathbf{p}}=
> \begin{bmatrix}
> x\\y\\z\\1
> \end{bmatrix}
> $$
>
> The transformation becomes:
>
> $$
> \boxed{
> \tilde{\mathbf{p}}'
> =
> \mathbf{T}\tilde{\mathbf{p}}
> }
> $$
>
> Homogeneous transformation matrices are fundamental to robot kinematics because they represent the position and orientation of one coordinate frame relative to another.

### 3.7. Inverse rigid transformation

> [!info] Inverse transformation
> Given:
>
> $$
> \mathbf{T}=
> \begin{bmatrix}
> \mathbf{R}&\mathbf{t}\\
> \mathbf{0}^T&1
> \end{bmatrix}
> $$
>
> Its inverse is:
>
> $$
> \boxed{
> \mathbf{T}^{-1}=
> \begin{bmatrix}
> \mathbf{R}^T&-\mathbf{R}^T\mathbf{t}\\
> \mathbf{0}^T&1
> \end{bmatrix}
> }
> $$
>
> This follows from the orthogonality property:
>
> $$
> \mathbf{R}^{-1}=\mathbf{R}^T
> $$
>
> The inverse transformation is used to convert coordinates between reference frames in the opposite direction.

### 3.8. Special Euclidean Group SE(3)

> [!abstract] Mathematical structure
> The set of all three-dimensional rigid transformations forms a mathematical group called the Special Euclidean Group:
>
> $$
> \boxed{
> SE(3)=
> \left\{
> \begin{bmatrix}
> \mathbf{R}&\mathbf{t}\\
> \mathbf{0}^T&1
> \end{bmatrix}
> \mid
> \mathbf{R}\in SO(3),
> \mathbf{t}\in\mathbb{R}^3
> \right\}
> $$
>
> The group operation is matrix multiplication.
>
> Its properties include:
>
> 1. **Closure:** The product of two rigid transformations is another rigid transformation.
> 2. **Associativity:** Matrix multiplication is associative.
> 3. **Identity:** There exists an identity transformation.
> 4. **Inverse:** Every rigid transformation has an inverse.
>
> The identity transformation is:
>
> $$
> \mathbf{I}_4=
> \begin{bmatrix}
> 1&0&0&0\\
> 0&1&0&0\\
> 0&0&1&0\\
> 0&0&0&1
> \end{bmatrix}
> $$

## 4. Applications and Examples

### 4.1. Coordinate-frame transformation

> [!example] Transforming a point between coordinate frames
>
> Consider a point represented in coordinate frame B:
>
> $$
> {}^B\mathbf{p}=
> \begin{bmatrix}
> 1\\2\\3
> \end{bmatrix}
> $$
>
> Suppose frame B is rotated by \(90^\circ\) around the Z-axis and translated relative to frame A by:
>
> $$
> {}^A\mathbf{t}_B=
> \begin{bmatrix}
> 2\\0\\1
> \end{bmatrix}
> $$
>
> The rotation matrix is:
>
> $$
> {}^A\mathbf{R}_B=
> \begin{bmatrix}
> 0&-1&0\\
> 1&0&0\\
> 0&0&1
> \end{bmatrix}
> $$
>
> The transformation is:
>
> $$
> {}^A\mathbf{p}
> =
> {}^A\mathbf{R}_B{}^B\mathbf{p}
> +
> {}^A\mathbf{t}_B
> $$
>
> Substituting:
>
> $$
> {}^A\mathbf{p}
> =
> \begin{bmatrix}
> 0&-1&0\\
> 1&0&0\\
> 0&0&1
> \end{bmatrix}
> \begin{bmatrix}
> 1\\2\\3
> \end{bmatrix}
> +
> \begin{bmatrix}
> 2\\0\\1
> \end{bmatrix}
> $$
>
> Therefore:
>
> $$
> {}^A\mathbf{p}
> =
> \begin{bmatrix}
> -2\\1\\3
> \end{bmatrix}
> +
> \begin{bmatrix}
> 2\\0\\1
> \end{bmatrix}
> $$
>
> $$
> \boxed{
> {}^A\mathbf{p}=
> \begin{bmatrix}
> 0\\1\\4
> \end{bmatrix}
> }
> $$
>
> The point expressed in frame A is \((0,1,4)\).

### 4.2. Robot manipulator kinematics

> [!example] Forward kinematics
>
> In a serial robot manipulator, each joint connects two adjacent links.
>
> The pose of the end-effector relative to the robot base is obtained by multiplying the transformations along the kinematic chain:
>
> $$
> \boxed{
> {}^0\mathbf{T}_n
> =
> {}^0\mathbf{T}_1
> {}^1\mathbf{T}_2
> \cdots
> {}^{n-1}\mathbf{T}_n
> }
> $$
>
> Where:
>
> - \({}^0\mathbf{T}_n\): End-effector pose relative to the base.
> - \({}^{i-1}\mathbf{T}_i\): Transformation from frame \(i\) to frame \(i-1\).
> - \(n\): Number of joints or transformations in the chain.
>
> This is the foundation of Forward Kinematics.

### 4.3. Applications in swarm robotics

> [!info] Multi-robot coordinate transformations
>
> Rigid transformations are also essential in swarm robotics.
>
> Typical applications include:
>
> - **Relative localization:** Expressing one robot's position relative to another robot.
> - **Formation control:** Maintaining desired relative positions and orientations.
> - **Sensor fusion:** Transforming measurements between camera, LiDAR, IMU, and robot-body frames.
> - **Multi-robot mapping:** Aligning local maps into a common global coordinate frame.
> - **Distributed navigation:** Converting locally estimated poses into shared reference frames.
>
> A relative pose between robots A and B can be represented as:
>
> $$
> {}^A\mathbf{T}_B
> =
> ({}^W\mathbf{T}_A)^{-1}
> {}^W\mathbf{T}_B
> $$
>
> Where W is a shared world reference frame.
>
> This relationship is particularly important in distributed multi-robot systems.


## 6. Limitations and Evaluation

> [!warning] Important limitations
>
> 1. **Euler-angle singularities:** Euler angles can suffer from gimbal lock.
>
> 2. **Noncommutativity:** The order of rotations affects the final orientation.
>
> 3. **Numerical errors:** Repeated matrix multiplication can introduce numerical deviations from perfect orthogonality.
>
> 4. **Representation ambiguity:** Multiple Euler-angle combinations or axis-angle representations can describe the same orientation.
>
> 5. **Coordinate convention dependence:** Active versus passive transformations, frame direction, and row-vector versus column-vector conventions must be specified.
>
> 6. **Rigid-body assumption:** Rigid transformations cannot represent deformation, scaling, or other non-rigid motions.
>
> 7. **Rotation interpolation:** Direct linear interpolation of rotation matrices generally does not preserve orthogonality.

> [!tip] Choosing a representation
>
> | Representation | Main advantage | Main limitation |
> |---|---|---|
> | Rotation matrix | Direct geometric interpretation | 9 entries with 6 constraints |
> | Euler angles | Intuitive and compact | Gimbal lock |
> | Axis-angle | Geometric interpretation | Singular or ambiguous at special angles |
> | Quaternion | Efficient and stable interpolation | Double-cover ambiguity |
> | Homogeneous matrix | Combines rotation and translation | 16 entries with structural constraints |

## 7. Verification and Evidence

> [!success] Established mathematical properties
>
> A valid three-dimensional rigid transformation:
>
> - Preserves Euclidean distances.
> - Preserves angles.
> - Preserves orientation when represented by a proper rotation with determinant \(+1\).
> - Has six independent degrees of freedom.
> - Can be represented using an element of \(SE(3)\).
>
> The following identities are fundamental:
>
> $$
> \mathbf{R}^T\mathbf{R}=\mathbf{I}
> $$
>
> $$
> \det(\mathbf{R})=1
> $$
>
> $$
> \mathbf{T}^{-1}=
> \begin{bmatrix}
> \mathbf{R}^T&-\mathbf{R}^T\mathbf{t}\\
> \mathbf{0}^T&1
> \end{bmatrix}
> $$
>
> **Confidence:** These are established mathematical results.
>
> **Further study:** Lie group representations and differential kinematics provide a deeper mathematical treatment of rigid-body motion.

## 8. Personal Notes

> [!question] Questions for further study
>
> - What is the difference between active and passive rotations?
> - Why are rotation matrices elements of \(SO(3)\)?
> - Why does the composition of rotations not commute?
> - How are quaternions related to rotation matrices?
> - How does \(SE(3)\) relate to \(SO(3)\)?
> - How are rigid transformations differentiated with respect to time?
> - How are twists and exponential coordinates used to represent rigid-body motion?
> - How are coordinate transformations implemented in ROS 2 TF2?

## 9. References

1. Murray, R. M., Li, Z., & Sastry, S. S. (1994). *A Mathematical Introduction to Robotic Manipulation*. CRC Press.
   - https://www.cds.caltech.edu/~murray/mlswiki/
   - Mathematical foundations of rigid-body transformations, Lie groups, and robot manipulation.

2. Lynch, K. M., & Park, F. C. (2017). *Modern Robotics: Mechanics, Planning, and Control*. Cambridge University Press.
   - https://modernrobotics.northwestern.edu/
   - Detailed treatment of rotation matrices, homogeneous transformations, \(SO(3)\), and \(SE(3)\).

3. Siciliano, B., Sciavicco, L., Villani, L., & Oriolo, G. (2009). *Robotics: Modelling, Planning and Control*. Springer.
   - Robot coordinate systems and kinematic transformations.

4. ROS 2 Documentation. *tf2: Transform Library*.
   - https://docs.ros.org/en/rolling/Concepts/Intermediate/About-Tf2.html
   - Practical coordinate-frame transformations in ROS 2.

