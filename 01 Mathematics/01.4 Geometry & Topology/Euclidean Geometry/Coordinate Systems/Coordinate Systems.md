---
type: technical-term
title: Coordinate Systems
aliases:
  - Coordinate System
  - Reference Coordinate System
  - Spatial Coordinate System
  - Coordinate Frame
abbreviation: ""
field:
  - Mathematics
  - Robotics
  - Physics
  - Computer Science
subfield:
  - Euclidean Geometry
  - Linear Algebra
  - Robot Kinematics
  - Computer Vision
  - Spatial Modeling
status: learning
confidence: 1
created: 2026-10-31
updated: 2026-10-31
tags:
  - technical-term
  - mathematics
  - robotics
  - coordinate-system
  - coordinate-frame
  - geometry
  - transformations
sources: []
projects: []
related:
  - "[[MOC - Coordinate Systems]]"
---

# Coordinate Systems

## 1. Identification

> [!abstract] Definition
> A **coordinate system** is a mathematical framework used to assign numerical coordinates to points in a geometric space relative to a specified reference origin, set of basis vectors, and coordinate convention.
>
> It provides a systematic method for representing positions, directions, orientations, and geometric relationships using numerical values.
>
> In robotics, coordinate systems are essential for describing the positions and orientations of robot links, joints, sensors, objects, and other robots.
>
> A coordinate system allows geometric quantities to be represented mathematically and transformed between different reference frames.

- **Domain:** Mathematics, Robotics, Physics, Computer Science.
- **Subdomains:** Euclidean Geometry, Linear Algebra, Robot Kinematics, Computer Vision.
- **Primary purpose:** Mathematical representation of spatial quantities.
- **Fundamental components:** Origin, basis vectors, coordinate axes, and coordinate values.
- **Primary applications:** Localization, mapping, robot kinematics, navigation, and sensor integration.

## 2. Definition and Core Concepts

### 2.1. Coordinate system

> [!info] Core concept
> A coordinate system establishes a relationship between geometric points and numerical coordinate representations.
>
> In three-dimensional Euclidean space, a Cartesian coordinate system is commonly defined by:
>
> 1. An origin \(O\).
> 2. Three mutually orthogonal basis directions.
> 3. An orientation convention.
> 4. A unit of measurement.
>
> A point \(P\) can then be represented by:
>
> $$
> \mathbf{p}=
> \begin{bmatrix}
> x\\y\\z
> \end{bmatrix}
> $$
>
> Where:
>
> - \(x\): Coordinate along the first axis.
> - \(y\): Coordinate along the second axis.
> - \(z\): Coordinate along the third axis.
>
> These coordinates describe the point relative to the selected coordinate system.

### 2.2. Coordinate system versus coordinate frame

> [!important] Terminological distinction
> The terms **coordinate system** and **coordinate frame** are closely related but are not always used identically.
>
> - **Coordinate system:** The mathematical convention used to assign coordinates, including its axes, origin, and coordinate representation.
> - **Coordinate frame:** A particular reference frame with a defined origin and orientation relative to another reference frame.
>
> In robotics, a coordinate frame is frequently represented by an origin and an orthonormal basis.
>
> A coordinate system defines how coordinates are interpreted, while a coordinate frame specifies the particular spatial reference used to express them.

### 2.3. Components of a Cartesian coordinate frame

> [!info] Fundamental components
>
> **1. Origin**
>
> The reference point from which coordinates are measured.
>
> $$
> O=(0,0,0)
> $$
>
> **2. Coordinate axes**
>
> Three mutually perpendicular directions in conventional 3D Cartesian coordinates:
>
> - X-axis
> - Y-axis
> - Z-axis
>
> **3. Basis vectors**
>
> The standard Cartesian basis is:
>
> $$
> \mathbf{e}_x=
> \begin{bmatrix}
> 1\\0\\0
> \end{bmatrix}
> $$
>
> $$
> \mathbf{e}_y=
> \begin{bmatrix}
> 0\\1\\0
> \end{bmatrix}
> $$
>
> $$
> \mathbf{e}_z=
> \begin{bmatrix}
> 0\\0\\1
> \end{bmatrix}
> $$
>
> **4. Coordinate values**
>
> The scalar coefficients specifying a point's position along the basis directions.

