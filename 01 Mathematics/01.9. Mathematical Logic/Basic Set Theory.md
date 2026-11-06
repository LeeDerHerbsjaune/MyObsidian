---
related:
  - "[[Set Operations]]"
  - "[[Set Constructions]]"
---
> [!abstract] Overview  
> **Basic Set Theory** is a fundamental branch of mathematics that provides the language and notation for describing, classifying, comparing, and manipulating collections of objects.
> 
> **Applications:**
> 
> - Linear Algebra
>     
> - Probability Theory
>     
> - Discrete Mathematics
>     
> - Control Theory
>     
> - Computer Science
>     

---

## 1. Fundamental Concepts

### 1.1. Set

> [!info] Definition  
> A **set** is a well-defined collection of distinct objects, called elements or members of the set.

**Mathematical notation:**

$$A={1,2,3,4,5}$$

**Examples:**

- The set of natural numbers.
    
- The set of solutions to an equation.
    
- The set of possible states of a dynamical system.
    

### 1.2. Element of a Set

> [!info] Definition  
> An **element** is an individual object that belongs to a particular set.

**Example:**

$$A={1,2,3,4}$$

$$1\in A$$

Here, 1 is an element of set A.

### 1.3. Set Membership

> [!info] Definition  
> **Set Membership** describes the relationship between an object and a set, indicating whether the object belongs to that set.

**Mathematical notation:**

|Symbol|Meaning|
|---|---|
|$\in$|Belongs to|
|$\notin$|Does not belong to|

**Example:**

$$A={2,4,6,8}$$

$$4\in A,\qquad 5\notin A$$

> [!warning] Important distinction  
> Set Membership is different from Subset:
> 
> - $x\in A$: x is an element of A.
>     
> - $B\subseteq A$: B is a subset of A.
>     

### 1.4. Empty Set

> [!info] Definition  
> An **empty set** is a set that contains no elements.

**Notation:**

$$\emptyset \quad \text{or} \quad {}$$

**Example:**

$$A={x\in\mathbb{R}\mid x^2+1=0}$$

$$A=\emptyset$$

> [!success] Important property  
> The empty set is a subset of every set:

$$\emptyset\subseteq A$$

### 1.5. Singleton Set

> [!info] Definition  
> A **singleton set** is a set that contains exactly one element.

**Example:**

$$A={5}$$

$$|A|=1$$

Here, $|A|$ represents the cardinality (number of elements) of A.

> [!warning] Important distinction  
> $${5}\neq 5$$
> 
> ${5}$ is a set containing the element 5, whereas 5 is the number itself.

### 1.6. Subset

> [!info] Definition  
> A set A is called a **subset** of set B if every element of A is also an element of B.

**Notation:**

$$A\subseteq B$$

**Example:**

$$A={1,2}$$

$$B={1,2,3,4}$$

$$A\subseteq B$$

> [!success] Important property  
> Every set is a subset of itself:

$$A\subseteq A$$

### 1.7. Proper Subset

> [!info] Definition  
> A set A is called a **proper subset** of set B if every element of A belongs to B, but A is not equal to B.

**Notation:**

$$A\subsetneq B$$

**Example:**

$$A={1,2},\qquad B={1,2,3}$$

$$A\subsetneq B$$

> [!warning] Important distinction
> 
> |Subset|Proper Subset|
> |---|---|
> |$A\subseteq B$|$A\subsetneq B$|
> |Allows $A=B$|Requires $A\neq B$|

### 1.8. Universal Set

> [!info] Definition  
> A **universal set** is the set containing all elements under consideration within a particular context or mathematical problem.

**Notation:**

$$U$$

**Example:**

$$U={1,2,3,4,5,6}$$

$$A={2,4,6}$$

$$A\subseteq U$$

> [!note] Application  
> The universal set defines the scope of elements being considered, particularly when performing set operations such as complementation.

### 1.9. Power Set

> [!info] Definition  
> The **power set** of a set A is the set of all possible subsets of A, including the empty set and A itself.

**Notation:**

$$\mathcal{P}(A)$$

**Example:**

$$A={1,2}$$

$$\mathcal{P}(A)={\emptyset,{1},{2},{1,2}}$$

> [!important] Important formula  
> If a set contains n elements, the number of its subsets is:

$$|\mathcal{P}(A)|=2^n$$

**Example:**

If $|A|=3$, then:

$$|\mathcal{P}(A)|=2^3=8$$

### 1.10. Set Equality

> [!info] Definition  
> Two sets are **equal** if they contain exactly the same elements.

**Notation:**

$$A=B$$

**Equivalent condition:**

$$A\subseteq B\quad\text{and}\quad B\subseteq A$$

**Example:**

$$A={1,2,3}$$

$$B={3,2,1}$$

$$A=B$$

> [!warning] Important properties
> 
> - The order of elements does not affect set equality.
>     
> - Duplicate elements are not counted multiple times.
>     

---

## 2. Mathematical Notation

