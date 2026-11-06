---
related:
  - "[[Set Structure]]"
---


> [!abstract] Overview  
> **Set Operations** studies the mathematical operations used to construct new sets from existing sets. These operations define relationships between sets and provide fundamental tools for manipulating, comparing, and analyzing collections of elements.
> 
> **Applications:**
> 
> - Discrete Mathematics
>     
> - Mathematical Logic
>     
> - Probability Theory
>     
> - Database Systems
>     
> - Computer Science
>     
> - Control Theory
>     

---

## 1. Fundamental Concepts

### 1.1. Union

> [!info] Definition  
> The **Union** of two sets A and B is the set containing all elements that belong to A, B, or both.

**Mathematical notation:**

$$A\cup B={x\mid x\in A\lor x\in B}$$

**Example:**

$$A={1,2,3}$$

$$B={3,4,5}$$

$$A\cup B={1,2,3,4,5}$$

> [!note] Important properties
> 
> - Elements appearing in both sets are included only once.
>     
> - Union is commutative.
>     
> - Union is associative.
>     
> - Union with the empty set leaves the original set unchanged.
>     

**Properties:**

$$A\cup B=B\cup A$$

$$A\cup(B\cup C)=(A\cup B)\cup C$$

$$A\cup\emptyset=A$$

### 1.2. Intersection

> [!info] Definition  
> The **Intersection** of two sets A and B is the set containing all elements that belong to both A and B.

**Mathematical notation:**

$$A\cap B={x\mid x\in A\land x\in B}$$

**Example:**

$$A={1,2,3}$$

$$B={3,4,5}$$

$$A\cap B={3}$$

> [!note] Important properties
> 
> - Only common elements are included.
>     
> - Intersection is commutative.
>     
> - Intersection is associative.
>     
> - Intersection with the empty set produces the empty set.
>     

**Properties:**

$$A\cap B=B\cap A$$

$$A\cap(B\cap C)=(A\cap B)\cap C$$

$$A\cap\emptyset=\emptyset$$

### 1.3. Set Difference

> [!info] Definition  
> The **Set Difference** between A and B is the set containing elements that belong to A but do not belong to B.

**Mathematical notation:**

$$A\setminus B={x\mid x\in A\land x\notin B}$$

**Example:**

$$A={1,2,3,4}$$

$$B={3,4,5,6}$$

$$A\setminus B={1,2}$$

$$B\setminus A={5,6}$$

> [!warning] Important distinction  
> Set Difference is generally not commutative:

$$A\setminus B\neq B\setminus A$$

**Important properties:**

$$A\setminus\emptyset=A$$

$$A\setminus A=\emptyset$$

$$\emptyset\setminus A=\emptyset$$

$$A\setminus B=A\cap B^c$$

### 1.4. Complement of a Set

> [!info] Definition  
> The **Complement** of a set A is the set containing all elements of the universal set U that do not belong to A.

**Mathematical notation:**

$$A^c=U\setminus A$$

Alternatively:

$$A^c={x\in U\mid x\notin A}$$

**Example:**

$$U={1,2,3,4,5,6}$$

$$A={1,2,3}$$

$$A^c={4,5,6}$$

> [!important] Important properties  
> The complement depends on the universal set U.

**Complement Laws:**

$$A\cup A^c=U$$

$$A\cap A^c=\emptyset$$

$$(A^c)^c=A$$

$$U^c=\emptyset$$

$$\emptyset^c=U$$

### 1.5. Symmetric Difference

> [!info] Definition  
> The **Symmetric Difference** of two sets A and B is the set containing elements that belong to exactly one of the two sets, but not both.

**Mathematical notation:**

$$A\triangle B=(A\setminus B)\cup(B\setminus A)$$

Alternatively:

$$A\triangle B=(A\cup B)\setminus(A\cap B)$$

**Example:**

$$A={1,2,3,4}$$

$$B={3,4,5,6}$$

$$A\triangle B={1,2,5,6}$$

> [!note] Important properties  
> Symmetric Difference is commutative and associative.

**Properties:**

$$A\triangle B=B\triangle A$$

$$A\triangle(B\triangle C)=(A\triangle B)\triangle C$$

$$A\triangle\emptyset=A$$

$$A\triangle A=\emptyset$$

### 1.6. Disjoint Sets

> [!info] Definition  
> Two sets are called **Disjoint Sets** if they have no elements in common. Their intersection is the empty set.

**Mathematical notation:**

$$A\cap B=\emptyset$$

**Example:**

$$A={1,2,3}$$

$$B={4,5,6}$$

$$A\cap B=\emptyset$$

Therefore, A and B are disjoint sets.

> [!warning] Important distinction  
> Disjoint sets have no common elements, whereas overlapping sets share at least one element.

**Application:**

- Partitioning data into separate categories.
    
- Defining mutually exclusive events in probability theory.
    