### 2.4. Position vector representation

> [!abstract] Position vector
> A point's position relative to an origin can be represented by a position vector.
>
> For a point \(P\):
>
> $$
> \overrightarrow{OP}
> =
> x\mathbf{e}_x+
> y\mathbf{e}_y+
> z\mathbf{e}_z
> $$
>
> In matrix form:
>
> $$
> \boxed{
> \mathbf{p}=
> \begin{bmatrix}
> x\\y\\z
> \end{bmatrix}
> }
> $$
>
> More generally:
>
> $$
> \mathbf{p}
> =
> x\mathbf{e}_x+
> y\mathbf{e}_y+
> z\mathbf{e}_z
> $$
>
> The numerical coordinates depend on the selected origin and basis, even though the geometric point itself does not change.

## 3. Technical Representation

### 3.1. Cartesian coordinate system

> [!abstract] Cartesian coordinates
> A Cartesian coordinate system represents positions using mutually perpendicular coordinate axes.
>
> In two dimensions:
>
> $$
> \mathbf{p}=
> \begin{bmatrix}
> x\\y
> \end{bmatrix}
> $$
>
> In three dimensions:
>
> $$
> \mathbf{p}=
> \begin{bmatrix}
> x\\y\\z
> \end{bmatrix}
> $$
>
> The Euclidean distance between two points is:
>
> $$
> d(\mathbf{p}_1,\mathbf{p}_2)
> =
> \sqrt{
> (x_2-x_1)^2+
> (y_2-y_1)^2+
> (z_2-z_1)^2
> }
> $$
>
> Cartesian coordinates are widely used in robotics because they provide a convenient representation for positions, translations, and geometric calculations.

### 3.2. Two-dimensional coordinate systems

> [!info] 2D Cartesian coordinates
> A two-dimensional coordinate system uses two perpendicular axes:
>
> - X-axis: Horizontal direction.
> - Y-axis: Vertical direction.
>
> A point is represented as:
>
> $$
> P=(x,y)
> $$
>
> This representation is useful for planar mechanisms, mobile robot navigation, and two-dimensional mapping.
>
> A free planar rigid body has three degrees of freedom:
>
> $$
> q=
> \begin{bmatrix}
> x\\y\\\theta
> \end{bmatrix}
> $$
>
> Where \(\theta\) describes its orientation in the plane.

### 3.3. Three-dimensional coordinate systems

> [!important] 3D Cartesian coordinates
> A three-dimensional coordinate system uses three independent spatial directions.
>
> A point is represented by:
>
> $$
> P=(x,y,z)
> $$
>
> Its position vector is:
>
> $$
> \mathbf{p}=
> x\mathbf{e}_x+
> y\mathbf{e}_y+
> z\mathbf{e}_z
> $$
>
> A free rigid body in 3D has six degrees of freedom:
>
> $$
> q=
> \begin{bmatrix}
> x&y&z&\phi&\theta&\psi
> \end{bmatrix}^T
> $$
>
> Where:
>
> - \(x,y,z\): Translational coordinates.
> - \(\phi\): Roll.
> - \(\theta\): Pitch.
> - \(\psi\): Yaw.
>
> This is one common parameterization of position and orientation, rather than a unique global coordinate representation of orientation.

### 3.4. Right-handed and left-handed coordinate systems

