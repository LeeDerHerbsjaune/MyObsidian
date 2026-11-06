---
type: technical-term
title: "Mechanical Systems"
aliases:
  - Mechanical System
field:
  - Physics
  - Mechanics
subfield:
  - Classical Mechanics
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mechanics
  - physical-systems
sources: []
related: []
projects: []
---

# Mechanical Systems

> [!abstract] Definition
> A **Mechanical System** is a physical system consisting of one or more bodies or material components whose motion, equilibrium, and mechanical interactions are studied using the principles of mechanics.
>
> A mechanical system is characterized by its physical components, configuration, degrees of freedom, constraints, mass distribution, and interactions with external and internal forces.
>
> In classical mechanics, mechanical systems are represented through mathematical models that describe their configurations and temporal evolution.

## 1. Fundamental Characteristics

### 1.1 System Components

> [!info] Physical Components
> A mechanical system may consist of:
>
> - **Particles:** Idealized bodies whose spatial dimensions are neglected.
> - **Rigid Bodies:** Bodies whose internal distances remain constant.
> - **Deformable Bodies:** Bodies whose shapes and dimensions can change under applied loads.
> - **Continuous Media:** Materials modeled as continuously distributed matter.
>
> The appropriate representation depends on the physical properties and mechanical behavior being investigated.

### 1.2 System Configuration

> [!definition] Configuration
> The **configuration** of a mechanical system describes the positions and orientations of all its components at a given instant.
>
> A configuration can be represented by a set of generalized coordinates:
>
> $$\mathbf{q} = (q_1,q_2,\ldots,q_n)$$
>
> where $n$ represents the number of independent generalized coordinates needed to specify the system's configuration.
>
> The collection of all admissible configurations forms the system's configuration space.

### 1.3 Degrees of Freedom

> [!definition] Degrees of Freedom
> The **degrees of freedom (DOF)** of a mechanical system are the minimum number of independent coordinates required to uniquely specify its configuration.
>
> For a system described by generalized coordinates:
>
> $$\mathbf{q} \in \mathbb{R}^n$$
>
> the number of degrees of freedom is $n$, provided the coordinates are independent and locally unconstrained.
>
> Constraints may reduce the number of independent degrees of freedom.

### 1.4 Mass Distribution

> [!definition] Mass Distribution
> Mass distribution describes how mass is spatially distributed throughout a mechanical system.
>
> It influences:
>
> - Translational inertia.
> - Rotational inertia.
> - Center-of-mass position.
> - Angular momentum.
> - Response to applied forces and torques.
>
> Depending on the model, mass may be concentrated at discrete points or distributed continuously throughout a body.

## 2. Classification of Mechanical Systems

> [!abstract] Classification Principle
> Mechanical systems can be classified according to their physical representation, number of components, motion characteristics, and interaction with their surroundings.
>
> These classification dimensions are independent and should not be interpreted as mutually exclusive categories.

### 2.1 According to Physical Representation

#### Particle Systems

> [!definition] Particle System
> A particle system represents a mechanical system as one or more particles with negligible spatial dimensions.
>
> Its mechanical state is described primarily through particle positions and velocities.
>
> Common examples include:
>
> - Single-particle systems.
> - Two-particle systems.
> - Systems of interacting particles.

#### Rigid Body Systems

> [!definition] Rigid Body System
> A rigid-body system consists of one or more rigid bodies whose internal distances remain constant during motion.
>
> Its configuration involves translational and rotational coordinates.
>
> Examples include:
>
> - Rotating disks.
> - Mechanical linkages.
> - Robotic manipulators.
> - Gear mechanisms.

#### Deformable Body Systems

> [!definition] Deformable Body System
> A deformable-body system consists of bodies whose shapes or dimensions can change under mechanical loading.
>
> Its behavior involves deformation, displacement, stress, and strain.
>
> Examples include:
>
> - Elastic structures.
> - Flexible beams.
> - Springs.
> - Deformable robotic components.

#### Continuum Systems

> [!definition] Continuum System
> A continuum system represents matter as a continuously distributed medium rather than a collection of discrete particles.
>
> Its mechanical state is described using spatially and temporally varying field quantities.
>
> Examples include:
>
> - Fluids.
> - Elastic solids.
> - Plastic materials.

