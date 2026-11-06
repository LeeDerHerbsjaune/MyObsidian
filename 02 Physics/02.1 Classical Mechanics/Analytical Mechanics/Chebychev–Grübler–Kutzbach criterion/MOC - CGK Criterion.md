## 5. Knowledge Relationships

### 5.1. Prerequisite concepts

> [!info] Required knowledge
> Understanding the CGK criterion requires familiarity with:
>
> - [[Rigid Body]] — A body whose internal distances remain constant.
> - Degrees of Freedom — The number of independent coordinates required to describe a system configuration.
> - [[Kinematic Pair]] — A connection between two bodies that restricts their relative motion.
> - [[Constraint Equation]] — A mathematical relationship restricting system configurations.
> - Three-Dimensional Euclidean Space — The geometric space in which spatial mechanisms operate.

### 5.2. Related concepts

> [!abstract] Conceptual connections
>
> | Concept | Relationship |
> |---|---|
> | [[Mobility Analysis]] | The primary problem addressed by the criterion. |
> | Robot Kinematics | Uses mobility to characterize robotic mechanisms. |
> | [[Jacobian Matrix]] | Characterizes instantaneous motion and local kinematic rank. |
> | [[Constraint Jacobian]] | Describes the independent and dependent kinematic constraints. |
> | [[Serial Manipulator]] | A common application of mobility analysis. |
> | [[Parallel Manipulator]] | A closed-chain mechanism requiring careful constraint analysis. |

### 5.3. Distinction from Jacobian-based mobility analysis

> [!important] CGK criterion vs. Jacobian rank
>
> The CGK criterion provides a structural estimate of mechanism mobility based on link and joint counts.
>
> Jacobian-based analysis determines local mobility by examining the rank of the constraint Jacobian.
>
> For a system with \(n\) generalized coordinates and constraint vector \(\boldsymbol{\Phi}(\mathbf q)=0\):
>
> $$
> \mathbf J_c(\mathbf q)
> =
> \frac{\partial \boldsymbol{\Phi}}{\partial \mathbf q}
> $$
>
> The local instantaneous mobility is:
>
> $$
> \boxed{M=n-\operatorname{rank}(\mathbf J_c)}
> $$
>
> This formulation accounts for the actual independence of the constraints at a particular configuration.

## 10. Knowledge Links and Further Development

> [!tip] Recommended next notes
>
> To develop a deeper understanding of mechanism mobility, consider creating the following notes:
>
> **Fundamental concepts**
> - [[Rigid Body]]
> - [[Kinematic Pair]]
> - [[Constraint Equation]]
>
> **Mathematical foundations**
> - [[Configuration Space]]
> - [[Constraint Jacobian]]
> - [[Jacobian Matrix]]
> - Matrix Rank
>
> **Advanced robotics**
> - Screw Theory
> - [[Reciprocal Screw]]
> - [[Instantaneous Mobility]]
> - [[Kinematic Singularity]]
> - [[Parallel Manipulator]]
>
> **Suggested learning sequence:**
>
> Rigid Body → Degree of Freedom → Kinematic Pair → CGK Criterion → Constraint Jacobian → Screw Theory → Parallel Robot Mobility Analysis.