> [!abstract] Coordinate-system handedness
> Coordinate-system handedness describes the orientation relationship between its three basis axes.
>
> **Right-handed coordinate system**
>
> The axes satisfy:
>
> $$
> \boxed{
> \mathbf{e}_x\times\mathbf{e}_y
> =
> \mathbf{e}_z
> }
> $$
>
> The orientation follows the right-hand rule.
>
> **Left-handed coordinate system**
>
> The axes satisfy:
>
> $$
> \mathbf{e}_x\times\mathbf{e}_y
> =
> -\mathbf{e}_z
> $$
>
> The orientation is reversed relative to the right-handed convention.
>
> | Property | Right-handed | Left-handed |
> |---|---|---|
> | Handedness | Right | Left |
> | Orientation | Positive | Reversed |
> | Cross-product convention | Standard right-hand rule | Opposite orientation convention |
> | Common applications | Robotics, physics | Some graphics systems |
>
> **Important:** The cross product is intrinsically defined in oriented three-dimensional Euclidean space. A left-handed coordinate representation changes the component-level sign convention associated with the chosen orientation.

### 3.5. Cylindrical coordinate system

> [!info] Cylindrical coordinates
> A cylindrical coordinate system represents a point using:
>
> - \(r\): Radial distance from the Z-axis.
> - \(\theta\): Azimuthal angle around the Z-axis.
> - \(z\): Height along the Z-axis.
>
> The coordinate representation is:
>
> $$
> P=(r,\theta,z)
> $$
>
> Conversion to Cartesian coordinates:
>
> $$
> \boxed{
> x=r\cos\theta
> }
> $$
>
> $$
> \boxed{
> y=r\sin\theta
> }
> $$
>
> $$
> \boxed{
> z=z
> }
> $$
>
> Conversion from Cartesian coordinates:
>
> $$
> r=\sqrt{x^2+y^2}
> $$
>
> $$
> \theta=\operatorname{atan2}(y,x)
> $$
>
> $$
> z=z
> $$
>
> **Applications:**
>
> - Cylindrical robot manipulators.
> - Rotational mechanisms.
> - Radial motion analysis.
> - Robot navigation around central obstacles.

### 3.6. Spherical coordinate system

> [!info] Spherical coordinates
> A spherical coordinate system represents a point using:
>
> - \(\rho\): Distance from the origin.
> - \(\theta\): Azimuthal angle in the XY-plane.
> - \(\varphi\): Polar angle measured from the positive Z-axis.
>
> The coordinate representation is:
>
> $$
> P=(\rho,\theta,\varphi)
> $$
>
> Conversion to Cartesian coordinates:
>
> $$
> \boxed{
> x=\rho\sin\varphi\cos\theta
> }
> $$
>
> $$
> \boxed{
> y=\rho\sin\varphi\sin\theta
> }
> $$
>
> $$
> \boxed{
> z=\rho\cos\varphi
> }
> $$
>
> Conversion from Cartesian coordinates:
>
> $$
> \rho=\sqrt{x^2+y^2+z^2}
> $$
>
> $$
> \theta=\operatorname{atan2}(y,x)
> $$
>
> $$
> \varphi=
> \operatorname{atan2}
> \left(
> \sqrt{x^2+y^2},z
> \right)
> $$
>
> The convention used here defines \(\varphi\) as the polar angle from the positive Z-axis.
>
> **Applications:**
>
> - Spherical robot manipulators.
> - Radar and LiDAR geometry.
> - Three-dimensional sensing.
> - Spatial localization.

### 3.7. Basis vectors and coordinate representation

> [!important] Basis representation
> A coordinate system can be described mathematically through its basis vectors.
>
> Let a basis be:
>
> $$
> B=
> \{\mathbf{b}_1,\mathbf{b}_2,\mathbf{b}_3\}
> $$
>
> Any vector in the corresponding three-dimensional vector space can be represented as:
>
> $$
> \mathbf{v}
> =
> v_1\mathbf{b}_1+
> v_2\mathbf{b}_2+
> v_3\mathbf{b}_3
> $$
>
> Its coordinate representation relative to basis \(B\) is:
>
> $$
> [\mathbf{v}]_B=
> \begin{bmatrix}
> v_1\\v_2\\v_3
> \end{bmatrix}
> $$
>
> If the basis vectors are orthonormal, the coordinate system is orthonormal.
>
> For an orthonormal basis:
>
> $$
> \mathbf{b}_i^T\mathbf{b}_j
> =
> \begin{cases}
> 1&i=j\\
> 0&i\neq j
> \end{cases}
> $$
>
> Equivalently:
>
> $$
> \mathbf{B}^T\mathbf{B}=\mathbf{I}
> $$
>
> where the columns of \(\mathbf{B}\) contain the basis vectors.

