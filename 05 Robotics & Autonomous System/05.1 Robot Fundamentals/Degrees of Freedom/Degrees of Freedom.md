---
type: technical-term
title: Degrees of Freedom
aliases:
  - DoF
  - DOF
  - Degrees of Freedom in Robotics
abbreviation: DoF
field:
  - Robotics
  - Mechanical Engineering
subfield:
  - Robot Kinematics
  - Mechanism Theory
  - Configuration Space
status: learning
confidence: 3
created: 2026-10-30
updated: 2026-10-30
tags:
  - technical-term
  - engineering
  - robotics
  - kinematics
sources:
  - "[https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-1-degrees-of-freedom-of-a-rigid-body/](https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-1-degrees-of-freedom-of-a-rigid-body/)"
  - "[https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-2-degrees-of-freedom-of-a-robot/](https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-2-degrees-of-freedom-of-a-robot/)"
related:
  - "[[📍 MOC - Degrees of Freedom]]"
projects: []
Essence: "[[Degrees of Freedom]]"
---

## 1. Identification

- **Standard English term:** Degrees of Freedom
    
- **Abbreviation:** DoF or DOF
    
- **Field:** Robotics, mechanical engineering, mechanics, control engineering, and applied mathematics
    
- **Subfields:** Robot kinematics, mechanism mobility, configuration-space analysis, and multibody dynamics
    
- **Synonyms:** Degrees of freedom of a system; kinematic degrees of freedom; mobility, in mechanism theory.
    
- **Related terms:** Independent coordinates, generalized coordinates, configuration, configuration space, kinematic constraints, joint mobility, and actuation.
    
- **Relevant reference:** Kevin M. Lynch and Frank C. Park, _Modern Robotics: Mechanics, Planning, and Control_ (2017), Chapter 2.
    

The exact interpretation depends on the discipline. In robot kinematics, DoF generally describes the dimension of a robot's configuration space. In statistics, it has a different meaning associated with independent information available for estimation or inference.

> [!important] Scope  
> This note focuses on **mechanical and robotic degrees of freedom**, not statistical degrees of freedom.

## 2. Definition & Core Concept — Định nghĩa và bản chất

### 2.1 Formal definition

Following Lynch and Park's treatment in _Modern Robotics_, the degrees of freedom of a robot are the minimum number of independent real-valued coordinates required to represent its configuration.

Let:

- $q$ denote a configuration vector.
    
- $\mathcal{C}$ denote the configuration space.
    
- $n$ denote the number of degrees of freedom.
    

Locally, the configuration can be represented by (n) independent coordinates:

$$  
q = [q_1,q_2,\ldots,q_n]^T  
$$

The number of degrees of freedom is the dimension of the configuration space:

$$  
\boxed{\mathrm{DoF}=\dim(\mathcal{C})}  
$$

This definition concerns configuration, such as joint positions and rigid-body pose. It does not, by itself, count velocities, forces, actuators, or all variables required to describe a system's dynamic state.

**Source:** Lynch and Park, _Modern Robotics_, Chapter 2, especially Sections 2.1–2.2.

### 2.2 Intuitive explanation

Imagine describing the position of a door.

If the door rotates around a fixed hinge, you only need one independent variable: its opening angle (\theta). Once that angle is known, its position is determined by the hinge geometry.

Therefore, the door has one degree of freedom.

Now imagine a robot arm with six independent revolute joints. If its base is fixed and the joints are independently movable, six joint angles are sufficient to specify its configuration.

The robot therefore has six degrees of freedom.

The essential question is:

**How many independent continuous quantities must I choose to determine the configuration of the entire system?**

### 2.3 What problem does DoF solve?

DoF helps engineers determine:

1. How many independent coordinates are needed to model a mechanism.
    
2. Which motions a robot can perform.
    
3. Whether a manipulator has enough mobility to achieve a desired pose.
    
4. How mechanical constraints reduce possible motion.
    
5. Whether a robot is kinematically redundant.
    
6. How to formulate motion planning, inverse kinematics, and control problems.
    

### 2.4 Core principles

- **Independence:** Each coordinate must contribute an independent degree of freedom.
    
