# K-Means Clustering

The source article uses K-Means to find a palette from an image's pixels. It describes converting pixels to CIELAB, initializing `K` centroids, assigning each pixel to its nearest centroid by Euclidean distance, updating each centroid to the mean of its assigned pixels, repeating until the centroids stop moving significantly, and remapping pixels to their centroid colors.

## Links
- Source: [[../sources/03_color_quantization_kmeans|Color Quantization and K-Means]]
- Related: [[color-quantization|Color quantization]], [[cielab|CIELAB]], [[color-banding|Color banding]]
