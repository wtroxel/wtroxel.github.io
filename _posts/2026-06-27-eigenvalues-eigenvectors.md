---
layout: post
title: "2.6 Eigenvalues and Eigenvectors"
date: 2026-06-27 12:00:00 -0800
categories:
   - machinelearning
---
Eigenvalues and eigenvectors are key players for eigendecomposition and complex transformations necessary for machine learning since it helps reduce the amount of information needed to process. "eigen" is derived from German meaning "inherent", and in this context, "eigenvector" refers to a vector that does not change direction when a linear transformation is applied, therefore, "inherent."

Given a square (n x n) matrix, A, the eigenvector is a non-zero vector with an unchanging direction in response to a linear transformation. Eigenvalues are the scaling factor for the eigenvector. Related terms for eigenvector/value include characteristic vector/value or proper vector/value.

Applying some transformation to an input vector will give an output vector, such that A * v = w, where v is the input vector and w is the output vector. The transformation matrix A, which is used to map one vector onto another, acts like a single scalar. A lambda term, if multiplied by the same input vector, is called the "eigenvalue." This multiplied with the corresponding eigenvector equivalent to output vector w described in the first sentence. This applies if there is a non-zero solution to the A * v = lambda * v, where the solution vector v is the eigenvector corresponding to lambda.

If one multiplies matrix A by vector v, it is the same as multiplying vector v by some scalar lambda. This lambda is the eigenvalue of the matrix A, and vector v is the eigenvector. One may re-write the equation such that it yields a zero vector. Further processing yields an identity matrix where all values in the (n x n) square matrix contains ones in the diagonal and zeros in all other positions.

The following photos show an example of how one would solve for the eigenvalues and eigenvectors of a given 3 x 3 square matrix (shown in the top left).

![CharacteristicPolynomial](/assets/machinelearning/26_1_characteristic_polynomial.png)
Figure 1. Setting up the characteristic polynomials for the matrix to solve for the lambda eigenvalue with the identity matrix I.

![EigenvalueComputation](/assets/machinelearning/26_2_eigenvalue_computation.png)
Figure 2. Computing eigenvalues for a 3x3 square matrix using the Laplace Displacement method. Laplace Displacement method is shown with the number in the top right and the corresponding values in blue.

![CoefficientMatrix](/assets/machinelearning/26_3_coefficient_matrix.png)
Figure 3. Computing the coefficient matrix for the two eigenvalues.

![EigenvectorComputation](/assets/machinelearning/26_4_eigenvector_calculation.png)
Figure 4. Computing eigenvector for the corresponding eigenvalue of lambda = -1. This method for the reduction resembles the workflow used for the Gaussian elimination. The computation of the eigenvector for corresponding eigenvalue of lambda = 2 is left as an exercise for the viewer.

Calculating eigenvectors and eigenvalues is useful for feature extraction, such as principal component analysis (PCA), a method which reduces a data set to essential dimensions while training an ML model. PCA is an example of "unsupervised ML" because it does not use pre-assigned categories for data.

There are some cases where it is necessary to apply the same matrix multiplication many times, or a "higher power" of a square matrix. The most effective way to calculate these higher powers is to diagonalize A, which entails finding the eigenvalues, eigenvectors, and how they relate to A^n. This enables the more straightforward changing of basis for any arbitrary number of matrix multiplications.

In an applied sense, Google PageRank is an algorithm used to prioritize search results on the Google search engine. This is a better alternative than simply showing the page with the same keywords or the most clicks as was done in early search engines. Synonyms for Google PageRank include "link popularity", "link value", "link equity", and "authority." Google PageRank checks how often a given page is linked on other webpages to determine how important it is. If a webpage is more important, then it is likely to receive links from other web pages, because users on those webpages will want other users to redirect towards it.

The most important part of PageRank is to calculate the importance based on the query results, calculate the probability using a range from 0 to 1, and assign the "PageRank" value to every page in the network of pages. The higher the PageRank result, the earlier it appears in the search results. This may be represented via a matrix, known as a "stochastic matrix" or a "probability matrix", where all the values provided are the probability of the link being selected and taking the user to another webpage. For example, if one were to look up CVS Pharmacy, they are likely to get results affiliated with CVS because those CVS links redirect to other CVS links. We can denote the importance using a series of linear equations and finding their solutions, which may be done more quickly using eigenvalues and eigenvectors.
