---
layout: post
title: "2.3 Vector Projections and Basis"
date: 2026-04-04 12:00:00 -0800
categories:
   - machinelearning
---
The dot product of vectors is widely used in machine learning algorithms. The dot product of two vectors is determined by multiplying the corresponding elements and taking the sum of them, showing the relationship between the two vectors. The vectors must be the same dimensionality.

If vector a is given by [3,1,4,1,5], and
If vector b is given by [2,7,1,8,2], then

The dot product is determined by taking the sum of the multiplied form of the corresponding vectors such that it follows the general form: a ⋅b = sum(ai * bi)

a⋅b = (3x2) + (1x7) + (4x1) + (1x8) + (5x2) = 35

The dot product is a commutative operation, meaning “a⋅b” and “b⋅a” are equal.
The dot product is distributive over addition, meaning “a⋅(b + c)” = “a⋅b + a⋅c”

If vector c is given by [1,4,1,4,2], then
a⋅(b + c) = a⋅b + a⋅c
  Because a⋅b = (3x2) + (1x7) + (4x1) + (1x8) + (5x2) = 35  
  Because a⋅c = (3x1) + (1x4) + (4x1) + (1x4) + (5x2) = 25  
  Therefore, a⋅(b + c) = a⋅b + a⋅c = 35 + 25 = 60  

Scalar and vector projections are useful to make mathematical operations and machine learning applications easier. The magnitude, also known as a norm or geometric length, is the distance from the tail to the head of a vector. Vector magnitude is indicated with two vertical bars around both sides of a vector, such as \|\|a\|\|.

Vector projection is where we place one vector, vector a, onto another vector, vector b, such that there is an orthogonal projection of a onto b. Orthogonal means perpendicularity, or right angles, relative between two intersecting lines. Calculating the orthogonality of vectors a and b requires a separate formula, where ((a⋅b) / \|\|b\|\|^2) * b. This characterizes how much of vector b acts in the same direction relative to vector a.

![Vector Projection](/assets/machinelearning/vectorprojection.png)
*Figure 1. Comparison between pushing a vehicle from the back, versus from the side, where the force vector is shown in red and the directional vector is shown in blue. The same force applied to a vector off to the side, represented by the red arrow, results in comparatively less force applied along the directional vector shown with the shorter purple arrow.* 

An example of this is trying to push a stalled vehicle from the side versus from behind (Figure 1.2). When pushing from behind, the force vector and car’s directional vector are pointed in the same way. But when pushing from the side, the force vector and the car's directional vector are not pointed in the same way. Therefore, it is worth considering the projection of the red force vector onto the blue directional vector to determine what is the actual force applied on the car in the direction of the blue directional vector.

Given two vectors, solve for the projection of one vector onto the other.
  If vector a is given by [3,1,4,1,5], and
  If vector b is given by [2,7,1,8,2], then

The magnitude of the vectors are given by:
  ||a|| = sqrt((3^2)+(1^2)+(4^2)+(1^2)+(5^2)) = 7.211
  ||b|| = sqrt((2^2)+(7^2)+(1^2)+(8^2)+(2^2)) = 11.045

Problem 1. Calculate the projection of vector a onto vector b
  p1 = ((a⋅b) / (\|\|b\|\|*\|\|b\|\|)) * b is given by:

  (35 / (11.045)^2) * (2) = 0.5738
  (35 / (11.045)^2) * (7) = 2.0083
  (35 / (11.045)^2) * (1) = 0.2869
  (35 / (11.045)^2) * (8) = 2.2952
  (35 / (11.045)^2) * (2) = 0.5738

Therefore, p1 =〈0.5738, 2.0083, 0.2869, 2.2952, 0.5738〉
 	
Problem 2. Calculate the projection of vector b onto vector a
  p2 = ((b⋅a / (\|\|a\|\|*\|\|a\|\|)) * a is given by:

  (35 / (7.211)^2) * (3) = 2.0193
  (35 / (7.211)^2) * (1) = 0.6731
  (35 / (7.211)^2) * (4) = 2.6924
  (35 / (7.211)^2) * (1) = 0.6731
  (35 / (7.211)^2) * (5) = 3.3655

Therefore, p2 = 〈2.0193, 0.6731, 2.6924, 0.6731, 3.3655〉

Another aspect of machine learning is changing vectors from one coordinate system to another coordinate system, or the changing basis from one to another. Every vector can be defined by a combination of basis vectors, which are one unit long on the horizontal and vertical axes. Any vector in space can be written as a combination of two vectors.

Basis vectors have two key conditions to meet:
  1. The set of vectors spans the vector space, the set of vectors that can be manipulated by scalars and subject to associative, commutative, and additive laws
  2. Linear independence from each other, meaning that one cannot create a new basis vector by multiplying it with a scalar, so every vector contributes uniquely to vector space

Every vector in the vector space can be built from elements of a spanning set using addition and scalar multiplication. A span is the set of all linear combinations of vectors in a subset. Imagine X is a subset of a vector space V. The span of X is the set of all linear combinations of vectors in X, and is denoted by sp(X). The span of most pairs of 2D vectors is all of 2D space, unless they are aligned in the same direction, at which point the span is all vectors whose tail shares a common point on the 2D coordinate plane.

![Vector Span](/assets/machinelearning/vectorspan.png)
*Figure 2. Three examples of a linear combination of two vectors within vector space. Black, red, and green are the original vectors while the orange, blue, and pink are the span of their linear combinations. Notably, all of 2D space is accessible with these vectors.*

In the above example, there are three example vectors in a vector space with two vectors spanning it. There are an infinite number of combinations one may use for the two vectors, but one may only combine two. For vectors to form a basis, they do not need unit vectors and they do not necessarily have to be orthogonal as shown in the case above. They just need to satisfy the linear independence requirement and be part of the vector set.