### 2.2 According to Number of Components

> [!definition] Single-Body System
> A mechanical system modeled as one body, such as a single rigid body or particle.

> [!definition] Multibody System
> A mechanical system consisting of multiple interconnected or interacting bodies.
>
> Its components may be connected through joints, constraints, or mechanical interactions.
>
> Examples include:
>
> - Robotic manipulators.
> - Vehicle suspension systems.
> - Walking mechanisms.
> - Industrial machinery.

### 2.3 According to Motion Characteristics

> [!definition] Static System
> A mechanical system whose configuration remains unchanged with respect to time under the conditions being studied.
>
> Static equilibrium generally requires:
>
> $$\sum_i \mathbf{F}_i = \mathbf{0}$$
>
> $$\sum_i \boldsymbol{\tau}_i = \mathbf{0}$$

> [!definition] Dynamic System
> A mechanical system whose configuration or mechanical state evolves with time.
>
> Its evolution is governed by equations of motion.

> [!definition] Oscillatory System
> A mechanical system that exhibits periodic or approximately periodic motion around an equilibrium configuration.
>
> Examples include:
>
> - Mass-spring systems.
> - Pendulums.
> - Mechanical vibration systems.

### 2.4 According to Interaction with the Environment

> [!definition] Isolated Mechanical System
> An idealized system that does not exchange energy or momentum with its surroundings.

> [!definition] Closed Mechanical System
> A system whose membership remains fixed, although external forces and energy transfer may occur.
>
> In mechanical modeling, the distinction between a closed system and an isolated system is important: a closed system may still interact mechanically with its environment.

> [!definition] Open Mechanical System
> A system in which matter can cross the system boundary.
>
> Such models are particularly relevant to systems involving mass flow.

## 3. Mathematical Representation

### 3.1 Configuration Space

> [!definition] Configuration Space
> The configuration space is the mathematical space containing all admissible configurations of a mechanical system.
>
> It is commonly denoted by:
>
> $$\mathcal{Q}$$
>
> A system's configuration is represented by:
>
> $$\mathbf{q} \in \mathcal{Q}$$
>
> For systems with constraints, the configuration space may have a geometric structure more general than Euclidean space.

### 3.2 State Space

> [!definition] State
> The state of a mechanical system contains sufficient information to determine its future evolution under a specified dynamical model.
>
> For a standard second-order mechanical system, the state can be represented by:
>
> $$\mathbf{x} =
> \begin{bmatrix}
> \mathbf{q}\\
> \dot{\mathbf{q}}
> \end{bmatrix}$$
>
> where:
>
> - $\mathbf{q}$ represents generalized coordinates.
> - $\dot{\mathbf{q}}$ represents generalized velocities.

### 3.3 Equations of Motion

> [!important] General Mechanical Formulation
> The dynamics of a mechanical system can often be expressed in generalized coordinates as:
>
> $$\mathbf{M}(\mathbf{q})\ddot{\mathbf{q}}
> + \mathbf{h}(\mathbf{q},\dot{\mathbf{q}})
> = \boldsymbol{\tau}$$
>
> where:
>
> - $\mathbf{M}(\mathbf{q})$ is the generalized mass matrix.
> - $\mathbf{h}(\mathbf{q},\dot{\mathbf{q}})$ represents velocity-dependent, potential, and other modeled internal terms.
> - $\boldsymbol{\tau}$ represents generalized applied forces.
>
> This is a common formulation for finite-dimensional mechanical systems. Constrained, dissipative, and more general mechanical systems may require additional terms.

### 3.4 Constraints

> [!definition] Mechanical Constraints
> Constraints restrict the admissible configurations or motions of a mechanical system.
>
> Holonomic constraints can be represented as:
>
> $$f(\mathbf{q},t)=0$$
>
> More general velocity constraints may be expressed as:
>
> $$\mathbf{A}(\mathbf{q},t)\dot{\mathbf{q}}
> + \mathbf{b}(\mathbf{q},t)=0$$
>
> Constraints influence the system's degrees of freedom and equations of motion.

## 4. Mechanical System Properties

