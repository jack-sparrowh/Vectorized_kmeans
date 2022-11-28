# Vectorized_kmeans
Kmeans algorithm using vectorization for fast clustering.

$$||X - C||_{2}^{2} = diag(XX^{T}) + 1_{n}diag(CC^{T})^{T} - 2XC^{T} = \sum_{i}(X \circ X)_{ij} + 1_{n}diag(CC^{T})^{T} - 2XC^{T}$$