

>[!quote] Introduction 
>> - The essence of DoF is the number of independent dimensions of motion or the minimum number of independent variables required to describe a system's configuration. 
>> - The main application of DoF is to quantify the complexity and motion capabilities of mechanical systems, as well as the degrees of freedom of data in computational models.
>

>[!note] Link MOC
> 1. Foundations

>1. DoF - Core Concept
>2. DoF - Advanced Topics
## 5. Knowledge Relationships — Quan hệ kiến thức

### 5.1 Prerequisites

>[!Foundation]
> - Coordinate System]] — Defines the reference frames used to describe motion.
    >
> - Rigid Body — Establishes the idealized mechanical body model.
    >
> - Generalized coordinates]] — Provides a coordinate representation of a mechanical system.
    >
> - Kinematic Constraint]] — Describes restrictions on admissible configurations or velocities.
   > 
> - Linear Algebra]] — Provides the rank and null-space concepts used in constraint analysis.    
> - 📐Independent Coordinates]]
> - 📐Configuration Space (C-space)]]
> -  Chebychev–Grübler–Kutzbach criterion]]
### 5.2 Parent concepts

- Mechanics
    
- Robot Kinematics
    
- Mechanism Theory
    

### 5.3 Closely related concepts

| Term                      | Relationship to DoF                                                                                               |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| [[Joint]]                 | Defines relative motion permitted between connected bodies.                                                       |
| [[Mobility]]              | Often synonymous with DoF in mechanism theory.                                                                    |
| [[Kinematic Constraint]]  | Restricts admissible configurations or motions.                                                                   |
| Jacobian Matrix           | Maps joint velocities to task-space velocities; rank reveals local motion capability.                             |
| Inverse Kinematics        | Finds configurations that achieve a desired end-effector pose.                                                    |
| [[Workspace]]             | Describes the set of positions or poses reachable by a robot.                                                     |
| Kinematic Singularity]]   | A configuration where the kinematic mapping loses rank and instantaneous motion capability changes.               |
| [[Actuation]]             | Determines which mechanical coordinates or combinations of coordinates can be controlled.                         |
| [[Redundant Manipulator]] | Has more independent configuration DoF than are required for a specified task, under the chosen task-space model. |


### 5.4 Commonly confused concepts

**DoF vs. number of joints**

A serial robot with six independent one-DoF joints typically has six configuration DoF. A closed-chain mechanism may have many joints but fewer overall DoF because of loop-closure constraints.

**DoF vs. number of actuators**

A mechanism can have unactuated DoF, passive joints, or coupled actuation. DoF and actuator count are not generally equal.

**Configuration DoF vs. task-space dimension**

A planar end-effector pose has three coordinates, but a particular robot may have fewer, equal, or more configuration DoF.

**Configuration DoF vs. state dimension**

A mechanical state commonly includes both configuration and velocity. For an unconstrained system with (n) configuration DoF, a local state representation often uses (2n) scalar coordinates, such as ((q,\dot q)). This does not mean the mechanism has (2n) configuration DoF.

**DoF vs. number of coordinates**

A model may use redundant coordinates, such as a rotation matrix with nine entries, to represent a configuration with only three rotational DoF. Constraints on the representation must be accounted for.


## 10. Knowledge Links & Further Development — Liên kết và mở rộng

### 10.1 Recommended learning path

```
flowchart TD
    A["Coordinate Systems"] --> B["Generalized Coordinates"]
    B --> C["Degrees of Freedom"]
    C --> D["Configuration Space"]
    C --> E["Kinematic Constraints"]
    E --> F["Constraint Jacobian"]
    D --> G["Forward Kinematics"]
    G --> H["Inverse Kinematics"]
    F --> I["Mechanism Mobility"]
    H --> J["Kinematic Singularity"]
    I --> J
```

### 10.2 Suggested next notes

2. [[Generalized coordinates]] — Learn how to parameterize mechanical systems.
    
3. [[Joint]] — Study revolute, prismatic, spherical, and other joint types.
    
4. [[Chebychev–Grübler–Kutzbach criterion]] — Estimate the mobility of mechanisms.
    
5. Jacobian Matrix — Analyze the mapping between joint and end-effector velocities.
    
6. Kinematic Singularity — Understand loss of instantaneous motion capability.
    
7. Holonomic Constraint — Model geometric restrictions on configurations.
    
8. Nonholonomic Constraint — Understand rolling constraints and mobile robot motion.
    
9. [[Actuation]] — Distinguish mechanical mobility from controllable inputs.
    
10. [[Swarm Robotics]] — Extend configuration-space reasoning to collective robot systems.
    

### 10.3 Actionable learning tasks

- Derive the DoF of a planar four-bar linkage using a mobility criterion.
    
- Implement a constraint-Jacobian rank check in Python.
    
- Compare configuration-space dimension and control-input dimension for a differential-drive robot.
    
- Analyze how adding a formation constraint affects the configuration space of a multi-robot system.
    
- Investigate how singularities alter the instantaneous motion capabilities of a manipulator.
    

**Knowledge graph position:** This is the canonical note for mechanical and robotic degrees of freedom. Use aliases for spelling variants such as `DOF`; create separate notes for statistical degrees of freedom or other discipline-specific meanings when needed.