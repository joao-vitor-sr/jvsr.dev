+++
title = "Overview over linear algebra"
date = 2023-03-29
slug = "katex"

[extra]
katex = true
+++

In recent years, linear models have become quite famous. And have assumed very
important roles in almost all the physical and social sciences, and as
expected, this has stimulated the growth in the interest in linear algebra.

The article that you're reading has the intent that even if you don't
understand anything about linear algebra, at least understand what it's and
why it's useful. I don't intend to explain all computations and proofs behind
the models, so if you're searching for something more complete, this is not
the place for you (good luck with your search 😀)

## Vectors

We can say that the foundation of linear models is the vector, so it's good to
understand what it's and why it's so important.

In the mathematical world, we have three main distinct approaches to what's a
vector. There is the computer science perspective, the physics, and the purely
mathematical one.

### Physics perspective

From the perspective of physics, a vector is an arrow in space. That contains
two properties magnitude, and direction, and its dimension can be
two-dimensional or three (on mathematical computation, it's possible to have
vectors on the fourth dimension, but since we cannot understand this dimension
at its full potential, the definition of this dimension is purely
mathematical).

Many physical quantities are vectors, and it's interesting how the same rule
of operations applies to all of them.

Generally, a vector may originate from any point in space and end at any other.

### Computer science perspective

In this perspective, vectors are a list of numbers with a length of n (this
represents the size of the list). The order matters.