|Terminology|Symbol|Description|
|---|---|---|
|Set|$A$|A collection of elements|
|Element|$x$|An individual object|
|Membership|$\in$|Belongs to a set|
|Non-membership|$\notin$|Does not belong to a set|
|Empty Set|$\emptyset$|A set with no elements|
|Singleton Set|${a}$|A set with exactly one element|
|Subset|$\subseteq$|A set contained in another set|
|Proper Subset|$\subsetneq$|A subset that is not equal to the original set|
|Universal Set|$U$|The set of all elements under consideration|
|Power Set|$\mathcal{P}(A)$|The set of all subsets of A|
|Set Equality|$A=B$|Two sets containing identical elements|
|Cardinality|$|A|$|The number of elements in a set|

---
## 4. Visualization and Simulation

> [!abstract] Recommended visualization methods  
> Visualization methods help transform abstract set-theoretic concepts into graphical representations.

### 4.1. Venn Diagram

**Purpose:** Graphically represents relationships between sets.

**Applications:**

- Union
    
- Intersection
    
- Difference
    
- Complement
    
- Subset relationships
    

### 4.2. Hasse Diagram / Subset Lattice

**Purpose:** Represents the hierarchical structure of subsets within a power set.

**Applications:**

- Power Set
    
- Subset relationships
    
- Partially Ordered Sets
    

### 4.3. Cartesian Product Visualization

**Purpose:** Represents ordered pairs formed from two sets, commonly using coordinate systems.

**Applications:**

- Ordered Pairs
    
- Relations
    
- Coordinate Systems
    
- State-space representation
    

---

## 5. Engineering Applications

> [!abstract] Connection to Control Theory  
> Set Theory plays an important role in control system modeling, particularly in representing state spaces, control input domains, system constraints, and safety regions.

### 5.1. State Space

The state space represents the set of all possible states of a system.

$$X=\mathbb{R}^n$$

Where:

- $X$: State space.
    
- $n$: Dimension of the state vector.
    

### 5.2. Control Input Set

The control input set describes the feasible control inputs available to a system.

$$U={u\in\mathbb{R}^m\mid u_{\min}\leq u\leq u_{\max}}$$

Where:

- $U$: Feasible control input set.
    
- $u$: Control input vector.
    
- $m$: Dimension of the input vector.
    
- $u_{\min},u_{\max}$: Lower and upper input bounds.
    

### 5.3. State Constraints

State constraints define the allowable region within the state space.

$$X_{\text{safe}}\subseteq X$$

Where:

- $X_{\text{safe}}$: Safe state set.
    
- $X$: Overall state space.
    

> [!tip] Related advanced topics
> 
> - Reachability Analysis
>     
> - Viability Theory
>     
> - Set Invariance
>     
> - Constraint Satisfaction
>     
> - Model Predictive Control (MPC)
>     

---

## 6. Research Perspectives

> [!question] Research arguments and perspectives

### 6.1. Set Representation and Computational Complexity

The choice of set representation affects computational efficiency and memory requirements, particularly when dealing with large or infinite sets.

**Research directions:**

- Computational Complexity
    
- Efficient Set Representation
    
- Symbolic Representation
    
- Computational Geometry
    

### 6.2. Set-based Modeling in Control Systems

Instead of representing a single state or control input, set-based modeling uses collections of possible values to describe system uncertainty and constraints.

**Research directions:**

- Set-based Control
    
- Uncertainty Modeling
    
- Robust Control
    
- Constraint Representation
    

### 6.3. Reachability and Safety Verification

Reachability analysis determines the set of states that a system can potentially reach, while safety verification checks whether these states intersect with unsafe regions.

**Research directions:**

- Reachability Analysis
    
- Safety Verification
    
- Reachable Set Computation
    
- Formal Methods
    

### 6.4. Set Invariance

Set invariance investigates the conditions under which a set of states remains within a specified region over time under system dynamics and control actions.

**Research directions:**

- Controlled Invariant Sets
    
- Positive Invariant Sets
    
- Control Invariant Regions
    
- Safety-critical Control
    

---

## 7. Learning Roadmap

> [!todo] Recommended learning sequence
> 
> - Basic Set Theory
>     
> - Set Representation
>     
> - Set Operations
>     
> - Set Properties
>     
> - Cardinality and Counting
>     
> - Cartesian Product and Relations
>     
> - Applications in Control Theory
>     

---

## 8. Summary

> [!summary] Key Takeaways
> 
> 1. Set Theory provides a mathematical foundation for describing collections of objects.
>     
> 2. Set Membership and Subset are two distinct concepts that must be understood separately.
>     
> 3. A Power Set represents all possible subsets of a given set.
>     
> 4. Cardinality determines the number of elements in a set.
>     
> 5. Set Operations provide the foundation for manipulating and comparing sets.
>     
> 6. In Control Theory, Set Theory is essential for modeling state spaces, constraints, uncertainty, and system safety.
>     

> [!quote] Core Idea  
> Set Theory is the mathematical language for describing collections, relationships, constraints, and mathematical structures.