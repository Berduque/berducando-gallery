```markdown
# Design System Document: The Nocturnal Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Curated Shadow"**

This design system moves away from the rigid, grid-locked structures of traditional SaaS and towards the fluid, evocative world of high-end art curation. We are not building a dashboard; we are building an immersive digital gallery. The aesthetic relies on the tension between bold, cinematic typography and an expansive "darkspace" that allows imagery to breathe. 

By utilizing intentional asymmetry—such as overlapping image containers and off-center text alignments—we break the "template" look. The interface should feel like a physical publication where depth is felt through tonal shifts rather than seen through borders.

---

## 2. Colors: Tonal Depth & Tactility
The palette is rooted in the "Nocturne" philosophy: a foundation of deep charcoals and blacks, punctuated by high-vibrancy accents that mimic the flash of paint on a dark canvas.

### The Palette
- **Core Dark:** `surface` (#131313) and `surface_container_lowest` (#0e0e0e).
- **The Glow (Accents):** `primary_container` (#ff5733) and `secondary` (#43d7fc). Use these sparingly for high-intent actions.
- **The High Contrast:** `on_background` (#e5e2e1) provides a soft, off-white readability that avoids the harshness of pure #FFFFFF.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. 
Boundaries must be created through:
1.  **Tonal Shifts:** Placing a `surface_container_low` (#1c1b1b) card against a `surface` (#131313) background.
2.  **Negative Space:** Using the `16` (5.5rem) or `20` (7rem) spacing tokens to create a natural visual break.

### Signature Textures & Glass
To add "soul" to the UI, employ **Glassmorphism**. For floating navigation or modal overlays, use `surface_container` with a 60% opacity and a `backdrop-blur` of 20px. This allows the painterly textures of the artwork to bleed through the interface, ensuring the UI feels integrated into the art, not sat on top of it.

---

## 3. Typography: The Editorial Voice
Our typography pairing creates a dialogue between the classic (the artist's hand) and the modern (the digital medium).

*   **The Display (Newsreader):** Used for large-scale storytelling. High-contrast serifs convey authority and elegance. `display-lg` (3.5rem) should be used for hero moments, often with tighter letter-spacing to feel "inked."
*   **The Interface (Manrope/Inter):** For utility. These sans-serifs are clean and invisible, ensuring that when the user is performing a task, the "art" moves to the background.
*   **The Signature (Alegreya Sans SC):** Reserved for specific brand identifiers or labels that require a bespoke, handcrafted feel (inspired by the source brand’s signature style).

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "software-heavy" for this system. We use **Tonal Layering** to imply height.

*   **The Layering Principle:** 
    *   *Base:* `surface` (#131313)
    *   *Mid-ground:* `surface_container_low` (#1c1b1b) for large content blocks.
    *   *Fore-ground:* `surface_container_high` (#2a2a2a) for interactive cards.
*   **Ambient Shadows:** If a floating element (like a context menu) requires a shadow, use a 40px blur with 6% opacity, tinted with the `primary` token (#ffb4a4) rather than black.
*   **The Ghost Border:** For accessibility on inputs, use `outline_variant` (#5b403a) at **15% opacity**. It should be a suggestion of a shape, not a hard cage.

---

## 5. Components

### Buttons
*   **Primary:** A "Glow" variant using a subtle gradient from `primary` to `primary_container`. No borders. Large horizontal padding (`6` / 2rem).
*   **Secondary:** `surface_variant` background with `on_surface` text.
*   **Tertiary:** Text-only, using `label-md` in All Caps with increased letter spacing.

### Cards & Lists
*   **The Forbidden Divider:** Never use horizontal lines to separate list items. Use `2.5` (0.85rem) of vertical padding and a subtle `surface_container_lowest` background on hover.
*   **Editorial Image Containers:** Images should not always be standard aspect ratios. Use the `xl` (0.75rem) roundedness scale, and occasionally allow images to "break" the container bleed for an overlapping, layered look.

### Input Fields
*   **Styling:** Minimalist. Only a bottom "Ghost Border" (15% opacity). Labels use `label-sm` and are always visible to maintain an architectural feel.

### Additional Signature Components
*   **The Immersive Carousel:** A full-bleed image slider where the `display-lg` text overlaps the image, utilizing a `backdrop-blur` on the text container to maintain legibility over complex textures.
*   **Cursor Follower:** A soft, blurred circle of `secondary_fixed_dim` (#43d7fc) at 10% opacity that follows the mouse, adding a tactile, painterly feel to the interaction.

---

## 6. Do’s and Don'ts

### Do
*   **Do** embrace asymmetry. Center-aligning everything feels like a template; off-setting a headline to the left and an image to the right creates "The Curated Shadow" look.
*   **Do** use `darkspace`. If you think there is enough room between elements, add one more level of the spacing scale.
*   **Do** treat typography as an image. Let the large serif headlines be the primary visual driver when photography is absent.

### Don’t
*   **Don’t** use pure #000000 for backgrounds. It kills the depth. Use `surface_container_lowest` (#0e0e0e) for the darkest areas to maintain the "painterly" feel.
*   **Don’t** use high-contrast borders. If the user can see the line clearly, it’s too heavy.
*   **Don’t** rush transitions. Use `cubic-bezier(0.16, 1, 0.3, 1)` for all transforms to ensure the UI feels sophisticated and "liquid."

---
*Document end.*```