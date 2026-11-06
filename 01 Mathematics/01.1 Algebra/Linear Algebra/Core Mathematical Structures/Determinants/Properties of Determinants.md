---
type: technical-term
title: "Properties of Determinants"
aliases: []
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - technical-term
  - linear-algebra
  - determinants
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023."
related: []
projects: []
---

> [!abstract] Definition
> The **properties of determinants** are algebraic identities and transformation rules that describe how the determinant changes under matrix operations.
>
> These properties are used to simplify determinant calculations, establish theoretical results, and determine matrix invertibility.

## 1. Identity Matrix

> [!math] Property
> For the identity matrix $I_n$:
>
> $$
> \det(I_n)=1
> $$

## 2. Transpose

> [!math] Property
> A matrix and its transpose have the same determinant:
>
> $$
> \boxed{\det(A^T)=\det(A)}
> $$
>
> Consequently, every determinant property stated in terms of rows has a corresponding property in terms of columns.

## 3. Matrix Multiplication

> [!math] Multiplicative Property
> For two square matrices $A$ and $B$ of the same order:
>
> $$
> \boxed{\det(AB)=\det(A)\det(B)}
> $$
>
> This property shows that the determinant is multiplicative with respect to matrix multiplication.
>
> In general, the determinant is not additive:
>
> $$
> \det(A+B)\neq\det(A)+\det(B)
> $$
>
> The equality does not hold in general.

## 4. Scalar Multiplication

> [!math] Property
> For an $n\times n$ matrix $A$ and scalar $c$:
>
> $$
> \boxed{\det(cA)=c^n\det(A)}
> $$
>
> The exponent $n$ appears because multiplying the entire matrix by $c$ scales each of its $n$ rows by $c$.

## 5. Elementary Row Operations

> [!important] Effect on Determinants
> The three elementary row operations affect determinants differently.
>
> **1. Row interchange**
>
> Swapping two rows changes the sign:
>
> $$
> R_i\leftrightarrow R_j
> \quad\Longrightarrow\quad
> \det(B)=-\det(A)
> $$
>
> **2. Row scaling**
>
> Multiplying one row by a scalar $c$ multiplies the determinant by $c$:
>
> $$
> R_i\rightarrow cR_i
> \quad\Longrightarrow\quad
> \det(B)=c\det(A)
> $$
>
> **3. Row replacement**
>
> Adding a multiple of one row to another row does not change the determinant:
>
> $$
> R_i\rightarrow R_i+cR_j
> \quad\Longrightarrow\quad
> \det(B)=\det(A)
> $$
>
> Here, $B$ denotes the matrix after the specified operation.

## 6. Linearly Dependent Rows or Columns

> [!important] Zero Determinant
> If the rows or columns of a square matrix are linearly dependent, then:
>
> $$
> \boxed{\det(A)=0}
> $$
>
> Conversely, if the determinant is zero, the rows and columns are linearly dependent.

## 7. Equal or Proportional Rows

> [!note] Special Cases
> - If two rows are identical, the determinant is zero.
> - If two columns are identical, the determinant is zero.
> - If one row or column is a scalar multiple of another, the determinant is zero.
>
> These are consequences of linear dependence.

## 8. Triangular Matrices

> [!math] Diagonal Product
> For an upper or lower triangular matrix:
>
> $$
> A=
> \begin{bmatrix}
> a_{11}&*&\cdots&*\\
> 0&a_{22}&\cdots&*\\
> \vdots&\ddots&\ddots&\vdots\\
> 0&\cdots&0&a_{nn}
> \end{bmatrix}
> $$
>
> Its determinant is the product of its diagonal entries:
>
> $$
> \boxed{
> \det(A)=\prod_{i=1}^{n}a_{ii}
> }
> $$

## 9. Inverse

> [!math] Determinant of an Inverse
> If $A$ is invertible:
>
> $$
> \det(A^{-1})=\frac{1}{\det(A)}
> $$
>
> This follows from:
>
> $$
> AA^{-1}=I
> $$
>
> and the multiplicative property of determinants.

## 10. Powers of a Matrix

> [!math] Property
> For a square matrix $A$ and a nonnegative integer $k$:
>
> $$
> \det(A^k)=(\det A)^k
> $$
>
> This follows by repeatedly applying the multiplicative property.

## 11. Practical Computational Strategy

> [!tip] Using Row Reduction
> Determinants can be calculated efficiently by transforming a matrix into triangular form.
>
> During elimination:
> - Track every row interchange because it changes the sign.
> - Track every row scaling because it changes the determinant by the scaling factor.
> - Row replacement does not change the determinant.
>
> Once the matrix is triangular, multiply its diagonal entries and account for all recorded changes.

## 12. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Matrices:** Provides the objects on which determinant operations are defined.
> - **Matrix Operations:** Provides multiplication and transpose operations.
> - **Elementary Row Operations:** Explains how row transformations affect determinants.

> [!info] Relevant
> - **Linear Independence:** Explains why dependent rows or columns produce a zero determinant.

### Downstream Knowledge

> [!info] Relevant
> - **Cofactor Expansion:** Uses determinant identities to calculate determinants recursively.
> - **Determinants and Invertibility:** Uses the nonzero-determinant criterion.
> - **Matrix Inverse:** Uses determinant identities involving inverses.

> [!info] Advanced
> - **Eigenvalues and Eigenvectors:** Uses determinant multiplicativity in characteristic-polynomial calculations.
> - **LU Decomposition:** Uses triangular matrix determinants to simplify determinant computation.

## 13. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., Pearson, 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., Wellesley-Cambridge Press, 2023.