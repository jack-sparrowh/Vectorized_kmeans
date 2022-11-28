# Vectorized_kmeans
Kmeans algorithm using vectorization for fast clustering.

## General informatioin

Algorithm uses vectorized approach for determining the matrix of Euclidead distances between all data points and given cluster centers. \
Let $X \in \mathbb{R}^{m\ \times\ n}$ be the data points with convenction that rows are observations and columns are features. Let $C \in \mathbb{R}^{K\ \times\ n}$ be the matrix of K cluster centers. Given those two we want to determine the Euclidean distances from each point to each cluster center and determine which data point belongs to what cluster center, by finding the closest ones. For this we can use below equation, where diagonal of outer product of $X$ is substituted with Hadamard product, that is much much faster.

$$||X - C||\_{2}^{2} = diag(XX^{T}) + 1\_{n}diag(CC^{T})^{T} - 2XC^{T} = \sum\_{i}(X \circ X)_{ij} + 1\_{n}diag(CC^{T})^{T} - 2XC^{T}$$

Row-wise sum of Hadamard products of $X$ is a column vector, but using numpy library it is broadcasted $\mathbb{R}^{m} \mapsto \mathbb{R}^{m\ \times\ K}$ for summation to be definded. \
$1\_{n}$ is a column vector with n entries.

## Example of use

Here is an example of the algorithm in photo compression. \
(K=16, tol=0.05, time=4.03 s ± 741 ms per loop (mean ± std. dev. of 7 runs, 1 loop each)) \
Photo is taken from: http://openclassroom.stanford.edu/MainFolder/courses/cs229/exercises/ex9/. \
Photo credit: The bird photo used in this project belongs to Frank Wouters.

![bird_large_test](https://user-images.githubusercontent.com/107581485/204329591-b492aeef-e975-4dab-adcf-e5ddde4d1680.png)

Full code for obtaining the same\close results is placed in Vectorized_Kmeans.ipynb