### 3.8. Transformation between coordinate systems

> [!important] Coordinate transformation
> The same geometric point can have different coordinate representations in different coordinate frames.
>
> Let:
>
> - Frame A be the reference frame.
> - Frame B be another coordinate frame.
> - \({}^A\mathbf{p}\) be the coordinates of a point expressed in A.
> - \({}^B\mathbf{p}\) be the coordinates of the same point expressed in B.
>
> The relationship is:
>
> $$
> \boxed{
> {}^A\mathbf{p}
> =
> {}^A\mathbf{R}_B
> {}^B\mathbf{p}
> +
> {}^A\mathbf{t}_B
> }
> $$
>
> Where:
>
> - \({}^A\mathbf{R}_B\): Orientation of frame B expressed in A.
> - \({}^A\mathbf{t}_B\): Position of the origin of B expressed in A.
>
> Using homogeneous coordinates:
>
> $$
> \boxed{
> \begin{bmatrix}
> {}^A\mathbf{p}\\1
> \end{bmatrix}
> =
> {}^A\mathbf{T}_B
> \begin{bmatrix}
> {}^B\mathbf{p}\\1
> \end{bmatrix}
> }
> $$
>
> Where:
>
> $$
> {}^A\mathbf{T}_B=
> \begin{bmatrix}
> {}^A\mathbf{R}_B&{}^A\mathbf{t}_B\\
> \mathbf{0}^T&1
> \end{bmatrix}
> $$
>
> This transformation changes the coordinate representation without changing the underlying geometric point.

### 3.9. Global and local coordinate systems

> [!abstract] Global coordinate system
> A global coordinate system provides a common reference for describing positions in an environment.
>
> Examples include:
>
> - World frame.
> - Map frame.
> - Earth-centered reference frame.
>
> **Local coordinate system**
>
> A local coordinate system describes positions relative to a specific object, robot, sensor, or location.
>
> Examples include:
>
> - Robot base frame.
> - End-effector frame.
> - Camera frame.
> - LiDAR frame.
> - IMU frame.
>
> The relationship between local and global frames is established through coordinate transformations.

### 3.10. Coordinate frames in a robotic system

> [!info] Typical robotic coordinate frames
>
> A robot commonly uses multiple coordinate frames:
>
> | Frame | Description |
> |---|---|
> | World frame | Global reference for the environment |
> | Map frame | Reference associated with a generated map |
> | Odometry frame | Locally continuous reference for estimated motion |
> | Base frame | Reference attached to the robot body |
> | Joint frame | Reference attached to a robot joint |
> | End-effector frame | Reference attached to the tool or gripper |
> | Camera frame | Reference associated with the camera |
> | LiDAR frame | Reference associated with the LiDAR sensor |
> | IMU frame | Reference associated with the inertial sensor |
>
> These frames form a transformation hierarchy that enables different robotic components to communicate spatial information consistently.

## 4. Applications and Examples

### 4.1. Example: Converting cylindrical coordinates to Cartesian coordinates

> [!example] Coordinate conversion
>
> Given a point in cylindrical coordinates:
>
> $$
> P=(r,\theta,z)=(2,60^\circ,3)
> $$
>
> Convert it into Cartesian coordinates.
>
> Using:
>
> $$
> x=r\cos\theta
> $$
>
> $$
> y=r\sin\theta
> $$
>
> $$
> z=z
> $$
>
> Substitute:
>
> $$
> x=2\cos60^\circ=1
> $$
>
> $$
> y=2\sin60^\circ=\sqrt{3}
> $$
>
> $$
> z=3
> $$
>
> Therefore:
>
> $$
> \boxed{
> P=(1,\sqrt{3},3)
> }
> $$

