# Lossless vs. Lossy Compression: How PNG and JPEG Shrink File Sizes

## Why Image Compression Is Necessary
Storing raw uncompressed pixel grids wastes storage and bandwidth. Image formats shrink file sizes using either **lossless compression** (exact bit-for-bit reconstruction) or **lossy compression** (discarding visual details the human eye rarely notices).

## PNG: Lossless Predictive Filtering and DEFLATE
**PNG (Portable Network Graphics)** preserves every pixel value identically:
1. **Delta Filtering:** Instead of storing raw pixel values, PNG predicts each pixel from its left and upper neighbors and stores only the small numerical difference (residual).
2. **DEFLATE Encoding:** A lossless dictionary and Huffman coding algorithm compresses repeated byte patterns.
- **Best For:** Sharp text, UI screenshots, diagrams, and quantized images with flat color regions or transparency.

## JPEG: Lossy Chroma Subsampling and DCT
**JPEG** achieves dramatic file-size reductions on photographs through three lossy steps:
1. **YCbCr Conversion & Chroma Subsampling:** Separates brightness (**luma**, $Y$) from color (**chroma**, $Cb$ and $Cr$), then halves color resolution horizontally and vertically because human eyes detect brightness detail much better than color detail.
2. **Discrete Cosine Transform (DCT):** Splits the image into $8 \times 8$ pixel blocks and converts spatial intensities into low- and high-frequency wave components.
3. **Frequency Quantization:** Divides high-frequency DCT coefficients by a quantization table and rounds small values to zero, discarding subtle textures.
- **Best For:** Natural photographs. Over-compressing sharp edges or text in JPEG causes blurry **ringing artifacts** and visible $8 \times 8$ **blocking artifacts**.

## References & Sources
- **W3C Portable Network Graphics (PNG) Specification:** https://www.w3.org/TR/png/
- **ITU-T Recommendation T.81 (JPEG Digital Compression Standard):** https://www.itu.int/rec/T-REC-T.81