- Dividing a system into non-overlapping regions.
    

### 1.7. De Morgan's Laws

> [!info] Definition  
> **De Morgan's Laws** describe the relationship between set complements and the operations of union and intersection. They provide a method for transforming expressions involving complements.

**First Law – Complement of a Union:**

$$  
(A\cup B)^c=A^c\cap B^c  
$$

The complement of a union equals the intersection of the individual complements.

**Second Law – Complement of an Intersection:**

$$  
(A\cap B)^c=A^c\cup B^c  
$$

The complement of an intersection equals the union of the individual complements.

> [!important] Generalized De Morgan's Laws  
> These laws can be extended to any finite collection of sets.

\bigcap_{i=1}^{n}A_i^c  
$$

\bigcup_{i=1}^{n}A_i^c  
$$

**Applications:**

- Mathematical proof and simplification.
    
- Boolean algebra.
    
- Digital logic circuit design.
    
- Logical condition transformation.
    
- Database query optimization.
    

### 1.8. Set Identities

> [!info] Definition  
> **Set Identities** are mathematical equations that hold for all sets under the same universal set. They describe fundamental relationships between set operations and can be used to simplify set expressions.

#### 1.8.1. Identity Laws

$$A\cup\emptyset=A$$

$$A\cap U=A$$

#### 1.8.2. Domination Laws

$$A\cup U=U$$

$$A\cap\emptyset=\emptyset$$

#### 1.8.3. Idempotent Laws

$$A\cup A=A$$

$$A\cap A=A$$

#### 1.8.4. Complement Laws

$$A\cup A^c=U$$

$$A\cap A^c=\emptyset$$

#### 1.8.5. Double Complement Law

$$  
(A^c)^c=A  
$$

#### 1.8.6. Commutative Laws

$$A\cup B=B\cup A$$

$$A\cap B=B\cap A$$

#### 1.8.7. Associative Laws

$$A\cup(B\cup C)=(A\cup B)\cup C$$

$$A\cap(B\cap C)=(A\cap B)\cap C$$

#### 1.8.8. Distributive Laws

$$

(A\cap B)\cup(A\cap C)  
$$

#### 1.8.9. Absorption Laws

$$A\cup(A\cap B)=A$$

$$A\cap(A\cup B)=A$$

#### 1.8.10. De Morgan's Laws

$$  
(A\cup B)^c=A^c\cap B^c  
$$

$$  
(A\cap B)^c=A^c\cup B^c  
$$

> [!tip] Important observation  
> Set Identities have a close mathematical relationship with Boolean Algebra. Union corresponds to logical OR, intersection corresponds to logical AND, and complement corresponds to logical NOT.

---

## 2. Mathematical Notation

|Terminology|Symbol|Description|
|---|---|---|
|Union|$A\cup B$|Elements in A or B|
|Intersection|$A\cap B$|Elements common to A and B|
|Set Difference|$A\setminus B$|Elements in A but not B|
|Complement|$A^c$|Elements outside A within U|
|Symmetric Difference|$A\triangle B$|Elements in exactly one of A or B|
|Disjoint Sets|$A\cap B=\emptyset$|Sets with no common elements|
|Universal Set|$U$|All elements under consideration|
|Empty Set|$\emptyset$|A set containing no elements|

---

## 3. Visualization and Simulation

> [!abstract] Recommended visualization methods  
> Visual representations help explain how set operations transform existing sets into new sets.

### 3.1. Venn Diagrams

**Purpose:** Represent set operations using overlapping regions.

**Applications:**

- Union: Shade all regions belonging to either set.
    
- Intersection: Shade only the overlapping region.
    
- Difference: Shade the region belonging to A but not B.
    
- Complement: Shade the region outside A but within U.
    
- Symmetric Difference: Shade the non-overlapping regions of A and B.
    

### 3.2. Set Operation Tables

**Purpose:** Represent the membership of individual elements before and after set operations.

**Example:**

Let:

$$A={1,2,3}$$

$$B={3,4,5}$$

|Element|In A|In B|In A ∪ B|In A ∩ B|
|---|---|---|---|---|
|1|True|False|True|False|
|2|True|False|True|False|
|3|True|True|True|True|
|4|False|True|True|False|
|5|False|True|True|False|

### 3.3. Boolean Representation

**Purpose:** Represent set membership using binary values.

- 1: Element belongs to the set.
    
- 0: Element does not belong to the set.
    

|Operation|Boolean Equivalent|
|---|---|
|Union|OR|
|Intersection|AND|
|Complement|NOT|
|Symmetric Difference|XOR|

> [!example] Example  
> If an element has membership values:
> 
> $$A=1,\qquad B=0$$
> 
> Then:
> 
> $$A\lor B=1$$
> 
> $$A\land B=0$$
> 
> $$A\oplus B=1$$

---

## 4. Engineering Applications