££
\begin{pmatrix}
1 & 3 & 5
\end{pmatrix} \\mathrel{\\char`≠} \begin{pmatrix}
3 & 1 & 5
\end{pmatrix}
££

### Mathematical Perspective

And finally, we have the mathematical approach, which remembers the physical
notion, but with some differences.

First of all, the vectors are not dependent on space, so it's possible to have
any n-dimensional vector without limits, and it's also similar to the CS
perspective, that it's a list of numbers.

## Matrices

With the definition of the vector clear, we can keep forward to the matrix
definition.

This definition provides a powerful tool. A matrix is a rectangular array of
numbers arranged into rows and columns.

££
\begin{bmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\\\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\\\
\vdots & & & \vdots \\\\
a_{m,1} & a_{m,2} & \cdots & a_{m,n}
\end{bmatrix}
££

It's an m by n (it's written as m x n) matrix. Matrices don't have numerical
values. Instead, it's a way to manage tables of numbers. A double subscript
represents any one of its elements. By convention, the first subscript is the
row, and the second one is the column, so the following equation represents a
value from matrix A, that's at row 1 and column 2

££
a_{1,2}
££

### Examples

Here is a small colection of matrices
££
\begin{bmatrix}
1 & 0 \\\\
0 & 1
\end{bmatrix} \begin{bmatrix}
a_{1,1} & a_{1,2} \\\\
a_{2,1} & a_{2,2}
\end{bmatrix} \begin{bmatrix}
a & b \\\\
c & d
\end{bmatrix} \begin{bmatrix}
1 & 2 & 4 \\\\
\lambda & \beta & \alpha
\end{bmatrix}
££

It's possible to have different numbers of rows and columns (the
fourth matrix is an example, with two rows and three columns)

## Operations

Even if a matrix is just a collection of numbers (arrays/tables) still is
possible to do operations, most of which will be similar to the traditional
ones. However, some require a "special" focus since they can be different.

### Equality

A matrix is said to be equal only if all elements are equal
(this applies to the size too).

_Examples:_

££
A = \begin{bmatrix}
1 & 0 \\\\
0 & 1
\end{bmatrix}, B = \begin{bmatrix}
1 & 1 \\\\
0 & 0
\end{bmatrix}
££
A is different from B, since the elements values are different

££
A = \begin{bmatrix}
1 & 4 & 7 \\\\
8 & 1 & 2
\end{bmatrix}, B = \begin{bmatrix}
5 & \lambda \\\\
\beta & 1
\end{bmatrix}
££
They are not equal, since the size is different, and therefore values are also

££
A = \begin{bmatrix}
2 & 8 \\\\
9 & 1
\end{bmatrix}, B = \begin{bmatrix}
2 & 8 \\\\
9 & 1
\end{bmatrix}
££
Here the matrices are equal, because the size is the same, and all elemnts have
the same value

### Multiplication by scalar

Given a matrix $(A)$ and a scalar $(\lambda)$ the product of $(\lambda)$
and $(A)$ written $(\lambda A )$ is
££
\lambda A = \begin{bmatrix}
  \lambda a_{1,1} & \cdots & \lambda a_{1,n} \\\\
  \lambda a_{2,1} & \cdots & \lambda a_{2,n} \\\\
  \vdots  & & \vdots \\\\
  \lambda a_{m, 1} & \cdots & \lambda a_{m, n}
\end{bmatrix}
££

Each element of A is multiplied by the scalar (in this case $(\lambda)$), and
the product will be a matrix m X n

_Examples:_

££
\begin{aligned}
\lambda = 2, && A = \begin{bmatrix}
4 & 7 \\\\
8 & 9
\end{bmatrix} && \lambda A = \begin{bmatrix}
8 & 14 \\\\
16 & 18
\end{bmatrix} \\\\\\\\
\lambda = -4, && A = \begin{bmatrix}
1 & 2 \\\\
0 & 1
\end{bmatrix}, && \lambda A = \begin{bmatrix}
-4 & -8 \\\\
0 & -4
\end{bmatrix}
\end{aligned}
££

### Addition

The sum C of a matrix A having m rows and n columns and a matrix B having m rows
and n columns is a matrix having m rows and n columns.

In addition, there's a sum in each element

_Examples:_

The sum

££
C = A + B
££

Expands to

££
\begin{aligned}
C &= \begin{bmatrix}
c_{1,1} & \cdots & c_{1,n} \\\\
\vdots & & \vdots \\\\
c_{m,1} & \cdots & c_{m,n}
\end{bmatrix} = \begin{bmatrix}
a_{1,1} & \cdots & a_{1,n} \\\\
\vdots & & \vdots \\\\
a_{m,1} & \cdots & a_{m,n}
\end{bmatrix} + \begin{bmatrix}
b_{1,1} & \cdots & b_{1,n} \\\\
\vdots & & \vdots \\\\
b_{m,1} & \cdots & b_{m,n}
\end{bmatrix} \\\\
&= \begin{bmatrix}
a_{1,1} + b_{1,1} & \cdots & a_{1,n} + b_{1,n} \\\\
\vdots & & \vdots \\\\
a_{m,1} + b_{m,1} & \cdots & a_{m,n} + b_{m,n}
\end{bmatrix}
\end{aligned}
££

If the number of rows or columns is different between the matrices, the
operation is said to be undefined.

Note that the addition is commutative (which in linear algebra is not always
true for all operations)

££
A + B = B + A,
A + (B + C) = (A + B) + C = A + B + C
££

### Subtraction

The subtraction is defined to be the sum of two matrices, but the matrix that
is subtracting is pre-multiplied by -1, as an example:

££
A - B = A + (-1) B
££

## Matrix multiplication

Think of a way to multiply two matrices. You can try to do something similar
to sum, multiplying each element with its equivalent on the other matrix.

So try to ponder a little and think of a way to multiply two different
matrices, even when the rows and columns lengths are equal.

Because of this, matrix multiplication is not equal to "traditional" matrix
operations. (this is not the unique reason)

So the operation of the multiplication is in this way.

### Operation

The operation is related to the row of matrix A and the column of
matrix B, as an example:

££
A = \begin{bmatrix}
1 & 3 \\\\
2 & 4
\end{bmatrix}, B = \begin{bmatrix}
2 & 1 \\\\
3 & 5
\end{bmatrix}, C = \begin{bmatrix}
1(2) + 3(3) & 1(1) + 3(5) \\\\
2(2) + 4(3) & 2(1) + 4(5)
\end{bmatrix} = \begin{bmatrix}
11 & 16 \\\\
16 & 22
\end{bmatrix}
££

As you can see, the first row multiplies the second column, and finally, there
is a sum of the elements.

££
A = \begin{bmatrix}
3 & 2 \\\\
6 & 1
\end{bmatrix}, B = \begin{bmatrix}
4 \\\\
5
\end{bmatrix}, C = \begin{bmatrix}
3(4) + 2(5) \\\\
6(4) + 1(5)
\end{bmatrix} = \begin{bmatrix}
22 \\\\
29
\end{bmatrix}
££

The matrix C is m X r when A is m X n, and B k X r. The resulting matrix has
the same number of rows as the first matrix and the same number of columns as
the second one.

Remember that the multiplication is not always commutative since not always
the rules of the rows and columns sizes are applied, see:

££
A = \begin{bmatrix}
2 & 1 \\\\
3 & 1
\end{bmatrix}, B = \begin{bmatrix}
2 \\\\
1
\end{bmatrix}, AB = \begin{bmatrix}
5 \\\\
7
\end{bmatrix}
££

However, BA is undefined since the number of columns in B is not the same as
the number of rows in A

## Linear dependence

Linear dependence or independence are properties of the set of vectors, not the
individual vectors.

A set is said to be a dependency, $( (a_1, \cdots, a_m) )$ from $(E^n)$
is said to be dependent if there is some scalar (not all zeros), that

££
\lambda_1 a_1 + \lambda_2 a_2 + \cdots + \lambda_m a_m = 0
££

or in other words, there is a set (in En)En) that when multiplied by a scalar.

## Basis Vectors

Until now, we were working with vector coordinates, but instead, think of each
coordinate as a scalar and think about how they change the space. The number
that those scalars modify is the basis vector.

With this in mind, think of vector coordinates as scalars that modify the
basis vectors.

With this definition, it's possible to have a different basis. And at the same
time, still, be possible to reach all points in space just by changing the
scalars.

## Linear transformations

It is not uncommon to apply transformations in a set of values. However,
linear models use a special kind of transformation called linear.

An example, $(Y = Ax)$ is a linear transformation, that moves x points to
other points in space.

It's possible to say the values of Y are the same as x, but after that, matrix
A transformed the points on x.

££
\begin{aligned}
y_1 = Ax_1, & & y_2 = Ax_2 \\\\
y_1 + y_2 &= Ax_1 + Ax_2 &= A(x_1 + x_2)
\end{aligned}
££

The technical definition is.

A linear transformation T on the space $(E^n)$ is a correspondence that maps
each vector x of $(E^n)$ into a vector T(x) of $(E^m)$, such that

££
T({\lambda}_1 x_1 + {\lambda}_2 + x_2) = {\lambda}_1 T(x_1) + {\lambda}_2T(x_2)
££

This equation preserves addition and multiplication by a scalar

Any matrix transformation is a linear transformation since all rules apply to
matrices

_Examples:_

Linear:
££
T({\lambda}_1 x_1 + {\lambda}_2 x_2) = a({\lambda}_1 x_1 + {\lambda}_2 x_2) =
{\lambda}_1(ax_1) + {\lambda}_2(ax_2) = {\lambda}_1 T(x_1) + {\lambda}_2 T(x_2)
££

It's linear, but the following one is not linear.

££
T(\lambda_1 x_1 + \lambda_2 x_2) = a(\lambda_1 x_1 + \lambda_2 x_2)^2 =
a(\lambda_1 x_1)^2 + a(\lambda_2 x_2)^2 + 2a\lambda_1 \lambda_2 x_1 x_2
££

So this equation is not linear and therefore is not a valid transformation.

## Determinant

A determinant is defined to be the number computed from
the following sum. Involving the $(n^2$) elements in A

££
|A| = \sum (\pm) a_{1,i}, a_{2,j}, \cdots, a_{n,r}
££

A sum sign is added if $( (i,j,\cdots,r) $) is an even permutation of
$( (1,2,\cdots,n) $) and a minus if it's an odd permutation.

In other words, a determinant can the numerical representation of a matrix,
representing how much this matrix modifies the space. (I will not cover the
computation)

## Rank

The rank is defined to be the dimension of the matrix, so a 2 X 2 matrix, that
when represented graphically, the result fills the n dimension.

It's the maximum number of linearly independent columns in A

## Conclusion

As you can see, linear algebra is a very deep branch of mathematics and has
many implementations in the sciences nowadays.

