---
layout: post
title: Linear Algebra - some notes
---


# Upcoming Linear Algebra Midterm Test

I haven't prepared well for it. I wish it will be a good result.
Tomorrow will be the **DAY**.

## Some rank inequalities
- $r(\mathbf{AB}) \leq min \left\\{ r(\mathbf{A}), r(\mathbf{B}) \right\\} $
- $r(\mathbf{A}) = r(\mathbf{A^{T}}) = r(\mathbf{AA^{T}})$
- $r(\mathbf{A + B}) \leq r(\mathbf{A}) + r(\mathbf{B}) \leq n + r(\mathbf{AB})$ (sylvester rank inequality)
- $r(\mathbf{ABC}) +r(\mathbf{B}) \geq r(\mathbf{AB}) + r(\mathbf{BC}) $ (Frobenius rank inequality)

## Some identities
- $(A-BDC)^{-1} = A^{-1} - A^{-1}B(D^{-1}+CA^{-1}B)^{-1} CA^{-1} $ (Woodbury identity)
- $((A-B^{-1})^{-1}-A^{-1})^{-1} = ABA-A $ (Hua's identity)

## Notes
- **Schwarz inequality**: $\lvert a^{T}b \rvert \leq \lvert \lvert a \rvert \rvert  \cdot  \lvert \lvert b \rvert \rvert $
- projection matrix $P = \displaystyle\frac{aa^{T}}{a^{T}a} \quad {\text{or}} \quad $ $$P=\begin{bmatrix} c^2 & cs \\ cs & s^2 \end{bmatrix}$$
- If $\mathbf{W^{\prep}=V} \quad {\text{then}} \quad \dim\mathbf{V} + \dim\mathbf{W} = n $
- orthogonal vectors: $x^{T}y = 0$
- Rotation matrix $$R = \begin{bmatrix} c & -s \\ s & c \end{bmatrix}$$
- Reflection matrix $$H = \begin{bmatrix} 2c^{2}-1 & 2cs \\ 2cs & 2s^{2}-1 \end{bmatrix}$$
- Linearity: $A(cx+dy) = c(Ax) +d(Ay)$
- $r = m$ have ***right-inverse***, $B= (A^{T}A)^{-1}A^{T}$ and $r = n$ have ***left-inverse***, $C = A^{T}(AA^{T})^{-1}$
#### The Four Fundamental Subspaces of a Matrix

For any $m \times n$ matrix A, there are four fundamental subspaces:

$1.$ $C(A)$ (Range)

- Definition: The subspace of $\mathbb{R}^m$ spanned by the column vectors of $A$.
- Dimension: $r = \text{rank}(A)$
- How to find:
  1. Reduce $A$ to RREF
  2. Identify the pivot columns in RREF
  3. The corresponding columns in the original matrix A form a basis for the column space

$2.$ $N(A)$ (Kernel)

- Definition: The subspace of $\mathbb{R}^n$ consisting of all vectors $\mathbf{x}$ such that$ A\mathbf{x} = \mathbf{0}$
- Dimension: $n - r$ (by Rank-Nullity Theorem)
- How to find:
  1. Reduce $A$ to RREF
  2. Solve the system$ A\mathbf{x} = \mathbf{0}$ from the RREF



$3.$ $C(A^{T})$

- Definition: The subspace of $\mathbb{R}^n$ spanned by the row vectors of $A$
- Dimension: $r = \text{rank}(A)$
- How to find:
  1. Reduce $A$ to RREF
  2. The non-zero rows in RREF form a basis for the row space
  - Note: Row operations preserve the row space

$4.$ $N(A^{T})$

- Definition: The subspace of $\mathbb{R}^m$ consisting of all vectors $\mathbf{y}$ such that $A^T\mathbf{y} = \mathbf{0}$
- Dimension: $m - r$
- How to find:
  1. Method 1: Find the null space of $A^T$ using the same procedure as for the null space
  2. Method 2: If $PA = R$ and $P$ tracks row operations, the rows of $P$ corresponding to zero rows in $R$ form a basis

Key Relationships:

- Column space and left null space are orthogonal complements in $\mathbb{R}^m$
- Row space and null space are orthogonal complements in $\mathbb{R}^n$
- $\text{dim}(C(A)) = \text{dim}(C(A^{T})) = \text{rank}(A)$
- $\text{dim}(C(A^{T})) = n - \text{rank}(A)$
- $\text{dim}(N(A^{T})) = m - \text{rank}(A)$

## Still notes
- $\mathbf{Ax=b} \quad {\text{is solvable if }} \quad r(\mathbf{A}) = m, {\text{has most 1 solution if}} \quad r(\mathbf{A}) = n$
  
#### Solve $\mathbf{Ax=b}$
1. solve $\mathbf{Ax=0}$
   1. reduce to RREF
   2. let free variables successively become 1
   3. find all the special solution
2. let free variables become 0, then solve $\mathbf{Ax=b}$

## And notes
- $(A^{T}A)^{T}=A^{T}A$ symmetric matrix
- $(AA^{-1})^{-1}=A^{-1}A$
- Gauss-Jordan method to find inverse
- Triangular factorization $A=LU \quad {\text{or}} \quad A=LDU$
- $r(AB)=r(A) \quad {\text{if}} \quad r(B)=n$
- If $A = u^{T}v \quad {\text{then}} \quad A^{n}= u^{T}(vu^{T})^{n-1}v$
- Suppose $A^{2}=A ,B^{2}=B;{\text{ then }} AB=BA=0 {\text{ if }} (A+B)^{2}=A+B$
- Skew-symmetric matrix $A^{T}=-A$
- To prove $\eta_{1},\eta_{2},\eta_{3} {\text{ are linear independent is equivalent to prove }} c_{1}\eta_{1}+c_{2}\eta_{2}+c_{3}\eta_{3} = 0 {\text{ only when }} c_{1}=c_{2}=c_{3}=0$. Apply $A$ on it serval times may be helpful
