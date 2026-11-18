# Source Summary: Color Models Compared

## Source
- Raw article: [02_color_spaces_rgb_hsv_lab.md](../../raw/02_color_spaces_rgb_hsv_lab.md)
- Topic: Color spaces RGB, HSV, and CIELAB

## Summary
A color space represents colors as numerical coordinates. RGB describes additive light used by screens and sensors; HSV reorganizes the RGB cube around hue, saturation, and value; CIELAB represents lightness and opponent color axes and is described as perceptually uniform.

## Key Details
- RGB channel values in the article range from `0` to `255`; combinations illustrate primary colors, black, and white.
- RGB Euclidean distance does not necessarily match how different colors look to people.
- HSV uses hue (`0°` to `360°`), saturation (`0%` to `100%`), and value (`0%` to `100%`).
- CIELAB uses `L*` for lightness (`0` black to `100` diffuse white), `a*` for green-to-red, and `b*` for blue-to-yellow.
- The article gives the Euclidean color difference formula: `ΔE = √((ΔL*)² + (Δa*)² + (Δb*)²)` and says it reliably measures perceived color differences in CIELAB.

## Linked Concepts
- [[../concepts/color-space|Color space]]
- [[../concepts/rgb|RGB]]
- [[../concepts/hsv|HSV]]
- [[../concepts/cielab|CIELAB]]

## References & Sources
- **W3C CSS Color Module Level 4 (Lab and LCH Color Spaces):** https://www.w3.org/TR/css-color-4/
- **International Commission on Illumination (CIE):** https://cie.co.at/
