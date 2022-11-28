# Vectorized_kmeans
Kmeans algorithm using vectorization for fast clustering.

$$||X - C||\_{2}^{2} = diag(XX^{T}) + 1\_{n}diag(CC^{T})^{T} - 2XC^{T} = \sum\_{i}(X \circ X)_{ij} + 1\_{n}diag(CC^{T})^{T} - 2XC^{T}$$

Here is an example of the algorithm in photo compression.
(K=16, tol=0.05, time=4.03 s ± 741 ms per loop (mean ± std. dev. of 7 runs, 1 loop each)) \
Photo is taken from: http://openclassroom.stanford.edu/MainFolder/courses/cs229/exercises/ex9/. \
Photo credit: The bird photo used in this exercise belongs to Frank Wouters.

![bird_large_test](https://user-images.githubusercontent.com/107581485/204329591-b492aeef-e975-4dab-adcf-e5ddde4d1680.png)