- **Constraints:** Geometric and mechanical constraints can reduce the number of independent coordinates.
    
- **Configuration:** DoF characterizes the possible configurations, not necessarily the dynamic state.
    
- **Local dimensionality:** For constrained or nonlinear systems, the number of DoF is generally the local dimension of the admissible configuration manifold.
    
- **Representation independence:** The same configuration may have multiple mathematical representations. The number of DoF is not necessarily the number of entries in every possible representation.
    

### 2.5 A useful mental model

Think of DoF as the number of independent controls needed to choose a configuration, assuming those controls correspond to independent coordinates.

| System                                                | Independent coordinates                                  | DoF |
| ----------------------------------------------------- | -------------------------------------------------------- | --- |
| Point constrained to a straight line                  | Position along the line                                  | 1   |
| Point moving on a plane                               | ($x$,$y$)                                                | 2   |
| Rigid body moving in a plane                          | ($x,y,\theta$)                                           | 3   |
| Free rigid body in 3D                                 | Three position and three orientation coordinates locally | 6   |
| Fixed-base robot with six independent revolute joints | Six joint angles                                         | 6   |

> [!warning] Limitation of the mental model  
> DoF is not always equal to the number of visible joints, motors, or variables in a software model. Coupled joints, closed kinematic chains, constraints, and redundant coordinate representations can change the relationship.

## 3. Technical Representation — Biểu diễn kỹ thuật

### 3.1 Degrees of freedom of a rigid body

For a rigid body in three-dimensional Euclidean space, a configuration consists of its position and orientation.

The position requires three independent coordinates:

$$  
p = [x,y,z]^T  
$$

The orientation has three independent degrees of freedom. One common local representation uses roll, pitch, and yaw angles.

Thus:

$$  
\boxed{\mathrm{DoF}_{\text{rigid body, 3D}}=3+3=6}  
$$

For planar motion:

$$  
\boxed{\mathrm{DoF}_{\text{rigid body, 2D}}=2+1=3}  
$$

| Motion type                       | Coordinates                         | DoF |
| --------------------------------- | ----------------------------------- | --- |
| Translation in 2D                 | ($x,y$)                             | 2   |
| Rotation in 2D                    | ($\theta$)                          | 1   |
| General planar rigid-body motion  | ($x,y,\theta$)                      | 3   |
| Translation in 3D                 | ($x,y,z$)                           | 3   |
| Orientation in 3D                 | Three local orientation coordinates | 3   |
| General spatial rigid-body motion | Position and orientation            | 6   |

**Coordinate convention:** Roll, pitch, and yaw depend on the selected axes and rotation order. They are not globally nonsingular coordinates for all possible orientations.

A rigid-body pose can instead be represented by a homogeneous transformation matrix in (SE(3)), which contains 16 matrix entries but only six independent configuration dimensions.

### 3.2 General constraint-counting principle

For a system with $n$ unconstrained coordinates and $m$ independent holonomic constraints:

$$  
f(q)=0,\qquad f:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}  
$$

If the constraint Jacobian has full row rank $m$ at the configuration of interest, the local configuration-space dimension is:

$$  
\boxed{\mathrm{DoF}=n-m}  
$$

where:

- $n$ is the number of coordinates before imposing constraints.
    
- $m$ is the number of independent scalar constraints.
    
- $f(q)$ is the vector of constraint equations.
    
- $q$ is the vector of generalized coordinates.
    

The constraint Jacobian is:

$$  
J_c(q)=\frac{\partial f}{\partial q}  
$$

When the rank is not (m), the local dimension is determined by the rank of the Jacobian, subject to the regularity of the constraint set:

$$  
\boxed{\mathrm{DoF}=n-\operatorname{rank}(J_c)}  
$$

This rank-based expression is a local result under suitable regularity assumptions. At singular configurations, the dimension or local structure may require more careful analysis.

> [!note] Independence matters  
> Two equations that appear different may represent dependent constraints. Subtracting the number of equations rather than the number of independent constraints can produce an incorrect DoF count.

### 3.3 Velocity-level interpretation

Differentiating a differentiable holonomic constraint gives:

