# Color Quantization: Reducing Millions of Colors with K-Means Clustering

## What Is Color Quantization?
**Color quantization** is the process of reducing the number of distinct colors in an image—often from $16,777,216$ possible 24-bit colors down to a compact palette of $K$ representative colors (such as $K = 8, 16,$ or $256$)—while keeping the image visually recognizable. It is essential for indexed image formats (like GIF and 8-bit PNG), retro graphics, and textile or yarn pattern generation.

## How K-Means Clustering Selects a Palette
Instead of picking evenly spaced colors that might miss the tones actually present in a photo, **K-Means clustering** finds the optimal $K$ palette colors directly from the image's pixels:
1. **Color Space Conversion:** Convert every pixel from RGB into **CIELAB** space so color distances reflect human visual perception.
2. **Centroid Initialization:** Choose $K$ initial cluster centers (centroids) in the 3D color space.
3. **Pixel Assignment:** Assign every pixel in the image to its nearest centroid using Euclidean distance.
4. **Centroid Update:** Recalculate each centroid as the mean color of all pixels assigned to that cluster.
5. **Iteration:** Repeat steps 3 and 4 until the centroids stop moving significantly.
6. **Remapping:** Replace every original pixel with its assigned centroid color.

## Trade-offs of Small Palettes
When $K$ is very small (for example, $K = 4$ or $K = 8$), smooth sky or skin gradients collapse into flat regions separated by abrupt edges. This visual artifact is known as **color banding** or **posterization**.

## References & Sources
- **scikit-learn Documentation — K-Means Clustering:** https://scikit-learn.org/stable/modules/clustering.html#k-means
- **scikit-image Documentation — Image Processing in Python:** https://scikit-image.org/docs/stable/