### 4.2. Example: Transforming coordinates between two frames

> [!example] Frame transformation
>
> Suppose a point is expressed in frame B as:
>
> $$
> {}^B\mathbf{p}=
> \begin{bmatrix}
> 1\\2\\3
> \end{bmatrix}
> $$
>
> Frame B is rotated by \(90^\circ\) around the Z-axis relative to frame A and has an origin at:
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
> The coordinate transformation is:
>
> $$
> {}^A\mathbf{p}
> =
> {}^A\mathbf{R}_B{}^B\mathbf{p}
> +
> {}^A\mathbf{t}_B
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
> {}^A\mathbf{p}
> =
> \begin{bmatrix}
> 0\\1\\4
> \end{bmatrix}
> }
> $$
>
> The same point is represented by different coordinate values in A and B.

### 4.3. Applications in robotics

> [!info] Robot kinematics
>
> Coordinate systems are used to describe:
>
> - Robot base position.
> - Joint locations and orientations.
> - Link configurations.
> - End-effector poses.
> - Relative positions between robot components.
>
> Forward kinematics computes the end-effector pose through a sequence of coordinate transformations:
>
> $$
> {}^0\mathbf{T}_n
> =
> {}^0\mathbf{T}_1
> {}^1\mathbf{T}_2
> \cdots
> {}^{n-1}\mathbf{T}_n
> $$
>
> Each transformation describes the spatial relationship between adjacent coordinate frames.

### 4.4. Applications in swarm robotics

> [!important] Multi-robot coordinate systems
>
> In swarm robotics, multiple robots must represent and exchange spatial information consistently.
>
> Consider a swarm containing robots \(R_1,R_2,\ldots,R_n\).
>
> Each robot may maintain its own local coordinate frame.
>
> A relative position between robots \(i\) and \(j\), expressed in frame \(i\), is:
>
> $$
> {}^i\mathbf{p}_j
> =
> ({}^W\mathbf{R}_i)^T
> ({}^W\mathbf{p}_j-{}^W\mathbf{p}_i)
> $$
>
> Where:
>
> - \(W\): Shared world reference frame.
> - \({}^W\mathbf{p}_i\): Position of robot \(i\) in the world frame.
> - \({}^W\mathbf{p}_j\): Position of robot \(j\) in the world frame.
> - \({}^W\mathbf{R}_i\): Orientation of robot \(i\) relative to the world frame.
>
> This representation is useful for:
>
> 1. Relative localization.
> 2. Formation control.
> 3. Cooperative navigation.
> 4. Distributed mapping.
> 5. Multi-robot collision avoidance.
> 6. Sensor measurement sharing.
>
> **Important:** A shared global frame is not always available in decentralized robotics. Robots may instead estimate relative transformations through inter-robot observations, odometry, or distributed localization algorithms.

### 4.5. Applications in ROS 2

> [!info] ROS 2 coordinate-frame management
>
> ROS 2 uses the `tf2` library to manage transformations between coordinate frames over time.
>
> A typical robotic transformation tree may contain:
>
> - `map`
> - `odom`
> - `base_link`
> - `camera_link`
> - `laser_frame`
> - `imu_link`
>
> Common transformation relationships include:
>
> $$
> {}^{map}\mathbf{T}_{odom}
> $$
>
> $$
> {}^{odom}\mathbf{T}_{base\_link}
> $$
>
> $$
> {}^{base\_link}\mathbf{T}_{camera\_link}
> $$
>
> These transformations allow sensor measurements and robot poses to be expressed in different frames.
>
> Reference:
>
> https://docs.ros.org/en/rolling/Concepts/Intermediate/About-Tf2.html


## 6. Limitations and Evaluation