$$  
J_c(q)\dot q=0  
$$

The admissible instantaneous velocities belong to the null space of the constraint Jacobian.

Under regularity assumptions:

$$  
\boxed{\mathrm{DoF}=\dim\ker(J_c)=n-\operatorname{rank}(J_c)}  
$$

This is useful in robot kinematics, constrained motion, and mechanism analysis.

For nonholonomic systems, such as idealized rolling robots, velocity constraints may restrict instantaneous motion without reducing the dimension of the configuration space in the same way as holonomic position constraints. Therefore, distinguish configuration-space dimension from instantaneous mobility when analyzing nonholonomic mechanisms.

### 3.4 Joint-based counting

For a fixed-base serial robot with independently variable joints:

$$  
\boxed{\mathrm{DoF}=\sum_{i=1}^{J} f_i}  
$$

where:

- $J$ is the number of joints.
    
- $f_i$ is the independent mobility of joint $i$.
    

Examples:

- Revolute joint: 1 DoF.
    
- Prismatic joint: 1 DoF.
    
- Helical joint: 1 DoF.
    
- Cylindrical joint: 2 DoF.
    
- Spherical joint: 3 DoF.
    

This formula applies directly when the joint coordinates are independent and there are no additional loop-closure or other constraints reducing mobility.

### 3.5 Grübler–Kutzbach mobility criterion

For many ideal mechanisms consisting of rigid links and lower-pair joints, a commonly used mobility criterion is:

$$  
\boxed{M=m(N-1-J)+\sum_{i=1}^{J}f_i}  
$$

where:

- $M$: predicted mechanism mobility.
    
- $m$: DoF of a free rigid body in the relevant motion space; ($m$=3) for planar motion and ($m$=6) for spatial motion.
    
- $N$: number of links, including the fixed ground link.
    
- $J$: number of joints.
    
- $f_i$: relative DoF permitted by joint (i).
    

Equivalently:

$$  
M=m(N-1)-\sum_{i=1}^{J}(m-f_i)  
$$

The formula assumes the idealized constraint structure used in its derivation. Special geometry, redundant constraints, singularities, and overconstrained mechanisms can cause the predicted mobility to differ from the actual mobility.

Do not apply the formula blindly to arbitrary parallel robots or mechanisms with special geometric dependencies.

### 3.6 Units and dimensional consistency

DoF is a dimensionless count.

However, its coordinates can have physical units:

- Revolute-joint coordinate: radians.
    
- Prismatic-joint coordinate: metres.
    
- Planar position: metres.
    
- Orientation parameters: radians.
    

The count of DoF has no SI unit, even when its coordinates do.

## 4. Applications & Examples — Ứng dụng và ví dụ

### 4.1 Example A: A fixed-base 2R planar manipulator

Consider a robot arm consisting of two rigid links connected by two independent revolute joints.

Let:

$$  
q=[\theta_1,\theta_2]^T  
$$

The joint coordinates are:

- $\theta_1$: angle of the first link relative to the base frame.
    
- $\theta_2$: angle of the second link relative to the first link.
    

The configuration space is locally two-dimensional:

$$  
\mathcal{C}=S^1\times S^1  
$$

Therefore:

$$  
\boxed{\mathrm{DoF}=2}  
$$

The end-effector position for link lengths ($l_1,l_2$) is:

$$  
x=l_1\cos\theta_1+l_2\cos(\theta_1+\theta_2)  
$$

$$  
y=l_1\sin\theta_1+l_2\sin(\theta_1+\theta_2)  
$$

The end-effector position has two Cartesian components, but its pose is constrained by the two joint variables. In general, the arm cannot independently specify an arbitrary planar position and orientation, which would require three independent task-space coordinates.

### 4.2 Example B: A free rigid body

A free rigid body in 3D has six configuration DoF.

A desired pose may be described locally by:

$$  
q=[x,y,z,\phi,\theta,\psi]^T  
$$

where ($\phi,\theta,\psi$) represent a chosen roll-pitch-yaw convention.

This provides three translational and three rotational coordinates.

