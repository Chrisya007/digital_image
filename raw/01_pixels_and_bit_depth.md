# Digital Image Anatomy: Pixels, Spatial Resolution, and Bit Depth

## What Is a Digital Image?
A raster digital image is a two-dimensional rectangular grid of tiny picture elements called **pixels**. Unlike continuous physical paintings, digital cameras and screens sample visual scenes at discrete grid coordinates $(x, y)$.

## Spatial Resolution and Aspect Ratio
**Spatial resolution** measures the grid dimensions in width by height (for example, $1920 \times 1080$ pixels, which equals $2,073,600$ total pixels or roughly $2.07$ megapixels). Higher spatial resolution captures finer geometric edges and textures, whereas zooming far into a low-resolution grid reveals visible square blocks known as **pixelation**.

## Bit Depth and Tonal Levels
Each pixel stores numerical intensity values encoded in binary bits. **Bit depth** determines how many distinct brightness steps a single channel can represent using the formula $2^n$, where $n$ is the number of bits:
- **1-bit (Binary):** $2^1 = 2$ tones (pure black `0` or pure white `1`).
- **8-bit Grayscale:** $2^8 = 256$ shades of gray ranging from `0` (black) to `255` (white).
- **24-bit True Color:** Uses three 8-bit channels (Red, Green, and Blue), producing $256 \times 256 \times 256 = 16,777,216$ possible colors.

## Uncompressed Memory Footprint
The raw uncompressed size of an image equals $\text{Width} \times \text{Height} \times \text{Bits Per Pixel}$. For example, an uncompressed $1000 \times 1000$ 24-bit RGB image requires $3,000,000$ bytes (approximately $2.86\text{ MB}$) before any file compression is applied.

## References & Sources
- **MDN Web Docs — Image File Type and Format Guide:** https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Image_types
- **Textbook Reference:** Rafael C. Gonzalez & Richard E. Woods, *Digital Image Processing* (4th ed.), Chapter 2: Digital Image Fundamentals.