# Source Summary: Dithering Algorithms

## Source
- Raw article: [04_dithering_error_diffusion.md](../../raw/04_dithering_error_diffusion.md)
- Topic: Ordered dithering and Floyd-Steinberg error diffusion

## Summary
Dithering arranges colors from a limited palette in fine spatial patterns to make gradients appear smoother. The article contrasts threshold-based ordered dithering with Floyd-Steinberg, which distributes each pixel's quantization error to neighboring unprocessed pixels.

## Key Details
- Ordered dithering compares pixel intensity against a repeating Bayer matrix, such as `2 × 2` or `4 × 4`. It is described as fast and as producing a crosshatch texture.
- Floyd-Steinberg quantizes the current pixel, computes `e = original color − palette color`, then distributes error to four neighbors.
- The right, bottom-left, bottom, and bottom-right weights are respectively `7/16`, `3/16`, `5/16`, and `1/16`; the article notes that their sum is `1`.
- The article says this weighting preserves average local brightness without adding colors to the palette.

## Linked Concepts
- [[../concepts/dithering|Dithering]]
- [[../concepts/ordered-dithering|Ordered dithering]]
- [[../concepts/floyd-steinberg|Floyd-Steinberg error diffusion]]
- [[../concepts/color-banding|Color banding]]

## References & Sources
- **Original Paper:** Robert W. Floyd & Louis Steinberg (1976), *"An Adaptive Algorithm for Spatial Greyscale"*, Proceedings of the Society for Information Display, Vol. 17(2), pp. 75–77.
- **IEEE Xplore Digital Library (Bryce E. Bayer, 1973 Ordered Dithering):** https://ieeexplore.ieee.org/
