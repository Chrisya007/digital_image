# Source Summary: Color Quantization and K-Means

## Source
- Raw article: [03_color_quantization_kmeans.md](../../raw/03_color_quantization_kmeans.md)
- Topic: Reducing the number of image colors with K-Means clustering

## Summary
Color quantization reduces an image to a palette of representative colors. The article describes using K-Means in CIELAB: initialize palette centers, assign pixels to their nearest center, update centers from assigned pixels, iterate, and remap pixels to the resulting palette.

## Key Details
- The article describes reducing 16,777,216 possible 24-bit colors to `K` representative colors, with examples `K = 8`, `16`, or `256`.
- K-Means converts pixels to CIELAB, initializes `K` centroids, assigns each pixel by Euclidean distance, updates centroids to the mean of their assigned pixels, repeats until movement is insignificant, and remaps each pixel.
- Small palettes, such as `K = 4` or `K = 8`, can turn smooth gradients into abrupt regions called color banding or posterization.

## Linked Concepts
- [[../concepts/color-quantization|Color quantization]]
- [[../concepts/k-means|K-Means clustering]]
- [[../concepts/color-banding|Color banding]]

## References & Sources
- **scikit-learn Documentation — K-Means Clustering:** https://scikit-learn.org/stable/modules/clustering.html#k-means
- **scikit-image Documentation — Image Processing in Python:** https://scikit-image.org/docs/stable/
