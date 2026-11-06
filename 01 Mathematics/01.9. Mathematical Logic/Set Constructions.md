---
related:
  - "[[Set Structure]]"
---


> [!abstract] Overview  
> Set constructions are mathematical methods used to build new sets from existing sets, organize collections of sets, and describe relationships between elements. They provide a foundation for discrete mathematics, algebra, topology, probability, and mathematical modeling.

## 1. Cartesian Product

> [!info] Definition  
> The **Cartesian Product** of two sets is the set of all ordered pairs formed by selecting one element from each set.
> 
> For two sets A and B:
> 
> $$A\times B={(a,b)\mid a\in A,\ b\in B}$$
> 
> The order of elements matters:
> 
> $$(a,b)\neq(b,a)$$
> 
> in general.

**Example**

Let:

$$A={1,2},\qquad B={x,y}$$

Then:

$$A\times B={(1,x),(1,y),(2,x),(2,y)}$$

If both sets are finite:

$$|A\times B|=|A|\cdot|B|$$

For multiple sets, the Cartesian product is:

$$A_1\times A_2\times\cdots\times A_n$$

Its elements are ordered n-tuples.

**Important Properties**

- A × B is generally not equal to B × A.
    
- A × (B × C) and (A × B) × C are not strictly equal as sets of differently nested tuples, but they are naturally equivalent through a bijection.
    
- If either A or B is empty, then:
    
    $$A\times B=\emptyset$$
    
- The empty-set property is:
    
    $$A\times\emptyset=\emptyset\times A=\emptyset$$
    

> [!example] Engineering Example  
> Consider a robot configuration described by position and orientation:
> 
> $$q=(x,y,\theta)$$
> 
> If the position space is P and the orientation space is Θ, the configuration space can be represented as:
> 
> $$Q=P\times\Theta$$
> 
> This construction is useful for describing the complete configuration space of robotic systems.

## 2. Indexed Families of Sets

> [!info] Definition  
> An **Indexed Family of Sets** is a collection of sets whose members are identified by indices from an index set.
> 
> Let I be an index set. An indexed family is written as:
> 
> $${A_i}_{i\in I}$$
> 
> where every Aᵢ is a set associated with an index i.

**Example**

Let:

$$I={1,2,3}$$

and:

$$A_1={1,2},\quad A_2={2,3},\quad A_3={3,4}$$

The indexed family is:

$${A_1,A_2,A_3}$$

**Generalized Set Operations**

The union of an indexed family is:

$$\bigcup_{i\in I}A_i={x\mid \exists i\in I,\ x\in A_i}$$

The intersection is:

$$\bigcap_{i\in I}A_i={x\mid \forall i\in I,\ x\in A_i}$$

For the example:

$$\bigcup_{i=1}^{3}A_i={1,2,3,4}$$

$$\bigcap_{i=1}^{3}A_i=\emptyset$$

**Important Distinctions**

- An ordinary collection of sets does not necessarily preserve the identity of each set through an index.
    
- An indexed family explicitly associates each set with an index.
    
- Different indices may correspond to identical sets.
    
- The index set may be finite, countably infinite, or uncountable.
    

> [!example] Engineering Example  
> In control systems, a family of feasible state sets can represent operating constraints under different conditions:
> 
> $${X_i}_{i\in I}$$
> 
> Each Xᵢ may describe admissible states under a particular operating mode, time interval, or environmental condition.

## 3. Disjoint Union

> [!info] Definition  
> A **Disjoint Union** combines multiple sets while preserving the identity of the set from which each element originates.
> 
> For two sets A and B, their tagged disjoint union is:
> 
> $$A\sqcup B=(A\times{0})\cup(B\times{1})$$
> 
> The tags 0 and 1 distinguish the origins of elements, even when the original sets contain identical elements.

**Example**

Let:

$$A={1,2},\qquad B={2,3}$$

Then:

$$A\sqcup B={(1,0),(2,0),(2,1),(3,1)}$$

The two occurrences of 2 remain distinct because they originate from different sets.

**Important Properties**

- The tagged components are pairwise disjoint.
    
- The original sets do not need to be disjoint.
    
- For finite sets:
    
    $$|A\sqcup B|=|A|+|B|$$
    
- For a family of sets:
    
    $$\bigsqcup_{i\in I}A_i=\bigcup_{i\in I}(A_i\times{i})$$
    

> [!example] Engineering Example  
> A hybrid system may have several operating modes:
> 
> - Mode 1: Standing
>     
> - Mode 2: Walking
>     
> - Mode 3: Running
>     
> 
> Each mode has its own state space. A disjoint union can combine these state spaces while preserving the mode identity:
> 
> $$X=\bigsqcup_{i\in M}X_i$$
> 
> This is useful when the same numerical state variables have different meanings or dynamics in different modes.

## 4. Quotient Set

> [!info] Definition  
> A **Quotient Set** is constructed by grouping elements of a set into equivalence classes according to an equivalence relation.
> 
> Let A be a set and let ~ be an equivalence relation on A. The quotient set is:
> 
> $$A/{\sim}={[a]\mid a\in A}$$
> 
> where [a] denotes the equivalence class containing a.

An equivalence relation must satisfy three properties:

**1. Reflexivity**

$$a\sim a$$

**2. Symmetry**

$$a\sim b\Rightarrow b\sim a$$

**3. Transitivity**

$$a\sim b\land b\sim c\Rightarrow a\sim c$$

**Example: Congruence Modulo 3**

Let A = ℤ, the set of integers, and define:

$$a\sim b\iff a-b\in 3\mathbb{Z}$$

The equivalence classes are:

$$[0]={\ldots,-6,-3,0,3,6,\ldots}$$

$$[1]={\ldots,-5,-2,1,4,7,\ldots}$$

$$[2]={\ldots,-4,-1,2,5,8,\ldots}$$

Therefore:

$$\mathbb{Z}/{\sim}={[0],[1],[2]}$$

**Important Properties**

- Every element belongs to exactly one equivalence class.
    
- Two equivalence classes are either identical or disjoint.
    
- The quotient set contains equivalence classes, not the original individual elements.
    
- The quotient set represents the original set after treating equivalent elements as indistinguishable.
    

> [!warning] Important Distinction  
> A quotient set is not simply a set difference or a subset of the original set. Its elements are equivalence classes, which are themselves subsets of the original set.

> [!example] Engineering Example  
> In robotics, different configurations may represent the same physical orientation. For example, angles differing by a full rotation are equivalent:
> 
> $$\theta_1\sim\theta_2\iff\theta_1-\theta_2=2k\pi,\quad k\in\mathbb{Z}$$
> 
> The quotient construction identifies these equivalent angle representations, allowing orientation to be modeled without treating 0 and 2π as physically different.

## 5. Equivalence Classes

> [!info] Definition  
> An **Equivalence Class** is the subset of a set containing all elements that are equivalent to a particular element under a given equivalence relation.
> 
> For a ∈ A:
> 
> $$[a]={x\in A\mid x\sim a}$$

**Example**

Consider the integers with the equivalence relation:

$$a\sim b\iff a-b\in 3\mathbb{Z}$$

The equivalence class of 1 is:

$$[1]={\ldots,-5,-2,1,4,7,\ldots}$$

The equivalence class of 4 is the same:

$$[4]=[1]$$

because:

$$1\sim4$$

**Important Properties**

- Every element belongs to its own equivalence class.
    
- If two elements are equivalent, their equivalence classes are identical:
    
    $$a\sim b\Rightarrow[a]=[b]$$
    
- If two elements are not equivalent, their equivalence classes are disjoint:
    
    $$a\not\sim b\Rightarrow[a]\cap[b]=\emptyset$$
    
- Every equivalence class is nonempty.
    