> [!abstract] Connection to Engineering and Control Theory  
> Set Operations are useful in engineering when combining, separating, and analyzing regions of possible system states, constraints, and operating conditions.

### 4.1. Constraint Intersection

Multiple constraints can be represented as individual sets. The feasible region is obtained by intersecting these sets.

$$X_{\text{feasible}}=X_1\cap X_2\cap\cdots\cap X_n$$

**Application:**

- Feasible state determination.
    
- Constraint satisfaction.
    
- Optimization problems.
    
- Motion planning.
    

### 4.2. Reachable Set Union

If a system can reach different regions under different conditions, the overall reachable region can be represented by their union.

$$R=R_1\cup R_2\cup\cdots\cup R_n$$

**Application:**

- Reachability analysis.
    
- Hybrid systems.
    
- Multiple operating modes.
    
- Safety verification.
    

### 4.3. Safe Set Complement

The unsafe region can be defined as the complement of the safe region within the overall state space.

$$X_{\text{unsafe}}=X\setminus X_{\text{safe}}$$

**Application:**

- Collision avoidance.
    
- Safety verification.
    
- Autonomous systems.
    
- Safety-critical control.
    

### 4.4. Feasible Region Difference

Removing prohibited operating regions from an admissible region can be represented using set difference.

$$X_{\text{allowed}}=X_{\text{admissible}}\setminus X_{\text{forbidden}}$$

**Application:**

- Obstacle avoidance.
    
- Workspace planning.
    
- Robot motion planning.
    
- Operational constraints.
    

### 4.5. Disjoint Operating Regions

Different operating modes can be modeled as disjoint sets when they are mutually exclusive.

$$X_i\cap X_j=\emptyset,\qquad i\neq j$$

**Application:**

- Hybrid control systems.
    
- Mode switching.
    
- System partitioning.
    
- Operating region classification.
    

---

## 5. Research Perspectives

> [!question] Research arguments and perspectives

### 5.1. Set-based Constraint Modeling

Set operations provide a mathematical framework for combining multiple constraints into a single feasible region.

**Research directions:**

- Feasible Set Computation.
    
- Constraint Aggregation.
    
- Set-based Optimization.
    
- Nonlinear Constraint Representation.
    

### 5.2. Reachability Analysis and Set Operations

Reachability analysis frequently requires the union and intersection of sets to determine possible system states and verify system behavior.

**Research directions:**

- Reachable Set Approximation.
    
- Set Propagation.
    
- Forward Reachability.
    
- Backward Reachability.
    
- Safety Verification.
    

### 5.3. Set-based Safety Verification

Safe and unsafe regions can be represented through complements, intersections, and differences to evaluate whether system trajectories violate safety constraints.

**Research directions:**

- Safe Set Construction.
    
- Unsafe Region Identification.
    
- Collision Detection.
    
- Invariant Set Computation.
    

### 5.4. Computational Efficiency of Set Operations

The computational cost of set operations becomes important when dealing with high-dimensional or complex sets.

**Research directions:**

- Efficient Set Representation.
    
- Computational Geometry.
    
- Interval Arithmetic.
    
- Polyhedral Computation.
    
- Zonotope Operations.
    

### 5.5. Set Operations in Boolean Algebra

The algebraic properties of set operations are closely related to Boolean logic and provide a foundation for digital systems and logical reasoning.

**Research directions:**

- Boolean Algebra.
    
- Logic Circuit Optimization.
    
- Formal Verification.
    
- Symbolic Computation.
    

---

## 6. Learning Roadmap

> [!todo] Recommended learning sequence
> 
> - Understand Union and Intersection.
>     
> - Understand Set Difference and Complement.
>     
> - Study Symmetric Difference.
>     
> - Understand Disjoint Sets.
>     
> - Derive and apply De Morgan's Laws.
>     
> - Memorize and prove Set Identities.
>     
> - Practice Venn Diagram transformations.
>     
> - Apply Set Operations to constraint modeling.
>     
> - Explore Set Operations in Control Theory.
>     

---

## 7. Summary

> [!summary] Key Takeaways
> 
> 1. Union combines elements belonging to either of two sets.
>     
> 2. Intersection identifies elements common to two or more sets.
>     
> 3. Set Difference removes elements belonging to another set.
>     
> 4. Complement identifies elements outside a given set within the universal set.
>     
> 5. Symmetric Difference identifies elements belonging to exactly one of two sets.
>     
> 6. Disjoint Sets have no common elements.
>     
> 7. De Morgan's Laws describe the relationship between complements, unions, and intersections.
>     
> 8. Set Identities provide algebraic rules for simplifying set expressions.
>     
> 9. Set Operations are fundamental to constraint modeling, reachability analysis, and safety verification.
>     

> [!quote] Core Idea  
> Set Operations provide the mathematical tools for combining, comparing, separating, and transforming collections of elements into new sets.