However, a six-DoF robot does not automatically reach every pose in space. Link geometry, joint limits, collisions, singularities, and workspace boundaries still matter.

### 4.3 Example C: A mobile robot

An idealized differential-drive robot moving on a plane is often represented by:

$$  
q=[x,y,\theta]^T  
$$

Its configuration space has three dimensions:

$$  
\dim(\mathcal{C})=3  
$$

But its instantaneous velocity is constrained by ideal rolling without lateral slip. A common kinematic model is:

$$  
\dot{x}=v\cos\theta  
$$

$$  
\dot{y}=v\sin\theta  
$$

$$  
\dot{\theta}=\omega  
$$

where $v$ is the forward speed in m/s and $\omega$ is the yaw rate in rad/s.

The robot has three configuration DoF but only two independently commanded velocity inputs in this model. It cannot move instantaneously in an arbitrary lateral direction.

This distinction is especially important in mobile robotics.

### 4.4 Example D: DoF in swarm robotics

For a swarm of $N$ point robots moving independently in a two-dimensional workspace, ignoring collisions and other inter-robot constraints, the collective configuration can be represented by:

$$  
q=[x_1,y_1,x_2,y_2,\ldots,x_N,y_N]^T  
$$

Each robot contributes two independent position coordinates:

$$  
\boxed{\mathrm{DoF}_{\text{swarm}}=2N}  
$$

For example, five independently moving planar point robots have ten configuration DoF under these assumptions.

If each robot also has an independently variable heading:

$$  
q=[x_1,y_1,\theta_1,\ldots,x_N,y_N,\theta_N]^T  
$$

then:

$$  
\boxed{\mathrm{DoF}_{\text{swarm}}=3N}  
$$

for the unconstrained configuration model.

**Important qualification:** These counts describe the configuration space, not the number of independent control inputs. Collision avoidance, formation constraints, communication-dependent control laws, and nonholonomic motion constraints may restrict feasible trajectories without necessarily reducing the configuration-space dimension.

### 4.5 Example E: Independent constraints

Suppose a mechanical model has four generalized coordinates:

$$  
q=[q_1,q_2,q_3,q_4]^T  
$$

and two independent holonomic constraints:

$$  
f_1(q)=q_1+q_2=0  
$$

$$  
f_2(q)=q_3-q_4=0  
$$

The constraint Jacobian is:

$$  
J_c=  
\begin{bmatrix}  
1&1&0&0\  
0&0&1&-1  
\end{bmatrix}  
$$

Since its rank is two:

$$  
\mathrm{DoF}=4-2=2  
$$

This is a mathematical illustration, not a physical experiment. It demonstrates how independent constraints reduce the dimension of the admissible configuration space.


## 6. Limitations & Evaluation — Giới hạn và đánh giá

### 6.1 Strengths

- Provides a compact description of system mobility.
    
- Helps select robot architectures and joint configurations.
    
- Supports kinematic modeling, trajectory planning, and mechanism design.
    
- Reveals whether a task may require more independent motion capability.
    
- Offers a principled way to analyze the effect of constraints.
    

### 6.2 Limitations

- A DoF count alone does not identify which motions are possible.
    
- It does not describe reachable workspace, dexterity, accuracy, speed, or payload.
    
- It does not guarantee independent actuation or controllability.
    
- A simple constraint count may fail for dependent constraints or special geometries.
    
- The dimension of the configuration space does not reveal its topology.
    
- Singular configurations may have different instantaneous motion properties from generic configurations.
    

### 6.3 Evaluation checklist

When calculating a mechanism's DoF:

1. Identify the bodies and the ground reference.
    
2. Choose independent or redundant generalized coordinates explicitly.
    
3. Identify all mechanical and geometric constraints.
    
4. Determine the rank of the independent constraint set.
    
5. Check whether the analysis is local or global.
    
6. Check for special configurations and singularities.
    
7. Distinguish configuration DoF from actuation and instantaneous mobility.
    
8. Validate the result against a kinematic model or independent analysis when necessary.
    

## 7. Verification & Evidence — Kiểm chứng và bằng chứng

### 7.1 Established theory

