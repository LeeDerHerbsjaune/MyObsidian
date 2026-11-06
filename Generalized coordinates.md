---
type: technical-term
title: Generalized Coordinates
aliases:
  - Generalized Coordinate
  - Generalized Position Coordinates
abbreviation: ""
field:
  - Mechanics
  - Robotics
subfield:
  - Analytical Mechanics
  - Multibody Dynamics
  - Robot Kinematics
status: learning
confidence: 2
created: 2026-10-30
updated: 2026-10-30
tags:
  - technical-term
  - mechanics
  - robotics
  - kinematics
sources: []
projects: []
---


## 1. Identification

> [!abstract] Definition
> **Generalized coordinates** are a set of independent variables used to describe the configuration of a mechanical system. They are commonly denoted by $q$ or by the vector $\mathbf{q}$, with the number of independent coordinates typically equal to the system's Degrees of Freedom (DoF).

- **Preferred term:** Generalized coordinates
- **Symbol:** $q_i$ for the $i$-th coordinate; $\mathbf{q}$ for the coordinate vector
- **Domain:** Mechanics, robotics, dynamics, control theory
- **Subdomains:** Analytical mechanics, robot kinematics, multibody dynamics

## 2. Definition and Core Concept

> [!info] Formal definition
> Let a mechanical system have \(n\) degrees of freedom. Its configuration can be represented locally by a vector of \(n\) independent generalized coordinates:
>
> $$
> \mathbf{q} =
> \begin{bmatrix}
> q_1 & q_2 & \cdots & q_n
> \end{bmatrix}^{\mathsf T}
> $$
>
> Each coordinate describes one independent aspect of the system's configuration. The coordinates need not be Cartesian positions; they may be angles, distances, or other suitable parameters.

> [!tip] Intuition
> Generalized coordinates provide a compact way to describe a system's pose without necessarily specifying the Cartesian position of every point.
>
> For example, a planar pendulum can be described by one angle, \(\theta\), instead of the Cartesian coordinates of its bob. Once the angle and pendulum length are known, the bob's position is determined.

### 2.1 Why generalized coordinates are useful

> [!important] Main purposes
> - Represent a mechanical configuration using a minimal set of independent variables.
> - Account for geometric constraints without introducing unnecessary variables.
> - Formulate equations of motion using Lagrangian Mechanics.
> - Describe robot configurations and joint states.
> - Support trajectory planning, simulation, and motion control.

## 3. Technical Representation

### 3.1 Generalized coordinate vector

> [!note] Mathematical representation
> For a system with \(n\) degrees of freedom:
>
> $$
> \mathbf{q} \in \mathcal{Q}
> $$
>
> where \(\mathcal{Q}\) is the system's configuration space.
>
> In a local coordinate representation:
>
> $$
> \mathbf{q} =
> \begin{bmatrix}
> q_1\\
> q_2\\
> \vdots\\
> q_n
> \end{bmatrix}
> $$
>
> The coordinates may have different physical meanings and units. For example, a robot configuration vector can contain both joint angles in radians and joint displacements in meters.

### 3.2 Relationship to Cartesian coordinates

> [!info] Coordinate transformation
> The Cartesian position of a point in a mechanical system can often be expressed as a function of the generalized coordinates:
>
> $$
> \mathbf{x} = \mathbf{f}(\mathbf{q},t)
> $$
>
> where:
>
> - \(\mathbf{x}\) is the Cartesian position vector.
> - \(\mathbf{q}\) is the generalized coordinate vector.
> - \(t\) is time.
> - \(\mathbf{f}\) describes the system's geometry and kinematic relationships.
>
> For a rigid pendulum of length \(l\), with angle \(\theta\) measured from the downward vertical:
>
> $$
> x = l\sin\theta
> $$
>
> $$
> y = -l\cos\theta
> $$
>
> Thus, the single generalized coordinate \(q=\theta\) determines both Cartesian coordinates.

### 3.3 Relationship to degrees of freedom

> [!important] Independence and constraints
> The number of generalized coordinates in a minimal, independent coordinate representation is equal to the number of degrees of freedom of the system.
>
> For \(N\) particles in three-dimensional space, the unconstrained system initially has \(3N\) Cartesian coordinates. If \(m\) independent holonomic constraints reduce the configuration dimension, then, under regularity assumptions:
>
> $$
> n = 3N-m
> $$
>
> More generally, the degrees of freedom equal the dimension of the admissible configuration space. The simple subtraction formula requires independent constraints and does not cover every type of constraint or singular configuration.

### 3.4 Generalized velocities

> [!note] Time derivatives
> The generalized velocity associated with \(q_i\) is:
>
> $$
> \dot{q}_i = \frac{dq_i}{dt}
> $$
>
> Collectively:
>
> $$
> \dot{\mathbf{q}} =
> \begin{bmatrix}
> \dot{q}_1 & \dot{q}_2 & \cdots & \dot{q}_n
> \end{bmatrix}^{\mathsf T}
> $$
>
> Generalized velocities describe the rates of change of the coordinates. Their units depend on the corresponding coordinates.
>
> For example, if \(q_i\) is an angle, \(\dot q_i\) is an angular velocity. If \(q_i\) is a linear displacement, \(\dot q_i\) is a linear velocity.

### 3.5 Generalized coordinates in Lagrangian mechanics

