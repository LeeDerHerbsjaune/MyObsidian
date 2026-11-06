---
type: technical-term
title: Chebychev–Grübler–Kutzbach Criterion
aliases:
  - Grübler–Kutzbach Criterion
  - Chebychev–Grübler Criterion
  - Kutzbach Criterion
abbreviation: CGK Criterion
field:
  - Mechanical Engineering
  - Robotics
subfield:
  - Mechanism Theory
  - Kinematics
  - Multibody Systems
status: learning
confidence: 1
created: 2026-10-30
updated: 2026-10-30
tags:
  - technical-term
  - robotics
  - mechanism
  - kinematics
  - degrees-of-freedom
sources: []
projects: []
related:
  - "[[MOC - CGK Criterion]]"
---

## 1. Identification

> [!abstract] Definition
> The **Chebychev–Grübler–Kutzbach (CGK) criterion** is a mathematical relationship used to estimate the mobility (number of degrees of freedom) of a mechanical mechanism based on the number of rigid bodies, kinematic joints, and constraints imposed by those joints.
>
> It is widely used in mechanism design, robot kinematics, and multibody system analysis to determine how many independent motions a mechanism can perform.

- **Domain:** Mechanical Engineering and Robotics
- **Subdomain:** Mechanism Kinematics
- **Primary application:** Mobility analysis of mechanical mechanisms
- **Key concept:** Degrees of Freedom (DoF)

## 2. Definition and Core Concept

### 2.1. Fundamental principle

> [!info] Core concept
> A mechanical mechanism consists of rigid bodies connected by joints.
>
> Each rigid body initially possesses a certain number of independent motions. Connecting bodies through joints introduces constraints that eliminate some of these motions.
>
> The CGK criterion estimates the remaining degrees of freedom after accounting for the constraints imposed by the joints.

The mobility of a mechanism depends on three main factors:

1. The number of rigid bodies.
2. The number of kinematic joints.
3. The number of independent constraints imposed by each joint.

### 2.2. General formula for spatial mechanisms

> [!important] Spatial Chebychev–Grübler–Kutzbach criterion
>
> For a mechanism composed of rigid bodies moving in three-dimensional space:
>
> $$
> M = 6(N-1-J) + \sum_{i=1}^{J} f_i
> $$
>
> Equivalently:
>
> $$
> \boxed{M = 6(N-1-J)+\sum_{i=1}^{J}f_i}
> $$
>
> Where:
>
> - $M$: Mobility or total degrees of freedom of the mechanism.
> - $N$: Total number of rigid bodies, including the ground link.
> - $J$: Total number of kinematic joints.
> - $f_i$: Relative degrees of freedom permitted by joint \(i\).
> - $6$: Degrees of freedom of a free rigid body in three-dimensional space.
>
> The term \(N-1\) represents the number of moving bodies relative to the grounded body.

### 2.3. General formula for planar mechanisms

> [!important] Planar Chebychev–Grübler–Kutzbach criterion
>
> For mechanisms whose motion is restricted to a plane:
>
> $$
> \boxed{M = 3(N-1-J)+\sum_{i=1}^{J}f_i}
> $$
>
> Where:
>
> - $M$: Mobility of the mechanism.
> - $N$: Total number of rigid bodies, including the ground link.
> - $J$: Total number of joints.
> - $f_i$: Relative degrees of freedom permitted by joint \(i\).
> - $3$: Degrees of freedom of a planar rigid body.
>
> A free planar rigid body has:
> - Two translational degrees of freedom: \(x,y\).
> - One rotational degree of freedom: \(\theta\).

## 3. Technical Representation

### 3.1. Degrees of freedom of rigid bodies

> [!info] Rigid-body mobility
> The number of independent motions of a free rigid body depends on the dimensionality of its configuration space.
>
> **Three-dimensional space:**
>
> $$
> DoF_{\text{spatial}}=6
> $$
>
> $$
> DoF = 3T+3R
> $$
>
> - Three translational motions: $T_x,T_y,T_z$.
> - Three rotational motions: $R_x,R_y,R_z$.
>
> **Two-dimensional space:**
>
> $$
> DoF_{\text{planar}}=3
> $$
>
> $$
> DoF = 2T+1R
> $$
>
> - Two translational motions: $T_x,T_y$.
> - One rotational motion: $R_z$.

### 3.2. Common kinematic joints

> [!info] Joint degrees of freedom
> A kinematic joint constrains the relative motion between two connected rigid bodies.
>
> The following table shows common joints and their permitted relative degrees of freedom.

| Joint type | Spatial DoF | Constraints |
|---|---:|---:|
| Fixed (Weld) | 0 | 6 |
| Revolute (R) | 1 | 5 |
| Prismatic (P) | 1 | 5 |
| Helical (H) | 1 | 5 |
| Cylindrical (C) | 2 | 4 |
| Universal (U) | 2 | 4 |
| Spherical (S) | 3 | 3 |
| Planar | 3 | 3 |
| Free joint | 6 | 0 |

> [!note] Important distinction
> The number of constraints imposed by a joint is:
>
> $$
> c_i = 6-f_i
> $$
>
> for spatial mechanisms.
>
> For planar mechanisms:
>
> $$
> c_i = 3-f_i
> $$
>
> These expressions assume ideal joints and count independent constraints.

### 3.3. Constraint-based formulation

> [!info] Constraint formulation
> An alternative way to understand mobility is to consider the configuration variables and independent constraint equations.
>
> For a spatial mechanism:
>
> $$
> M = 6(N-1)-C
> $$
>
> where \(C\) is the total number of independent kinematic constraints.
>
> If all joint constraints are independent:
>
> $$
> C=\sum_{i=1}^{J}(6-f_i)
> $$
>
> Therefore:
>
> $$
> M=6(N-1)-\sum_{i=1}^{J}(6-f_i)
> $$
>
> This simplifies to the spatial CGK formula.
>
> **Important:** The number of constraint equations is not necessarily equal to the number of independent constraints. Redundant constraints and special geometric configurations can change the actual mobility.

