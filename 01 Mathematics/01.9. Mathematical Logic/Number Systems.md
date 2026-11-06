---
type: technical-term
title: Number Systems
aliases:
  - Number System
  - Mathematical Number Systems
abbreviation: ""
field:
  - Mathematics
  - Computer Science
  - Engineering
subfield:
  - Set Theory
  - Algebra
  - Number Theory
  - Mathematical Foundations
status: learning
confidence: 1
created: 2026-10-31
updated: 2026-10-31
tags:
  - technical-term
  - mathematics
  - number-systems
  - algebra
  - mathematical-foundations
related:
  - "[[MOC - Number Systems]]"
---
# Number Systems

## 1. Identification

> [!abstract] Definition
> A **number system** is a mathematical framework consisting of a collection of numbers together with operations and, depending on the structure, relations that define how those numbers behave.
>
> Number systems provide the foundation for counting, measuring, comparing quantities, representing mathematical objects, and performing numerical computations.

- **Preferred term:** Number Systems
- **Domain:** Mathematics
- **Subdomains:** Number Theory, Algebra, Set Theory, Mathematical Foundations
- **Primary mathematical structures:** Sets equipped with arithmetic operations and relations.

## 2. Definition and Core Concept

### 2.1 Fundamental Number Sets

> [!abstract] Classification of Number Systems
> The commonly used number systems in mathematics include natural numbers, integers, rational numbers, real numbers, and complex numbers.
>
> Each system extends the capabilities of the preceding systems by introducing additional types of numbers.

The conventional inclusion hierarchy is:

$$
\mathbb{N}\subseteq
\mathbb{Z}\subseteq
\mathbb{Q}\subseteq
\mathbb{R}\subseteq
\mathbb{C}
$$

Where:

| Symbol | Name | Description |
|---|---|---|
| \(\mathbb{N}\) | Natural numbers | Counting numbers |
| \(\mathbb{Z}\) | Integers | Positive, negative, and zero |
| \(\mathbb{Q}\) | Rational numbers | Ratios of integers |
| \(\mathbb{R}\) | Real numbers | Rational and irrational numbers |
| \(\mathbb{C}\) | Complex numbers | Numbers with real and imaginary parts |

**Convention:** Some mathematical disciplines define \(\mathbb{N}\) as including zero, while others start at one. This note uses the convention:

$$
\mathbb{N}=\{0,1,2,3,\ldots\}
$$

### 2.2 Natural Numbers

> [!abstract] Natural Numbers
> The **natural numbers** are the numbers used primarily for counting and indexing.
>
> Under the convention used in this note:

$$
\mathbb{N}=\{0,1,2,3,\ldots\}
$$

Examples:

$$
0,\ 1,\ 2,\ 3,\ 4,\ 5,\ldots
$$

Important properties:
- Closed under addition.
- Closed under multiplication.
- Not closed under subtraction.
- Not closed under division.

For example:

$$
3+2=5\in\mathbb{N}
$$

But:

$$
2-5=-3\notin\mathbb{N}
$$

### 2.3 Integers

> [!abstract] Integers
> The **integers** are numbers consisting of negative whole numbers, zero, and positive whole numbers.

$$
\mathbb{Z}=
\{\ldots,-3,-2,-1,0,1,2,3,\ldots\}
$$

Important properties:
- Closed under addition.
- Closed under subtraction.
- Closed under multiplication.
- Not closed under division.

Example:

$$
3-7=-4\in\mathbb{Z}
$$

However:

$$
\frac{1}{2}\notin\mathbb{Z}
$$

### 2.4 Rational Numbers

> [!abstract] Rational Numbers
> A **rational number** is a number that can be expressed as the ratio of two integers, where the denominator is nonzero.

$$
\mathbb{Q}=
\left\{
\frac{p}{q}
\;\middle|\;
p,q\in\mathbb{Z},\ q\neq0
\right\}
$$

Examples:

$$
\frac{1}{2},\quad
-\frac{3}{4},\quad
5,\quad
0.25
$$

Important properties:
- Closed under addition.
- Closed under subtraction.
- Closed under multiplication.
- Closed under division by nonzero rational numbers.

A rational number has a decimal representation that either terminates or eventually repeats.

### 2.5 Irrational Numbers

> [!abstract] Irrational Numbers
> An **irrational number** is a real number that cannot be expressed as a ratio of two integers.

The irrational numbers are represented by:

$$
\mathbb{R}\setminus\mathbb{Q}
$$

Examples:

$$
\sqrt{2},\quad
\pi,\quad
e
$$

Their decimal expansions are non-terminating and non-repeating.

> [!important] Distinction
> Irrational numbers are not a separate extension in the standard inclusion chain. They form the complement of the rational numbers within the real numbers.