> [!important] Fundamental Properties
> The principal properties used to characterize mechanical systems include:
>
> | Property | Description |
> |---|---|
> | Mass | Measure of translational inertia |
> | Inertia Tensor | Describes rotational inertia distribution |
> | Configuration | Spatial arrangement of system components |
> | Degrees of Freedom | Number of independent configuration variables |
> | Constraints | Restrictions on admissible motion |
> | Generalized Forces | Forces associated with generalized coordinates |
> | Energy | Capacity associated with the system's mechanical state |
> | Momentum | Measure of translational or rotational motion |
> | Equilibrium | State satisfying mechanical balance conditions |
> | Stability | Response to sufficiently small perturbations |

## 5. Mechanical System Modeling

> [!abstract] Modeling Process
> Mechanical system modeling involves constructing a mathematical representation of a physical system.
>
> A typical modeling process consists of:
>
> 1. Identifying the system boundary and physical components.
> 2. Selecting appropriate idealizations.
> 3. Defining reference frames and coordinate systems.
> 4. Identifying generalized coordinates and degrees of freedom.
> 5. Establishing mechanical constraints.
> 6. Identifying masses, inertial properties, and external interactions.
> 7. Formulating the governing equations.
> 8. Specifying initial conditions and boundary conditions where applicable.
>
> The selected model should retain the physical characteristics relevant to the problem while avoiding unnecessary complexity.

## 6. Limitations and Idealizations

> [!warning] Modeling Limitations
> Mechanical systems are frequently represented using idealized assumptions:
>
> - **Point-Mass Approximation:** Neglects body dimensions and rotational effects.
> - **Rigid-Body Approximation:** Neglects elastic deformation.
> - **Continuum Hypothesis:** Treats matter as continuously distributed.
> - **Ideal Constraints:** Assumes prescribed geometric or kinematic relationships.
> - **Ideal Joints:** Neglects clearance, friction, and compliance when appropriate.
>
> These assumptions are modeling choices rather than universal physical properties.

## 7. Knowledge Relationships

### 7.1 Foundation Knowledge

> [!note] Essential Foundations
> - **Classical Mechanics:** Provides the physical principles governing mechanical systems.
> - **Kinematics:** Describes the configurations and motion of mechanical components.
> - **Linear Algebra:** Supports mathematical representations of coordinates and transformations.
> - **Calculus:** Provides the mathematical tools for describing motion and change.
> - **Differential Equations:** Describes the evolution of mechanical states.

> [!note] Relevant Foundations
> - **Euclidean Geometry:** Provides spatial and geometric relationships.
> - **Vector Calculus:** Supports spatial descriptions of mechanical quantities.
> - **Differential Geometry:** Provides a framework for configuration spaces and constrained mechanical systems.

### 7.2 Downstream Knowledge

> [!note] Relevant Developments
> - **Particle Mechanics:** Studies systems modeled using particles.
> - **Rigid Body Mechanics:** Studies the motion and equilibrium of rigid bodies.
> - **Continuum Mechanics:** Studies continuously distributed matter.
> - **Multibody Dynamics:** Studies interconnected mechanical bodies.
> - **Analytical Mechanics:** Develops mathematical formulations of mechanical systems.
> - **Mechanical Vibrations:** Studies oscillatory mechanical behavior.

> [!note] Advanced Developments
> - **Nonlinear Dynamics:** Investigates nonlinear mechanical system evolution.
> - **Constrained Dynamics:** Develops the mathematical treatment of constrained mechanical systems.
> - **Computational Mechanics:** Develops numerical methods for solving mechanical models.
> - **Robotics Dynamics:** Applies mechanical system models to robotic mechanisms.

## 8. References

> [!bibliography]
> 1. John R. Taylor, *Classical Mechanics*, 2005.
> 2. Herbert Goldstein, Charles Poole, and John Safko, *Classical Mechanics*, 3rd edition, 2001.
> 3. Ahmed A. Shabana, *Dynamics of Multibody Systems*, 4th edition, 2013.
> 4. Thomas R. Kane and David A. Levinson, *Dynamics: Theory and Applications*, 1985.

## 9. Further Development

> [!todo] Recommended Independent Notes
> - Particle Mechanics
> - Systems of Particles
> - Rigid Body Systems
> - Deformable Body Systems
> - Multibody Systems
> - Mechanical Constraints
> - Configuration Space
> - State Space