---
type: technical-term
title: "Matrix Multiplication"
aliases:
  - Matrix Product
  - Matrix-Vector Multiplication
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - mathematics
  - linear-algebra
  - matrix-multiplication
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---

# Matrix Multiplication

> [!abstract] Definition
> Matrix multiplication is an operation that combines two matrices by taking dot products between rows of the first matrix and columns of the second matrix.

## 1. Dimension Compatibility

> [!important] Multiplication Rule
> If:
>
> $$
> A\in\mathbb{F}^{m\times n},
> \qquad
> B\in\mathbb{F}^{n\times p}
> $$
>
> then:
>
> $$
> AB\in\mathbb{F}^{m\times p}
> $$
>
> The number of columns in $A$ must equal the number of rows in $B$.

## 2. Entrywise Definition

> [!definition] Matrix Product
> The entry in row $i$ and column $j$ of $C=AB$ is:
>
> $$
> c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}
> $$
>
> Each entry is the dot product of row $i$ of $A$ and column $j$ of $B$.

<LearningViz type_id="MATRIX_MULTIPLICATION_ROW_COLUMN_RULE" />

## 3. Example

Let:

$$
A=
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix},
\qquad
B=
\begin{bmatrix}
5&6\\
7&8
\end{bmatrix}
$$

Then:

$$
AB=
\begin{bmatrix}
1(5)+2(7)&1(6)+2(8)\\
3(5)+4(7)&3(6)+4(8)
\end{bmatrix}
$$

$$
AB=
\begin{bmatrix}
19&22\\
43&50
\end{bmatrix}
$$

## 4. Algebraic Properties

> [!important] Fundamental Properties
> **Associativity**
> $$
> (AB)C=A(BC)
> $$
>
> **Distributivity**
> $$
> A(B+C)=AB+AC
> $$
>
> $$
> (A+B)C=AC+BC
> $$
>
> **Identity**
> $$
> AI_n=A,\qquad I_mA=A
> $$
>
> **Scalar Compatibility**
> $$
> \alpha(AB)=(\alpha A)B=A(\alpha B)
> $$

> [!warning] Noncommutativity
> $$
> AB\neq BA
> $$
>
> Matrix multiplication is generally not commutative. In addition, one of $AB$ and $BA$ may exist while the other does not.

## 5. Matrix-Vector Multiplication

> [!definition] Matrix Acting on a Vector
> For $A\in\mathbb{F}^{m\times n}$ and $\mathbf{x}\in\mathbb{F}^n$:
>
> $$
> A\mathbf{x}\in\mathbb{F}^m
> $$
>
> This product forms a linear combination of the columns of $A$, with entries of $\mathbf{x}$ as coefficients.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — provides matrix structure and dimensions.
- **Vectors** — provides the vectors used in matrix-vector products.
- **Dot Product** — explains the row-column computation.

### Downstream Knowledge
- **Linear Transformations** — interprets matrix multiplication as composition of linear maps.
- **Matrix Inverse** — studies inverses of matrix products.
- **Matrix Factorization** — represents matrices as products of simpler matrices.

## 7. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*, 2000.