> [!abstract] Lagrangian formulation
> A mechanical system can be described using a Lagrangian:
>
> $$
> L(\mathbf{q},\dot{\mathbf{q}},t)
> = T(\mathbf{q},\dot{\mathbf{q}},t)
> - V(\mathbf{q},t)
> $$
>
> where \(T\) is kinetic energy and \(V\) is potential energy.
>
> For each generalized coordinate \(q_i\), the Euler–Lagrange equation is:
>
> $$
> \frac{d}{dt}
> \left(
> \frac{\partial L}{\partial \dot q_i}
> \right)
> -
> \frac{\partial L}{\partial q_i}
> = Q_i
> $$
>
> Here, \(Q_i\) is the generalized nonconservative force associated with \(q_i\), when such forces are represented explicitly. Conservative forces derived from \(V\) are already included in \(L\).
>
> The generalized-coordinate formulation is especially useful when the system has geometric constraints or when Cartesian equations would require many redundant variables.

## 4. Applications and Examples

### 4.1 Simple pendulum

> [!example] One-degree-of-freedom system
> For an ideal planar pendulum with fixed length \(l\):
>
> $$
> \mathbf{q} = [\theta]
> $$
>
> The bob's Cartesian position is:
>
> $$
> \mathbf{x} =
> \begin{bmatrix}
> l\sin\theta\\
> -l\cos\theta
> \end{bmatrix}
> $$
>
> The system has one degree of freedom because its configuration is determined by a single independent angle.

### 4.2 Two-link planar robot arm

> [!example] Robot kinematics
> For a planar manipulator with two revolute joints:
>
> $$
> \mathbf{q} =
> \begin{bmatrix}
> \theta_1\\
> \theta_2
> \end{bmatrix}
> $$
>
> where \(\theta_1\) and \(\theta_2\) are joint angles.
>
> If the link lengths are \(l_1\) and \(l_2\), the end-effector position is:
>
> $$
> x = l_1\cos\theta_1
> + l_2\cos(\theta_1+\theta_2)
> $$
>
> $$
> y = l_1\sin\theta_1
> + l_2\sin(\theta_1+\theta_2)
> $$
>
> The generalized coordinates describe the joint configuration, while the forward-kinematics equations determine the end-effector pose.

### 4.3 Mobile robot

> [!example] Planar pose
> A mobile robot moving on a plane can often be described by:
>
> $$
> \mathbf{q} =
> \begin{bmatrix}
> x\\
> y\\
> \theta
> \end{bmatrix}
> $$
>
> where \(x,y\) denote position in a world frame and \(\theta\) denotes heading.
>
> This is a pose representation with three configuration variables. However, the robot's feasible instantaneous motions may be restricted by nonholonomic constraints, such as the no-lateral-slip condition of an ideal differential-drive robot. Consequently, three configuration variables do not imply three independently controllable instantaneous velocity components.

## 5. Knowledge Relationships

> [!note] Related concepts
> - Degrees of Freedom (DoF) — the number of independent configuration variables required to describe the system locally.
> - [[Generalized Velocity]] — the time derivative of a generalized coordinate.
> - [[Lagrangian Mechanics]] — a formulation of dynamics based on generalized coordinates, velocities, and the Lagrangian.
> - [[Holonomic Constraint]] — a constraint expressible as a relation among configuration variables and possibly time.
> - Robot Kinematics — the study of relationships between robot configurations and the positions and orientations of its components.

### 5.1 Important distinctions

> [!warning] Generalized coordinates are not necessarily Cartesian coordinates
> Cartesian coordinates are one possible choice of generalized coordinates, but generalized coordinates can also be joint angles, distances, or other independent parameters.
>
> Generalized coordinates are also not necessarily generalized forces. A generalized force \(Q_i\) is associated with a virtual displacement in the corresponding coordinate \(q_i\); its physical unit depends on that coordinate.

## 6. Limitations and Evaluation

> [!important] Coordinate selection
> A good coordinate choice can simplify the equations of motion, but no single coordinate representation is optimal for every problem.
>
> - **Coordinate singularities:** A coordinate chart may fail to represent certain configurations regularly.
> - **Constraints:** A redundant coordinate representation may require explicit constraint equations and additional mathematical machinery.
> - **Nonholonomic systems:** Constraints on velocities cannot generally be eliminated by simply reducing the number of configuration coordinates.
> - **Mixed units:** A coordinate vector may combine angular and translational variables, requiring care in numerical optimization and control.
> - **Global representation:** Some configuration spaces cannot be represented by one nonsingular coordinate chart everywhere.

## 7. Verification and Evidence

> [!info] Established principles
> The definitions and equations in this note follow standard formulations of analytical mechanics and robot kinematics.
>
> The precise number of degrees of freedom depends on the system's configuration space, constraints, and regularity assumptions. The examples above assume idealized mechanisms with the stated geometry.

## 8. Personal Notes

> [!question] Questions for further study
> - How are generalized coordinates selected for a constrained multibody system?
> - How are generalized forces derived from virtual work?
> - How do generalized coordinates relate to the robot Jacobian?
> - How do configuration coordinates differ from state variables in a dynamical system?

## 9. References

- Goldstein, H., Poole, C. P., and Safko, J. L. *Classical Mechanics*, 3rd ed., Addison-Wesley, 2002.
- Murray, R. M., Li, Z., and Sastry, S. S. *A Mathematical Introduction to Robotic Manipulation*. CRC Press, 1994. Available at: https://www.cds.caltech.edu/~murray/mlswiki/

## 10. Knowledge Links and Further Development

> [!tip] Suggested next notes
> 1. [[Degrees of Freedom|Degrees of Freedom (DoF)]]
> 2. Configuration Space
> 3. [[Generalized Velocity]]
> 4. [[Generalized Forces]]
> 5. [[Holonomic Constraint]]
> 6. [[Euler–Lagrange Equation|Euler-Lagrange Equation]]
> 7. Robot Jacobian