- The collection of all equivalence classes forms a partition of the original set.
    

**Representative Element**

An element selected from an equivalence class is called a representative.

For example, the integers 1, 4, and 7 are all representatives of the same equivalence class modulo 3.

> [!warning] Important Distinction  
> An equivalence class is one group of equivalent elements, whereas a quotient set is the collection of all equivalence classes.

## 6. Partitions of Sets

> [!info] Definition  
> A **Partition of a Set** is a collection of nonempty subsets that divides the original set into mutually disjoint groups, such that every element belongs to exactly one group.
> 
> Let A be a nonempty set. A collection:
> 
> $$\mathcal{P}={A_i}_{i\in I}$$
> 
> is a partition of A if it satisfies three conditions.

**Condition 1: Nonempty Blocks**

$$A_i\neq\emptyset,\quad\forall i\in I$$

**Condition 2: Pairwise Disjointness**

$$A_i\cap A_j=\emptyset,\quad i\neq j$$

**Condition 3: Complete Coverage**

$$\bigcup_{i\in I}A_i=A$$

**Example**

Let:

$$A={1,2,3,4,5,6}$$

A valid partition is:

$$\mathcal{P}={{1,3,5},{2,4},{6}}$$

This is a partition because:

- Every block is nonempty.
    
- No element appears in more than one block.
    
- Every element of A is included.
    

**Invalid Partition Examples**

- $${{1,2},{2,3},{4,5,6}}$$ — Invalid because the first two blocks overlap.
    
- $${{1,2},{3,4}}$$ — Invalid because elements 5 and 6 are missing.
    
- $${{1,2},{3,4},\emptyset}$$ — Invalid because an empty block is included.
    

> [!example] Engineering Example  
> In robotics, a state space can be divided into regions according to operating conditions:
> 
> - Stable region
>     
> - Unstable region
>     
> - Collision region
>     
> - Boundary region
>     
> 
> If these regions are defined to be nonempty, mutually disjoint, and collectively cover the entire state space, they form a partition.
> 
> This is useful for state classification, hybrid control, motion planning, and safety analysis.

## 7. Relationship Between Equivalence Relations, Equivalence Classes, Quotient Sets, and Partitions

These four concepts are closely connected.

> [!important] Fundamental Theorem  
> Every equivalence relation on a set induces a unique partition of that set into equivalence classes.
> 
> Conversely, every partition of a set defines an equivalence relation in which two elements are equivalent if and only if they belong to the same block.

The relationship can be represented as:

$$\text{Equivalence Relation}\longleftrightarrow\text{Partition}$$

$$\text{Partition}=\text{Collection of Equivalence Classes}$$

$$\text{Quotient Set}=\text{Set of All Equivalence Classes}$$

**Conceptual Example**

Let:

$$A={1,2,3,4,5,6}$$

Define two elements as equivalent if they have the same parity.

The equivalence classes are:

$$[0]={2,4,6}$$

$$[1]={1,3,5}$$

The corresponding partition is:

$$\mathcal{P}={{2,4,6},{1,3,5}}$$

The quotient set is:

$$A/{\sim}={[0],[1]}$$

The original six elements are represented by only two equivalence classes.

## 8. Mathematical Notation Summary

|Concept|Notation|Meaning|
|---|---|---|
|Cartesian Product|$$A\times B$$|Set of ordered pairs|
|Indexed Family|$${A_i}_{i\in I}$$|Family of sets indexed by I|
|Indexed Union|$$\bigcup_{i\in I}A_i$$|Elements belonging to at least one set|
|Indexed Intersection|$$\bigcap_{i\in I}A_i$$|Elements belonging to every set|
|Disjoint Union|$$A\sqcup B$$|Union preserving component identity|
|Equivalence Relation|$$a\sim b$$|Relation identifying equivalent elements|
|Equivalence Class|$$[a]$$|All elements equivalent to a|
|Quotient Set|$$A/{\sim}$$|Set of all equivalence classes|
|Partition|$$\mathcal{P}$$|Collection of disjoint, nonempty blocks covering a set|

