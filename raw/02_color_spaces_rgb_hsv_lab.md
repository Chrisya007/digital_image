# Color Models Compared: RGB, HSV, and Perceptual CIELAB Space

## Why Multiple Color Spaces Exist
A **color space** is a mathematical coordinate system that represents colors as tuples of numbers. Different tasks require different geometries: displays emit light, humans describe paint by hue and brightness, and algorithms need distances that match human vision.

## RGB (Red, Green, Blue)
**RGB** is an **additive color model** built for hardware screens and camera sensors. Every pixel combines red, green, and blue light intensities from `0` to `255`:
- `(255, 0, 0)` produces pure red; `(0, 255, 0)` produces pure green; `(0, 0, 255)` produces pure blue.
- `(0, 0, 0)` produces black (no light), while `(255, 255, 255)` produces white (full light).
- **Limitation:** Euclidean distance in RGB does not match human perception. Two colors can have the same numerical distance in RGB while looking nearly identical or wildly different to the human eye.

## HSV (Hue, Saturation, Value)
**HSV** rearranges the RGB cube into a cylindrical model aligned with human intuition:
- **Hue ($H$):** The color type measured around a circle from $0^\circ$ to $360^\circ$ ($0^\circ$ red, $120^\circ$ green, $240^\circ$ blue).
- **Saturation ($S$):** Color purity from $0\%$ (gray) to $100\%$ (vivid pigment).
- **Value ($V$):** Brightness from $0\%$ (black) to $100\%$ (full brightness).

## CIELAB ($L^*a^*b^*$)
**CIELAB** was designed by the International Commission on Illumination (CIE) to be **perceptually uniform**:
- **$L^*$:** Lightness from `0` (black) to `100` (diffuse white).
- **$a^*$:** Green-to-red opponent axis (negative values are green, positive values are red).
- **$b^*$:** Blue-to-yellow opponent axis (negative values are blue, positive values are yellow).
Because CIELAB is perceptually uniform, the straight-line Euclidean distance $\Delta E = \sqrt{(\Delta L^*)^2 + (\Delta a^*)^2 + (\Delta b^*)^2}$ reliably measures how different two colors look to a human observer, making CIELAB ideal for color clustering and quantization.

## References & Sources
- **W3C CSS Color Module Level 4 (Lab and LCH Color Spaces):** https://www.w3.org/TR/css-color-4/
- **International Commission on Illumination (CIE):** https://cie.co.at/