### 2.6 Real Numbers

> [!abstract] Real Numbers
> The **real numbers** consist of all rational and irrational numbers.
>
> They represent points on the continuous one-dimensional number line.

$$
\mathbb{R}=
\mathbb{Q}\cup
(\mathbb{R}\setminus\mathbb{Q})
$$

Examples:

$$
-5,\quad
0,\quad
\frac{2}{3},\quad
\sqrt{2},\quad
\pi
$$

Important properties:
- Closed under addition, subtraction, and multiplication.
- Closed under division by nonzero real numbers.
- Equipped with an order relation.
- Complete with respect to the usual absolute-value metric.

The completeness property distinguishes the real numbers from the rational numbers.

### 2.7 Complex Numbers

> [!abstract] Complex Numbers
> A **complex number** is a number consisting of a real part and an imaginary part.

$$
z=a+bi
$$

where:

- \(a\in\mathbb{R}\): Real part.
- \(b\in\mathbb{R}\): Imaginary coefficient.
- \(i\): Imaginary unit.

The imaginary unit satisfies:

$$
i^2=-1
$$

The set of complex numbers is:

$$
\mathbb{C}=
\{a+bi\mid a,b\in\mathbb{R}\}
$$

Examples:

$$
3+2i,\quad
-1+4i,\quad
5,\quad
2i
$$

Every real number is also a complex number with zero imaginary part:

$$
a=a+0i
$$

Therefore:

$$
\mathbb{R}\subseteq\mathbb{C}
$$

## 3. Technical Representation

### 3.1 Number Systems as Sets

> [!info] Set-Theoretic Representation
> Number systems can be represented as sets whose elements satisfy specific mathematical definitions.
>
> These sets can be equipped with operations such as addition and multiplication.

For example:

$$
\mathbb{Z}\subseteq\mathbb{Q}
$$

because every integer can be represented as a rational number:

$$
n=\frac{n}{1}
$$

Similarly:

$$
\mathbb{Q}\subseteq\mathbb{R}
$$

This connects number systems directly to Set-Theoretic Foundations.

### 3.2 Algebraic Structures

> [!abstract] Algebraic Structure
> A number system can be studied as an algebraic structure by examining its elements, operations, and algebraic properties.

| Number system | Common algebraic structure |
|---|---|
| \(\mathbb{N}\) | Commutative monoid under addition |
| \(\mathbb{Z}\) | Commutative ring |
| \(\mathbb{Q}\) | Field |
| \(\mathbb{R}\) | Ordered complete field |
| \(\mathbb{C}\) | Algebraically closed field |

These descriptions refer to the standard arithmetic operations and structures.

### 3.3 Arithmetic Operations

The fundamental arithmetic operations include:

**Addition**

$$
a+b=c
$$

**Subtraction**

$$
a-b=c
$$

**Multiplication**

$$
a\cdot b=c
$$

**Division**

$$
\frac{a}{b}=c,\qquad b\neq0
$$

Different number systems support different operations while preserving closure properties.

### 3.4 Closure Property

> [!abstract] Closure
> A set is closed under an operation if applying that operation to elements of the set always produces another element of the same set.

For a binary operation \(\circ\):

$$
\forall a,b\in S,\quad
a\circ b\in S
$$

Example:

$$
\forall a,b\in\mathbb{Z},
\quad a+b\in\mathbb{Z}
$$

However:

$$
2-5=-3\in\mathbb{Z}
$$

while natural numbers are not closed under subtraction.

### 3.5 Cartesian Products and Coordinate Spaces

> [!info] Product of Number Systems
> Cartesian products of number systems construct higher-dimensional mathematical spaces.

For example:

$$
\mathbb{R}^2=
\mathbb{R}\times\mathbb{R}
$$

$$
\mathbb{R}^3=
\mathbb{R}\times\mathbb{R}\times\mathbb{R}
$$

In general:

$$
\mathbb{R}^n=
\underbrace{
\mathbb{R}\times\cdots\times\mathbb{R}
}_{n\text{ factors}}
$$

An element of \(\mathbb{R}^3\) is an ordered triple:

$$
\mathbf{x}=(x,y,z)
$$

where:

$$
x,y,z\in\mathbb{R}
$$

This provides the numerical foundation for Euclidean Space and Coordinate Systems.

### 3.6 Complex Plane

> [!info] Geometric Representation
> Complex numbers can be represented as points in a two-dimensional plane called the complex plane or Argand plane.

For:

$$
z=a+bi
$$

its corresponding point is:

$$
(a,b)\in\mathbb{R}^2
$$

The modulus is:

$$
|z|=\sqrt{a^2+b^2}
$$

The complex conjugate is:

