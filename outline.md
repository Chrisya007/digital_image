# Single-Page Scrapbook Journal Outline

## Node 1: Outline Draft

**Working title:** How Digital Images Work  
**Audience:** Beginners with no prior background in computer graphics or signal processing.  
**Format:** A single, vertically scrolling scrapbook journal with page-like sections, short explanations, hand-drawn-style diagrams, color swatches, and source notes. All technical claims, definitions, formulas, and numbers will be limited to the knowledge base in [wiki/index.md](./wiki/index.md). The five source summaries retain the original references and URLs.

### Page 1 — Cover: A Digital Image, Up Close
- Introduce the topic: pixels, color spaces, quantization, and compression.
- Set up the journal's path from an image grid to color representation, palette reduction, and file compression.
- Visual direction: a simple pixel-grid illustration with a small RGB swatch strip.
- Source note: [wiki/sources/01_pixels_and_bit_depth.md](./wiki/sources/01_pixels_and_bit_depth.md).

### Page 2 — The Image Is a Grid
- Explain raster pixels and spatial resolution as width by height.
- Use the source's `1920 × 1080` example and its pixelation description.
- Introduce bit depth with `2^n`, then connect width, height, and bits per pixel to the uncompressed-size formula.
- Visual direction: a zoomed pixel grid beside a small resolution/bit-depth notebook card.
- Source note: [wiki/sources/01_pixels_and_bit_depth.md](./wiki/sources/01_pixels_and_bit_depth.md).

### Page 3 — Color Has More Than One Address
- Explain a color space as numerical coordinates and compare RGB, HSV, and CIELAB.
- Show RGB's red, green, and blue channels; HSV's hue, saturation, and value; and CIELAB's lightness and opponent axes.
- Include the source's CIELAB `ΔE` formula and explain its role in measuring perceived color difference.
- Visual direction: three labeled color-model cards, with a small set of channel or axis labels.
- Source note: [wiki/sources/02_color_spaces_rgb_hsv_lab.md](./wiki/sources/02_color_spaces_rgb_hsv_lab.md).

### Page 4 — Making a Smaller Palette
- Define color quantization as reducing an image to representative palette colors.
- Walk through the source's K-Means process: convert to CIELAB, initialize centroids, assign pixels, update centroids, iterate, and remap.
- Introduce color banding as a small-palette trade-off.
- Visual direction: a before-and-after palette strip with a compact K-Means step diagram.
- Source note: [wiki/sources/03_color_quantization_kmeans.md](./wiki/sources/03_color_quantization_kmeans.md).

### Page 5 — Dots That Suggest More Colors
- Explain dithering as a way to make gradients appear smoother with a limited palette.
- Contrast ordered dithering's repeating Bayer threshold grid with Floyd-Steinberg error diffusion.
- Show the four Floyd-Steinberg neighbor weights exactly as given in the source.
- Visual direction: a threshold-grid sketch beside a pixel-neighbor diagram with labeled error arrows.
- Source note: [wiki/sources/04_dithering_error_diffusion.md](./wiki/sources/04_dithering_error_diffusion.md).

### Page 6 — Two Ways to Pack an Image
- Contrast lossless PNG with lossy JPEG.
- Summarize PNG's predictive filtering and DEFLATE, then JPEG's YCbCr conversion and chroma subsampling, DCT, and frequency quantization.
- Include the source's suggested use cases and JPEG artifact examples without adding further comparisons.
- Visual direction: paired PNG/JPEG notebook cards with process arrows and the article's use-case labels.
- Source note: [wiki/sources/05_compression_png_vs_jpeg.md](./wiki/sources/05_compression_png_vs_jpeg.md).

### Page 7 — The Image-Making Trail
- Recap the learning path: pixel grid and bit depth; color coordinates; palette reduction; dithering; compression.
- End with a compact glossary of the exact technical terms used in the journal: RGB, HSV, CIELAB, K-Means, Floyd-Steinberg, DEFLATE, and DCT.
- Visual direction: a connected trail of small labeled sketches referring back to the previous pages.
- Source notes: link to all five source summaries in [wiki/index.md](./wiki/index.md).

## Node 2: Review Checkpoint

**Status:** Awaiting review and approval. Do not build `index.html` until the user approves this outline.

**Workflow note:** The current [AGENTS.md](./AGENTS.md) contains Sections 1–2 only; Section 5 and its Node 1/Node 2 instructions are not present. This draft follows the requested Node 1 scope and the outline role described in Section 2. No presentation page has been built.
