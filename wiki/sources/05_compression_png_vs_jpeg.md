# Source Summary: PNG and JPEG Compression

## Source
- Raw article: [05_compression_png_vs_jpeg.md](../../raw/05_compression_png_vs_jpeg.md)
- Topic: Lossless PNG and lossy JPEG compression

## Summary
Image compression reduces storage and bandwidth needs. PNG is described as lossless, using predictive filtering followed by DEFLATE. JPEG is described as lossy, using YCbCr conversion and chroma subsampling, DCT, and frequency quantization.

## Key Details
- Lossless compression reconstructs the image bit-for-bit; lossy compression discards visual detail.
- PNG predicts pixel values from left and upper neighbors, stores differences (residuals), and compresses repeated byte patterns using DEFLATE.
- The article identifies PNG as suitable for sharp text, UI screenshots, diagrams, and quantized images with flat color regions or transparency.
- JPEG halves color resolution horizontally and vertically after separating luma (`Y`) from chroma (`Cb` and `Cr`).
- JPEG uses DCT on `8 × 8` pixel blocks, then quantizes frequency coefficients; small values are rounded to zero.
- The article identifies JPEG as suitable for natural photographs and notes ringing and `8 × 8` blocking artifacts with over-compression of sharp edges or text.

## Linked Concepts
- [[../concepts/image-compression|Image compression]]
- [[../concepts/png|PNG]]
- [[../concepts/jpeg|JPEG]]

## References & Sources
- **W3C Portable Network Graphics (PNG) Specification:** https://www.w3.org/TR/png/
- **ITU-T Recommendation T.81 (JPEG Digital Compression Standard):** https://www.itu.int/rec/T-REC-T.81
