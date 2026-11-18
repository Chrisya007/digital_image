# Source Summary: Digital Image Anatomy

## Source
- Raw article: [01_pixels_and_bit_depth.md](../../raw/01_pixels_and_bit_depth.md)
- Topic: Pixels, spatial resolution, bit depth, and uncompressed memory footprint

## Summary
A raster digital image is a two-dimensional grid of pixels sampled at discrete coordinates. Spatial resolution is the grid's width and height; bit depth determines the number of tonal values a channel can encode. The uncompressed image size depends on width, height, and bits per pixel.

## Key Details
- Spatial resolution is expressed as width by height. The article gives `1920 × 1080` pixels as `2,073,600` pixels, or roughly `2.07` megapixels.
- Bit depth `n` represents `2^n` distinct brightness steps per channel.
- A 1-bit image has two tones; 8-bit grayscale has 256 shades; 24-bit true color uses three 8-bit RGB channels and can represent 16,777,216 colors.
- Uncompressed size is `Width × Height × Bits Per Pixel`. The article's `1000 × 1000` 24-bit RGB example requires `3,000,000` bytes, approximately `2.86 MB`, before compression.
- Enlarging a low-resolution grid can reveal square blocks called pixelation.

## Linked Concepts
- [[../concepts/pixels|Pixels]]
- [[../concepts/spatial-resolution|Spatial resolution]]
- [[../concepts/bit-depth|Bit depth]]
- [[../concepts/uncompressed-memory-footprint|Uncompressed memory footprint]]

## References & Sources
- **MDN Web Docs — Image File Type and Format Guide:** https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Image_types
- **Textbook Reference:** Rafael C. Gonzalez & Richard E. Woods, *Digital Image Processing* (4th ed.), Chapter 2: Digital Image Fundamentals.
