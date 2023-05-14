+++
title = "Orthogonal Linear Transformation"
description = ""
date = 2023-05-13

[extra]
katex = true
+++

## Requirements

In this post, I will describe several definitions of an orthogonal linear
transformation, so I assume that the reader knows groups and linear algebra, it
doesn't need to be advanced, therefore.

## Introduction

In life, there're many places where symmetry is essential, and in
mathematics a branch that is useful to describe symmetry are the groups,
they're the precise way to describe symmetry

## Symmetry

The Greek roots of the word symmetry mean, roughly, measuring at the same time.
Symmetry is not only a topic of math, it's also in common use in discussions of
art. However, I don't want to consider if a square is more pleasing to the eyes
than a rectangle.

So I want to give a formal description of symmetry, before going to the main
the topic of this post

### Definition(s)

![Triangle symmetry](/13052023202513.png)

If you think the line AB as a mirror, then the left half of the image is the
reflection of the right half. This is an example of bilateral symmetry, each
point P on one side corresponds to a point P', this can be described as

££
\mathbb{R}^2 \rightarrow \mathbb{R}^2 \\\\
(x, y) \rightarrow (-x, y)
££

this carries the figure into itself; that is

££
r(F) = F
££

Have in mind that there're images that the bilateral symmetry does not apply,
as an example, a scalene triangle would not always be symmetric

Another type of symmetry is the rotational kind, that the image or object, is
just rotated on its center, it's easy to see which shapes would fill perfectly
on this kind, squares, equilateral triangles,...

## Orthogonal Linear Transformation

And we reached the main topic, an orthogonal linear transformation, this kind
of transformation is defined by, A linear transformation $\sigma : \mathbb{R}^2
\rightarrow \mathbb{R}^2$, if it is distance preserving, that is, if:

££
|\sigma(U) - \sigma(V)| = |U - V|
££


another way to phrase it is, that for each pair u, v of elements of V, we have:

££
(U, V) = (Tu, Tv)
££

Simplifying, this transformation will keep the distances between points, and
therefore, the angle also will be the same after the transformation, this is
the reason why the name is an orthogonal transformation.

Have in mind that this transformation does not mean that the result will be
symmetric to the original one, the unique thing that, surely, it's the distance
between points and angles, the symmetry would be a subgroup of the orthogonal
group, to be specific it would be:

££
\sigma(F) = F
££

Have in mind that all transformations that were listed in the Symmetry section,
are also orthogonal transformations, since the definition still holds.

An example is:

££
T(x) = \begin{bmatrix}
\cos{\theta} & -\sin{\theta} \\\\
\sin{\theta} & \cos{\theta}
\end{bmatrix}x
££

## References

1. Rotman, Joseph. Galois Theory. Springer Science and Business Media, 1998.
2. Rotman, Joseph J. A First Course in Abstract Algebra: With Applications. Pearson, 2006.
3. Hoffman, Kenneth, and Ray Alden Kunze. Linear Algebra. Prentice Hall, 1971.