## 9. Visualization and Simulation Methods

### 9.1 Cartesian Product Visualization

Use coordinate systems to visualize Cartesian products.

For example:

$$A=[0,1],\quad B=[0,1]$$

Then:

$$A\times B=[0,1]\times[0,1]$$

This produces a square region in two-dimensional space.

For three-dimensional systems:

$$A\times B\times C$$

can represent a volume or configuration space.

**Recommended visualizations:**

- Cartesian coordinate plots
    
- 2D and 3D point clouds
    
- Configuration-space diagrams
    
- State-space plots
    

### 9.2 Indexed Families Visualization

Represent each set as a separate region or layer.

For example:

$$A_1,A_2,A_3,\ldots,A_n$$

Visualize how these sets overlap, expand, or change with the index.

**Recommended visualizations:**

- Venn diagrams
    
- Time-dependent set diagrams
    
- Layered state-space plots
    
- Set evolution animations
    

### 9.3 Disjoint Union Visualization

Use different colors or labels to distinguish the origin of elements.

Even when two components contain identical numerical values, their tags should remain different.

**Recommended visualizations:**

- Tagged node diagrams
    
- Multi-mode state-space diagrams
    
- Graph-based representations
    
- Hybrid automata
    

### 9.4 Quotient Set and Equivalence Classes Visualization

Group elements into clusters according to an equivalence relation.

For example, integers can be grouped by their remainder modulo 3.

**Recommended visualizations:**

- Cluster diagrams
    
- Graph representations of equivalence relations
    
- Color-coded equivalence classes
    
- Partition diagrams
    

### 9.5 Partition Visualization

Divide a set into non-overlapping regions.

**Recommended visualizations:**

- Venn-style region diagrams
    
- Treemaps
    
- Cluster plots
    
- State-space region maps
    

## 10. Applications in Engineering and Control Theory

### 10.1 Configuration Space in Robotics

The Cartesian product constructs configuration spaces from multiple independent variables:

$$Q=Q_1\times Q_2\times\cdots\times Q_n$$

This allows a robot's complete configuration to be represented as one mathematical object.

### 10.2 Hybrid Dynamical Systems

Disjoint unions represent state spaces with multiple operating modes:

$$X=\bigsqcup_{i\in M}X_i$$

Each mode may have different equations of motion, constraints, and transition rules.

### 10.3 Reachability Analysis

Indexed families describe reachable sets under different initial conditions, time intervals, or disturbances:

$${R(t)}_{t\in T}$$

The union of these sets can describe the total region reachable over a specified time interval:

$$R_{\text{total}}=\bigcup_{t\in T}R(t)$$

### 10.4 State-Space Classification

Partitions divide the state space into regions with different properties:

$$X=\bigcup_{i=1}^{n}X_i$$

This can support:

- Stability classification
    
- Safe and unsafe region identification
    
- Motion planning
    
- Operating mode selection
    
- Controller switching
    

### 10.5 State Abstraction and Model Reduction

Quotient sets can group states that are considered equivalent under a selected relation.

This can reduce the complexity of a model by replacing many individual states with a smaller number of abstract states.

However, the equivalence relation must preserve the properties relevant to the analysis. Arbitrary grouping can remove important dynamical or safety information.

## 11. Research Perspectives and Important Arguments

### 11.1 Set Construction as a Modeling Tool

Set constructions are not merely abstract mathematical operations. They provide a systematic way to represent complex engineering systems.

The choice of construction determines what information is preserved:

- Cartesian products preserve combinations of variables.
    
- Indexed families preserve associations with indices.
    
- Disjoint unions preserve component identity.
    
- Quotient sets identify equivalent elements.
    
- Partitions organize elements into mutually exclusive groups.
    

### 11.2 State-Space Explosion

