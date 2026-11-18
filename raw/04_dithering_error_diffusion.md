# Dithering Algorithms: Simulating Smooth Gradients with Limited Palettes

## The Banding Problem After Quantization
When color quantization reduces an image to a small palette, smooth tonal transitions break into visible stair-step bands (**color banding**). **Dithering** solves this by intentionally scattering pixels of available palette colors in fine spatial patterns so that, from a normal viewing distance, the human eye blends them into intermediate shades.

## Ordered Dithering (Bayer Matrix)
**Ordered dithering** compares each pixel's intensity against a fixed repeating threshold grid called a **Bayer matrix** (such as $2 \times 2$ or $4 \times 4$) before rounding to the nearest palette color. It is computationally fast and produces a distinctive crosshatch texture, making it popular in early computer displays and pixel art.

## Floyd-Steinberg Error Diffusion
**Floyd-Steinberg dithering** produces far more natural photographic gradients by spreading each pixel's rounding error to neighboring unprocessed pixels:
1. Quantize the current pixel $(x, y)$ to its closest color in the limited palette.
2. Compute the **quantization error**: $e = \text{original color} - \text{palette color}$.
3. Distribute fractions of $e$ to four immediate neighbors:
   - Right neighbor $(x+1, y)$ receives $\frac{7}{16} e$
   - Bottom-left neighbor $(x-1, y+1)$ receives $\frac{3}{16} e$
   - Bottom neighbor $(x, y+1)$ receives $\frac{5}{16} e$
   - Bottom-right neighbor $(x+1, y+1)$ receives $\frac{1}{16} e$

Because the weights sum to $\frac{7+3+5+1}{16} = 1$, average local brightness is preserved across the image without adding new colors to the palette.

## References & Sources
- **Original Paper:** Robert W. Floyd & Louis Steinberg (1976), *"An Adaptive Algorithm for Spatial Greyscale"*, Proceedings of the Society for Information Display, Vol. 17(2), pp. 75–77.
- **IEEE Xplore Digital Library (Bryce E. Bayer, 1973 Ordered Dithering):** https://ieeexplore.ieee.org/