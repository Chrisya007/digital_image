# Floyd-Steinberg Error Diffusion

Floyd-Steinberg dithering quantizes a pixel to the closest palette color and computes its quantization error as `e = original color − palette color`. It distributes that error to unprocessed neighbors: `7/16` to the right, `3/16` to the bottom-left, `5/16` to the bottom, and `1/16` to the bottom-right. The source article notes that the weights sum to `1` and that average local brightness is preserved without adding palette colors.

## Links
- Source: [[../sources/04_dithering_error_diffusion|Dithering Algorithms]]
- Related: [[dithering|Dithering]], [[ordered-dithering|Ordered dithering]], [[color-quantization|Color quantization]]