$$
\overline{z}=a-bi
$$

This representation is useful in signal processing, control theory, and mathematical modeling.

## 4. Applications and Examples

### 4.1 Mathematics and Engineering

> [!example] Numerical Modeling
> Number systems provide the mathematical domain for representing physical quantities, measurements, and mathematical models.

Examples:

| Application | Number system |
|---|---|
| Counting objects | \(\mathbb{N}\) |
| Temperature differences | \(\mathbb{Z}\) |
| Ratios and proportions | \(\mathbb{Q}\) |
| Continuous measurements | \(\mathbb{R}\) |
| Sinusoidal signal analysis | \(\mathbb{C}\) |

### 4.2 Robotics Applications

> [!example] Robot Configuration
> A robot's configuration can be represented using real-valued variables.

For a robot with \(n\) independent real-valued configuration coordinates:

$$
\mathbf{q}=
\begin{bmatrix}
q_1\\
q_2\\
\vdots\\
q_n
\end{bmatrix}
\in\mathbb{R}^n
$$

where \(q_i\) represents a configuration variable.

Examples:
- Joint angles.
- Joint translations.
- Cartesian positions.
- Robot velocities.
- Robot accelerations.

The actual configuration space may be a subset or a more structured space than \(\mathbb{R}^n\), depending on joint constraints and topology.

### 4.3 Swarm Robotics

> [!example] Multi-Robot Position Representation
> The position of robot \(i\) in three-dimensional Euclidean space can be represented as:

$$
\mathbf{p}_i=
\begin{bmatrix}
x_i\\
y_i\\
z_i
\end{bmatrix}
\in\mathbb{R}^3
$$

For a swarm of \(N\) robots:

$$
\mathbf{P}=
\begin{bmatrix}
\mathbf{p}_1\\
\mathbf{p}_2\\
\vdots\\
\mathbf{p}_N
\end{bmatrix}
\in\mathbb{R}^{3N}
$$

This representation supports:
- Formation control.
- Relative position calculations.
- Consensus algorithms.
- Distributed localization.
- Multi-agent trajectory planning.

### 4.4 Complex Numbers in Control Systems

> [!example] Frequency-Domain Analysis
> Complex numbers are widely used to represent sinusoidal signals and system responses in the frequency domain.

A complex frequency variable is:

$$
s=\sigma+j\omega
$$

where:
- \(\sigma\): Real component.
- \(\omega\): Angular frequency.
- \(j\): Engineering notation for the imaginary unit.

The Laplace transform and transfer functions use complex variables to analyze system dynamics and stability.


## 6. Limitations and Evaluation

> [!warning] Important Mathematical Distinctions
>
> 1. **Natural number convention:** Some definitions include zero, while others do not.
> 2. **Rational versus real numbers:** Not every real number can be represented as a ratio of integers.
> 3. **Real versus complex numbers:** Complex numbers extend the real numbers but do not inherit their usual total ordering.
> 4. **Numerical representation:** Computers generally represent real numbers using finite-precision approximations rather than storing arbitrary real numbers exactly.
> 5. **Abstract structure:** A number system is more than a collection of symbols; its operations and structural properties are essential.

> [!important] Real Numbers Are Not the Same as Floating-Point Numbers
> The mathematical set \(\mathbb{R}\) is continuous and uncountable.
>
> Computer floating-point formats represent only a finite subset of numerical values, with rounding and precision limitations.

## 7. Verification and Evidence

> [!success] Established Mathematical Framework
> The standard number systems and their inclusion relationships are foundational mathematical concepts.
>
> Their algebraic structures provide the basis for arithmetic, algebra, analysis, numerical computation, and engineering mathematics.

**Verification status:**
- Number system definitions: Established.
- Set inclusion hierarchy: Established.
- Algebraic classifications: Established.
- Cartesian product representations: Established.
- Robotics applications: Established mathematical applications.

## 8. Personal Notes

> [!question] Questions for Further Study
> - How are natural numbers formally constructed using set theory?
> - Why are rational numbers insufficient for representing all real quantities?
> - What makes the real number system complete?
> - Why are complex numbers necessary for polynomial equations?
> - What is the difference between a field and an ordered field?
> - How are real and complex numbers represented computationally?
> - Why is \(\mathbb{R}^n\) important in robotics and state-space modeling?

## 9. References

1. Enderton, H. B. (1977). *Elements of Set Theory*. Academic Press.
2. Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.
3. Lang, S. (2002). *Algebra* (3rd ed.). Springer.
4. Dummit, D. S., & Foote, R. M. (2004). *Abstract Algebra* (3rd ed.). Wiley.
5. Apostol, T. M. (1967). *Calculus, Volume 1* (2nd ed.). Wiley.