Cartesian products can cause a rapid increase in dimensionality.

If each of n variables has m possible discrete values, the total number of combinations is:

$$m^n$$

This is known as combinatorial state-space growth.

It is an important challenge in:

- Robotics
    
- Hybrid systems
    
- Formal verification
    
- Model checking
    
- Multi-agent systems
    

A research question is how to construct a sufficiently expressive state space without introducing unnecessary complexity.

### 11.3 Equivalence Relations and Model Reduction

Quotient constructions can reduce the number of states by grouping equivalent states.

However, a key research challenge is defining an equivalence relation that preserves the properties of interest.

For example:

- Does the reduced model preserve stability?
    
- Does it preserve reachability?
    
- Does it preserve collision-free behavior?
    
- Does it preserve the original system's input-output behavior?
    

In dynamical systems, bisimulation and behavioral equivalence provide more structured ways to define state equivalence.

### 11.4 Partition-Based Safety Verification

Partitions can divide a continuous state space into smaller regions for analysis.

For example:

$$X=X_{\text{safe}}\cup X_{\text{unsafe}}$$

with:

$$X_{\text{safe}}\cap X_{\text{unsafe}}=\emptyset$$

This representation is useful in safety verification, although practical verification may require additional methods such as reachability analysis and invariant-set computation.

### 11.5 Discrete and Continuous Representations

Set constructions can be applied to both discrete and continuous systems.

Examples include:

- Finite sets of robot operating modes.
    
- Continuous position and velocity spaces.
    
- Hybrid state spaces combining discrete and continuous variables.
    
- Quotient spaces representing periodic or symmetric configurations.
    

A major modeling challenge is selecting a mathematical representation that captures both the system's structure and its physical meaning.

## 12. Additional Concepts Worth Studying

|Concept|Why It Matters|
|---|---|
|Relations|General framework for describing relationships between elements|
|Functions and Mappings|Formalize transformations between sets|
|Equivalence Relations|Define when elements should be treated as identical|
|Partial Orders|Organize elements through hierarchical relationships|
|Bijections|Establish structural equivalence between sets|
|Cardinality|Measure the size of sets|
|Power Sets|Construct the collection of all subsets|
|Set Partitions and Bell Numbers|Study the number of possible partitions|
|Bisimulation|Define behavioral equivalence between system states|
|Quotient Topology|Extend quotient constructions to topological spaces|
|Product Spaces|Generalize Cartesian products to structured mathematical spaces|

## 13. Suggested Learning Roadmap

1. Understand Cartesian products and ordered tuples.
    
2. Study indexed families and generalized union/intersection.
    
3. Distinguish ordinary union from disjoint union.
    
4. Learn binary relations and their properties.
    
5. Understand equivalence relations and equivalence classes.
    
6. Derive quotient sets from equivalence relations.
    
7. Study partitions and their relationship with equivalence classes.
    
8. Explore quotient constructions in algebra and topology.
    
9. Apply these concepts to configuration spaces and hybrid dynamical systems.
    
10. Investigate state abstraction, bisimulation, and formal verification.
    

## 14. Summary

> [!summary] Key Takeaways
> 
> - **Cartesian Product** constructs sets of ordered combinations.
>     
> - **Indexed Families of Sets** organize collections using an index set.
>     
> - **Disjoint Union** combines sets while preserving the identity of each component.
>     
> - **Equivalence Relations** define which elements should be considered equivalent.
>     
> - **Equivalence Classes** group elements that are equivalent to one another.
>     
> - **Quotient Sets** represent collections of equivalence classes.
>     
> - **Partitions** divide a set into nonempty, mutually disjoint subsets that cover the entire set.
>     
> 
> The central relationship is that equivalence relations generate partitions, and quotient sets are collections of the resulting equivalence classes.
> 
> These constructions are fundamental for building configuration spaces, representing hybrid systems, simplifying mathematical models, and organizing state spaces for control and verification.