The relationship between configuration-space dimension and DoF is established in robot kinematics and mechanism theory. The six DoF of a free rigid body in 3D and the three DoF of a planar rigid body follow from their respective configuration representations.

### 7.2 Analytical verification

For a constrained model (f(q)=0), compute:

$$  
J_c(q)=\frac{\partial f}{\partial q}  
$$

Then, at a regular configuration:

$$  
\mathrm{DoF}=n-\operatorname{rank}(J_c(q))  
$$

A reproducible verification should specify the configuration at which the Jacobian is evaluated, since its rank can vary with configuration.

### 7.3 Suggested numerical check

```
import numpy as np

J_c = np.array([
    [1.0, 1.0, 0.0, 0.0],
    [0.0, 0.0, 1.0, -1.0],
])

n_coordinates = 4
constraint_rank = np.linalg.matrix_rank(J_c)
dof = n_coordinates - constraint_rank

print("Constraint rank:", constraint_rank)
print("Degrees of freedom:", dof)
```

Expected output:

```
Constraint rank: 2
Degrees of freedom: 2
```

This is a reproducible numerical illustration of a supplied constraint matrix. It is not evidence from a physical mechanism or a robot simulation.

### 7.4 Verification status

- **Theoretical definition:** Supported by the cited robotics textbook and its educational materials.
    
- **Analytical example:** Derived directly from the stated constraints.
    
- **Numerical example:** Expected result follows from the supplied matrix; execution has not been independently reported here.
    
- **Physical experiment:** Not performed.
    
- **Special mechanisms:** Require case-specific validation when constraint dependencies, singularities, or nonholonomic conditions are present.
    

## 8. Personal Notes — Ghi chú cá nhân

### 8.1 Memory aid

> Count the independent continuous choices needed to specify the configuration.

For a free rigid body in 3D:

- Three coordinates specify position.
    
- Three coordinates specify orientation.
    
- Total: six DoF.
    

For a planar differential-drive robot:

- Three configuration coordinates: (x,y,\theta).
    
- Two independent velocity inputs in the idealized model.
    
- Therefore, configuration dimension and instantaneous input dimension differ.
    

### 8.2 Common misconceptions

- A robot with six DoF is not guaranteed to reach every 6D pose.
    
- Six joints do not necessarily imply six independent DoF.
    
- An unactuated joint can still contribute a mechanical DoF.
    
- A velocity constraint does not always reduce configuration-space dimension.
    
- A six-DoF pose representation does not require exactly six numbers in every possible data structure.
    

### 8.3 Learning prompts

- Explain why a free rigid body has six DoF.
    
- Derive the DoF of a planar 2R manipulator.
    
- Distinguish configuration DoF from control inputs for a differential-drive robot.
    
- Compute the rank of a constraint Jacobian.
    
- Explain why closed-chain robots need more careful mobility analysis.
    
- Relate manipulator DoF to Jacobian rank and task-space motion.
    

**Current knowledge gaps:** Personal mastery, implementation experience, and unresolved questions are not yet documented.

## 9. References — Tài liệu tham khảo

1. Lynch, K. M., and Park, F. C. (2017). _Modern Robotics: Mechanics, Planning, and Control_. Cambridge University Press. Chapter 2, "Configuration Space."
    
    - [Publisher chapter: Configuration Space](https://doi.org/10.1017/9781316661239.005)
        
    - [Section 2.1: Degrees of Freedom of a Rigid Body](https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-1-degrees-of-freedom-of-a-rigid-body/)
        
    - [Section 2.2: Degrees of Freedom of a Robot](https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-2-degrees-of-freedom-of-a-robot/)
        
2. IEEE Robotics and Automation Society. _Robotics and Automation Society University — Kinematics_.
    
    - [IEEE RAS educational resource](https://www.ieee-ras.org/ras-university/)
        
3. Hauser, K. _Robotic Systems: Kinematics_. University of Illinois Urbana-Champaign.
    
    - [Kinematics educational notes](https://motion.cs.illinois.edu/RoboticSystems/Kinematics.html)
        

The cited sources support the core definitions and robotics examples. Particular mobility calculations should be checked against the assumptions of the mechanism under consideration.

