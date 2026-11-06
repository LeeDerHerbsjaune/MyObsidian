---
type: technical-term
title: "Cofactor Expansion"
aliases:
  - Laplace Expansion
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
> **Cofactor expansion**, also called **Laplace expansion**, is a recursive method for calculating the determinant of a square matrix by expressing it as a sum of products involving matrix entries and their corresponding cofactors.
>
> It reduces the calculation of an $n\times n$ determinant to determinants of $(n-1)\times(n-1)$ submatrices.

## 1. Minor

> [!abstract] Definition
> The **minor** of an entry $a_{ij}$, denoted by $M_{ij}$, is the determinant of the submatrix obtained by deleting row $i$ and column $j$ from the original matrix.
>
> If $A$ is an $n\times n$ matrix, then $M_{ij}$ is the determinant of an $(n-1)\times(n-1)$ matrix.

## 2. Cofactor

> [!abstract] Definition
> The **cofactor** of the entry $a_{ij}$ is:
>
> $$
> \boxed{
> C_{ij}=(-1)^{i+j}M_{ij}
> }
> $$
>
> The factor $(-1)^{i+j}$ determines the sign of the minor.

> [!note] Cofactor Sign Pattern
> The signs follow a checkerboard pattern:
>
> $$
> \begin{bmatrix}
> +&-&+&\cdots\\
> -&+&-&\cdots\\
> +&-&+&\cdots\\
> \vdots&\vdots&\vdots&\ddots
> \end{bmatrix}
> $$

## 3. Cofactor Expansion Along a Row

> [!math] Row Expansion
> The determinant can be expanded along any row $i$:
>
> $$
> \boxed{
> \det(A)=
> \sum_{j=1}^{n}a_{ij}C_{ij}
> }
> $$
>
> Equivalently:
>
> $$
> \det(A)=
> \sum_{j=1}^{n}
> (-1)^{i+j}a_{ij}M_{ij}
> $$

## 4. Cofactor Expansion Along a Column

> [!math] Column Expansion
> The determinant can also be expanded along any column $j$:
>
> $$
> \boxed{
> \det(A)=
> \sum_{i=1}^{n}a_{ij}C_{ij}
> }
> $$
>
> Equivalently:
>
> $$
> \det(A)=
> \sum_{i=1}^{n}
> (-1)^{i+j}a_{ij}M_{ij}
> $$
>
> Both row and column expansions produce the same determinant.

## 5. Example: 3 × 3 Matrix

> [!example] Cofactor Expansion
> Consider:
>
> $$
> A=
> \begin{bmatrix}
> a&b&c\\
> d&e&f\\
> g&h&i
> \end{bmatrix}
> $$
>
> Expanding along the first row:
>
> $$
> \det(A)=
> a\begin{vmatrix}e&f\\h&i\end{vmatrix}
> -b\begin{vmatrix}d&f\\g&i\end{vmatrix}
> +c\begin{vmatrix}d&e\\g&h\end{vmatrix}
> $$
>
> Evaluating the $2\times2$ determinants:
>
> $$
> \det(A)=a(ei-fh)-b(di-fg)+c(dh-eg)
> $$

## 6. Choosing an Expansion Direction

> [!tip] Computational Efficiency
> Cofactor expansion can be performed along any row or column.
>
> A useful strategy is to choose a row or column containing the largest number of zeros.
>
> Every zero entry eliminates one term from the expansion, reducing the number of subdeterminants that must be calculated.

## 7. Important Properties

> [!important] Key Properties
> - Cofactor expansion is valid along every row and every column.
> - The resulting determinant is independent of the chosen expansion direction.
> - An $n\times n$ determinant is reduced to determinants of order $n-1$.
> - The signs of cofactors alternate according to $(-1)^{i+j}$.
> - Cofactor expansion is mathematically general but can be computationally expensive for large matrices.

## 8. Connection to the Adjugate Matrix

> [!note] Adjugate
> The **adjugate matrix** of $A$, denoted by $\operatorname{adj}(A)$, is the transpose of its cofactor matrix:
>
> $$
> \operatorname{adj}(A)=C^T
> $$
>
> Where $C$ is the matrix whose entries are the cofactors $C_{ij}$.
>
> The adjugate satisfies:
>
> $$
> A\operatorname{adj}(A)
> =
> \operatorname{adj}(A)A
> =
> \det(A)I
> $$
>
> Consequently, if $\det(A)\neq0$:
>
> $$
> A^{-1}
> =
> \frac{1}{\det(A)}
> \operatorname{adj}(A)
> $$
>
> This provides a theoretical formula for the inverse of a nonsingular square matrix.

## 9. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Determinants:** Cofactor expansion is a method for evaluating determinants.
> - **Matrix Operations:** Submatrix construction requires understanding matrix structure.

> [!info] Relevant
> - **Properties of Determinants:** Provides identities useful for simplifying calculations.

### Downstream Knowledge

> [!info] Relevant
> - **Determinants and Invertibility:** Cofactors contribute to the adjugate formula for the inverse.
> - **Matrix Inverse:** The adjugate provides an explicit inverse formula when the determinant is nonzero.

> [!info] Advanced
> - **Characteristic Polynomial:** Cofactor expansion can be used to calculate $\det(\lambda I-A)$.

## 10. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., Pearson, 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., Wellesley-Cambridge Press, 2023.