## 4. Applications and Examples

### 4.1. Example: Four-bar planar linkage

> [!example] Mobility calculation
> Consider a conventional planar four-bar linkage.
>
> Given:
>
> - Number of links: \(N=4\).
> - Number of revolute joints: \(J=4\).
> - Each revolute joint permits one relative degree of freedom: $f_i=1$.
>
> Using the planar CGK criterion:
>
> $$
> M=3(N-1-J)+\sum_{i=1}^{J}f_i
> $$
>
> Substitute the values:
>
> $$
> M=3(4-1-4)+4(1)
> $$
>
> $$
> M=3(-1)+4
> $$
>
> $$
> \boxed{M=1}
> $$
>
> **Interpretation:**
>
> The four-bar linkage has one degree of freedom. Therefore, specifying the input angle of one moving link determines the configuration of the remaining links, subject to assembly and geometric constraints.

### 4.2. Example: Spatial serial robot manipulator

> [!example] Six-joint serial manipulator
> Consider a spatial serial robot consisting of:
>
> - One ground link.
> - Six moving links.
> - Six revolute joints.
>
> Therefore:
>
> $$
> N=7,\quad J=6,\quad f_i=1
> $$
>
> Applying the spatial criterion:
>
> $$
> M=6(N-1-J)+\sum_{i=1}^{J}f_i
> $$
>
> $$
> M=6(7-1-6)+6(1)
> $$
>
> $$
> \boxed{M=6}
> $$
>
> **Interpretation:**
>
> The serial manipulator has six joint variables and therefore has six nominal degrees of freedom.
>
> This does not guarantee that its end-effector can reach every arbitrary pose. Reachability and instantaneous motion capability also depend on the manipulator geometry and its Jacobian matrix.

### 4.3. Applications in robotics

> [!info] Engineering applications
> The CGK criterion is useful in:
>
> - **Robot architecture design:** Estimating the mobility of serial and parallel robots.
> - **Mechanism synthesis:** Determining the number of joints and links required for a desired mobility.
> - **Parallel manipulators:** Estimating the mobility of closed-chain robotic systems.
> - **Mechanical system analysis:** Evaluating the kinematic structure of linkages.
> - **Redundancy analysis:** Identifying mechanisms with more available motion variables than required for a particular task, subject to the criterion's assumptions.

## 6. Limitations and Evaluation

> [!warning] Limitations of the CGK criterion
>
> The CGK criterion is a mobility-counting formula, not a universal proof of actual mechanism mobility.
>
> Its main assumptions and limitations include:
>
> 1. **Independent constraints:** It generally assumes that the constraints introduced by joints are independent.
>
> 2. **Generic configurations:** Special geometric arrangements can produce additional instantaneous freedoms or singularities.
>
> 3. **Redundant constraints:** Some joint constraints may be dependent, causing the criterion to underestimate mobility.
>
> 4. **Overconstrained mechanisms:** Certain mechanisms possess structural or geometric properties that cannot be correctly characterized by simple link-and-joint counting.
>
> 5. **Geometric dependence:** Joint-axis alignment and special link arrangements may significantly affect actual mobility.
>
> 6. **Negative mobility predictions:** A negative result does not represent a physically meaningful negative number of degrees of freedom. It indicates that the simple counting assumptions are insufficient for that mechanism.

> [!important] When to use another method
> For complex parallel robots, overconstrained mechanisms, and mechanisms near singular configurations, use:
>
> - Constraint Jacobian rank analysis.
> - Screw theory.
> - Reciprocal screw analysis.
> - Instantaneous mobility analysis.
>
> These methods provide a more detailed understanding of the mechanism's actual kinematic freedoms.

## 7. Verification and Evidence

> [!success] Established technical facts
>
> - A free rigid body has six degrees of freedom in three-dimensional space.
> - A free rigid body has three degrees of freedom in planar motion.
> - The CGK criterion estimates mobility from the number of links and joint freedoms.
> - The independence of constraints is essential to the accuracy of the counting method.
> - Jacobian rank analysis provides a systematic approach to determining local mobility.
>
> **Confidence:** The fundamental equations and their standard assumptions are established results in classical mechanism theory.
>
> **Further verification required:** Specialized overconstrained mechanisms should be analyzed using their actual constraint equations or screw-system structure.

## 8. Personal Notes

> [!question] Questions for further study
>
> - Why can the CGK criterion fail for certain parallel manipulators?
> - How does screw theory explain the mobility of spatial mechanisms?
> - What is the relationship between mechanism mobility and Jacobian rank?
> - How do singular configurations affect the instantaneous degrees of freedom of a robot?
> - How can the criterion be extended to mechanisms with multiple closed kinematic loops?

## 9. References

1. **Uicker, J. J., Pennock, G. R., & Shigley, J. E.** (2017). *Theory of Machines and Mechanisms* (5th ed.). Oxford University Press.
   - A standard textbook covering mechanism mobility, kinematic analysis, and linkage synthesis.

2. **Murray, R. M., Li, Z., & Sastry, S. S.** (1994). *A Mathematical Introduction to Robotic Manipulation*. CRC Press.
   - https://www.cds.caltech.edu/~murray/mlswiki/
   - Mathematical foundations of robot kinematics, rigid-body transformations, and screw theory.

3. **Gogu, G.** (2005). *Structural Synthesis of Parallel Robots, Part 1: Methodology*. Springer.
   - A reference on structural synthesis and mobility analysis of parallel mechanisms.

