# Design System Document: Modern Zen Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Curated Sanctuary"**

This design system rejects the "fitness app" aesthetic in favor of a high-end editorial experience. It is designed to feel like a premium lifestyle magazine—intimate, quiet, and deeply personal. We break the traditional digital "template" look by utilizing intentional asymmetry, expansive whitespace (the "breath" of the layout), and a typography scale that favors dramatic contrast. 

The goal is to move the user from a state of digital noise to a state of tranquil focus. Every element must feel "placed" rather than "pushed," using overlapping components and varying surface depths to create a sense of physical layering.

---

## 2. Colors & Atmospheric Depth

The palette is rooted in the earth. Warm neutrals provide the foundation, charcoal provides the intellectual weight, and soft clay acts as the human touchpoint.

### Surface Hierarchy & Nesting
To achieve a "Modern Zen" feel, we abandon the concept of flat backgrounds. We treat the UI as stacked sheets of fine, handmade paper.
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Differentiation must be achieved through background shifts. For example, a `surface-container-low` (#f6f3ef) section should sit directly against a `surface` (#fcf9f5) background to create a soft, tectonic shift.
*   **The Glass & Gradient Rule:** For floating elements (like navigation bars or mobile overlays), use Glassmorphism. Apply `surface-container-lowest` (#ffffff) at 80% opacity with a `backdrop-blur` of 20px. 
*   **Signature Textures:** Use a subtle linear gradient for primary CTAs, transitioning from `primary` (#824f3f) to `primary-container` (#9e6756). This adds a "soul" to the buttons that flat color lacks.

### Key Color Tokens
*   **Base:** `surface` (#fcf9f5) - The "paper" of the sanctuary.
*   **Ink:** `on-surface` (#1c1c1a) - Used for high-contrast, editorial serif headings.
*   **Accent:** `primary` (#824f3f) - The "clay" used for intentional calls to action.
*   **Muted:** `secondary` (#5f5e5e) - The "charcoal" used for secondary labels and instructional text.

---

## 3. Typography: The Editorial Voice

The typography is a dialogue between the traditional (Serif) and the modern (Sans-Serif). 

*   **Display & Headlines (Noto Serif):** These are your "hero" moments. Use `display-lg` (3.5rem) with generous letter-spacing (-0.02em) to create an authoritative, premium feel. Headlines should often be center-aligned or intentionally offset to break the grid.
*   **Body & Titles (Manrope):** The sans-serif is the functional "guide." It should be clean, airy, and never crowded. Use `body-lg` (1rem) for general prose with a line-height of 1.6 to ensure the text "breathes."
*   **Labels:** Use `label-md` (0.75rem) in all-caps with 0.1em tracking for category tags or "eyebrow" text above headings.

---

## 4. Elevation & Depth: Tonal Layering

We convey hierarchy through **Tonal Layering** rather than structural lines or heavy shadows.

*   **The Layering Principle:** Depth is achieved by stacking `surface-container` tiers. A card should be `surface-container-lowest` (#ffffff) placed upon a `surface-container-low` (#f6f3ef) background. This creates a "soft lift."
*   **Ambient Shadows:** If a floating element (like a booking modal) requires a shadow, it must be an "Ambient Shadow": 
    *   `box-shadow: 0 20px 40px rgba(28, 28, 26, 0.05);` 
    *   The shadow is a tinted version of `on-surface`, never pure black, ensuring it feels like natural light in a room.
*   **The "Ghost Border":** For input fields or cards where definition is legally or functionally required, use `outline-variant` (#d7c2bd) at **20% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary:** Clay background (`primary`), white text (`on-primary`). Shape: `md` (0.375rem). Padding: `3` (1rem) vertical, `6` (2rem) horizontal.
*   **Tertiary (Editorial Link):** `on-surface` text with a 1px underline using `primary-fixed-dim`. No background. Used for "Read Story" or "View Journal."

### Cards & Content Blocks
*   **Constraint:** Forbid the use of divider lines. 
*   **Style:** Use vertical whitespace (Scale `10` or `12`) to separate content sections. Imagery should use a `DEFAULT` (0.25rem) radius to keep the edges crisp but not sharp.
*   **Asymmetry:** In editorial cards, let the image bleed to one edge while the text sits in a padded `surface-container-highest` box that slightly overlaps the image.

### Inputs
*   **Style:** Minimalist. No background fill. Only a bottom border using `outline-variant` at 40% opacity. When focused, the border transitions to `primary` (#824f3f).

### Signature Component: The "Zen Loader"
*   Instead of a spinning wheel, use a slow-pulsing circular paths using `primary-fixed-dim` (#fab7a3), mimicking a breathing rhythm.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** embrace asymmetry. Allow a heading to start on the second column of a grid while the body text starts on the fourth.
*   **Do** use "Negative Space" as a functional element. If a screen feels "empty," it is likely working.
*   **Do** use high-quality, grain-textured photography with soft natural lighting.

### Don’t:
*   **Don’t** use pure black (#000000). Always use `on-surface` (#1c1c1a) for text to maintain the "warmth" of the brand.
*   **Don’t** use standard "Material Design" shadows. They are too aggressive for this sanctuary.
*   **Don’t** crowd the edges. Keep a minimum page margin of `8` (2.75rem) on desktop to maintain the editorial "frame."
*   **Don't** use "Click Here." Use evocative, active language like "Begin Your Practice" or "Enter the Space."