> [!warning] Important limitations
>
> **1. Coordinate singularities**
>
> Some coordinate representations become singular at particular configurations.
>
> For example, spherical coordinates have an undefined azimuth angle on the Z-axis.
>
> **2. Representation ambiguity**
>
> Different coordinate systems may represent the same physical point or orientation using different numerical values.
>
> **3. Convention inconsistency**
>
> Different software libraries and engineering disciplines may use different axis directions, handedness, units, and rotation conventions.
>
> **4. Numerical precision**
>
> Repeated transformations can introduce floating-point errors.
>
> **5. Frame calibration**
>
> Incorrectly estimated transformations between sensors and robot frames produce systematic localization and perception errors.
>
> **6. Global-frame limitations**
>
> A global coordinate system may not be directly observable in decentralized multi-robot environments.
>
> **7. Time dependence**
>
> Coordinate-frame relationships can change over time, especially when frames are attached to moving robots or articulated components.

> [!tip] Best practices in robotics
>
> - Explicitly identify the source and destination coordinate frames.
> - Use consistent units, preferably SI units.
> - Specify right-handed or left-handed conventions.
> - Document axis directions and rotation conventions.
> - Use homogeneous transformation matrices for rigid 3D frame transformations.
> - Distinguish point coordinates from free-vector coordinates.
> - Validate transformation chains before using them in control or localization.
> - Account for timestamps when transforming measurements from moving sensors.

## 7. Verification and Evidence

> [!success] Established mathematical facts
>
> - Coordinates depend on the selected coordinate system.
> - A coordinate frame is characterized by an origin and an oriented basis.
> - Cartesian coordinates provide a common representation of Euclidean space.
> - Coordinate transformations change numerical representations without necessarily changing the underlying geometric objects.
> - Homogeneous transformations combine rotation and translation.
> - A free rigid body in 3D has six degrees of freedom.
> - Coordinate-frame transformations are fundamental to robot kinematics and sensor fusion.
>
> **Confidence:** 1/5 — Initial familiarity level, not a measure of scientific validity.
>
> **Further study:** Investigate coordinate charts, generalized coordinates, transformation groups, and time-dependent reference frames.

## 8. Personal Notes

> [!question] Questions for further study
>
> - What is the mathematical difference between a coordinate system and a coordinate frame?
> - How do coordinate transformations differ from physical transformations?
> - Why are orthonormal basis vectors important in robotics?
> - What are the differences between Cartesian, cylindrical, and spherical coordinates?
> - How are coordinate frames connected through a transformation tree?
> - Why does ROS 2 distinguish `map`, `odom`, and `base_link`?
> - How can multiple robots establish a common reference frame without GPS?
> - How are coordinate systems represented on Lie groups?
> - How do coordinate conventions affect multi-robot sensor fusion?

## 9. References

1. Murray, R. M., Li, Z., & Sastry, S. S. (1994). *A Mathematical Introduction to Robotic Manipulation*. CRC Press.
   - https://www.cds.caltech.edu/~murray/mlswiki/
   - Mathematical foundations of coordinate frames, rigid-body transformations, and robot manipulation.

2. Lynch, K. M., & Park, F. C. (2017). *Modern Robotics: Mechanics, Planning, and Control*. Cambridge University Press.
   - https://modernrobotics.northwestern.edu/
   - Coordinate frames, rigid transformations, and robot kinematics.

3. Siciliano, B., Sciavicco, L., Villani, L., & Oriolo, G. (2009). *Robotics: Modelling, Planning and Control*. Springer.
   - Robot coordinate systems and manipulator kinematics.

4. ROS 2 Documentation. *tf2: Transform Library*.
   - https://docs.ros.org/en/rolling/Concepts/Intermediate/About-Tf2.html
   - Coordinate-frame transformation management in ROS 2.

5. Barfoot, T. D. (2017). *State Estimation for Robotics*. Cambridge University Press.
   - Mathematical foundations of coordinate transformations, localization, and state estimation.

