---
layout: post
title: "2.6 Introduction to Matrices"
date: 2026-06-30 12:00:00 -0800
categories:
   - machinelearning
---
Eigenvalues and eigenvectors are key players for eigendecomposition and complex transformations necessary for machine learning since it helps reduce the amount of information needed to process. "eigen" is derived from German meaning "inherent", and in this context, "eigenvector" refers to a vector that does not change direction when a linear transformation is applied, therefore, "inherent."

Given a square (n x n) matrix, A, the eigenvector is a non-zero vector with an unchanging direction in response to a linear transformation. Eigenvalues are the scaling factor for the eigenvector. Related terms for eigenvector/value include characteristic vector/value or proper vector/value.

Applying some transformation to an input vector will give an output vector, such that A * v = w, where v is the input vector and w is the output vector. The transformation matrix A, which is used to map one vector onto another, acts like a single scalar. A lambda term, if multiplied by the same input vector, is called the "eigenvalue." This multiplied with the corresponding eigenvector equivalent to output vector w described in the first sentence. This applies if there is a non-zero solution to the A * v = lambda * v, where the solution vector v is the eigenvector corresponding to lambda.

If one multiplies matrix A by vector v, it is the same as multiplying vector v by some scalar lambda. This lambda is the eigenvalue of the matrix A, and vector v is the eigenvector. One may re-write the equation such that it yields a zero vector. Further processing yields an identity matrix where all values in the (n x n) square matrix contains ones in the diagonal and zeros in all other positions.

Calculating eigenvectors and eigenvalues is useful for feature extraction, such as principal component analysis (PCA), a method which reduces a data set to essential dimensions while training an ML model. PCA is an example of "unsupervised ML" because it does not use pre-assigned categories for data.

There are some cases where it is necessary to apply the same matrix multiplication many times, or a "higher power" of a square matrix. The most effective way to calculate these higher powers is to diagonalize A, which entails finding the eigenvalues, eigenvectors, and how they relate to A^n.


