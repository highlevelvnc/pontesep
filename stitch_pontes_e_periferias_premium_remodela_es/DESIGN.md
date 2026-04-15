```markdown
# Design System Strategy: High-End Editorial & Technical Precision

## 1. Overview & Creative North Star: "The Architectural Sanctuary"
This design system is built to reflect the precision of high-end engineering and the serenity of a luxury spa. The "Creative North Star" is **The Architectural Sanctuary**. We are not building a utility website; we are curating a digital showroom. 

To achieve this, the design system moves away from "app-like" density. It embraces **intentional asymmetry**, where large editorial type bleeds off-center to create a sense of movement, and **tonal layering**, where depth is felt rather than seen. We prioritize breathing room (white space) as a luxury commodity, ensuring every technical detail—from a pipe fitting to a marble slab—is framed with the authority of a gallery piece.

---

## 2. Colors: Tonal Depth & Accents
The palette is a sophisticated mix of greyscale foundations punctuated by "Petroleum Blue" (`primary`) for technical authority and "Satin Gold" (`secondary`) for premium finishes.

### The "No-Line" Rule
Standard UI relies on borders to separate sections. In this design system, **1px solid borders are strictly prohibited for sectioning.** Transitions must be handled through background shifts:
- A `surface` section transitioning into a `surface-container-low` block.
- Utilizing `surface-container-highest` for high-impact callouts against a `surface` background.

### Surface Hierarchy & Nesting
Think of the UI as a physical stack of premium materials (stone, glass, metal). 
- **Base Level:** `surface` (#fcf9f8).
- **Secondary Level:** `surface-container-low` (#f6f3f2) for subtle grouping.
- **Top Level:** `surface-container-lowest` (#ffffff) for high-contrast "floating" cards that suggest pure cleanliness.

### The "Glass & Gradient" Rule
To evoke the reflective surfaces of high-end bathroom fixtures:
- **Glassmorphism:** Use `surface` colors at 80% opacity with a `backdrop-filter: blur(20px)` for navigation bars and floating modals.
- **Signature Textures:** Use subtle linear gradients from `primary` (#082c31) to `primary-container` (#224247) on hero buttons. This adds a "brushed metal" depth that flat color cannot replicate.

---

## 3. Typography: The Editorial Voice
We utilize a high-contrast pairing to balance technical confidence with contemporary elegance.

- **Display & Headlines (Manrope):** This is our "Authoritative" voice. Use `display-lg` (3.5rem) with tight letter-spacing for hero sections. Headlines should be treated as architectural elements—don't be afraid to use wide margins or left-aligned "staircase" layouts.
- **Body & Labels (Work Sans):** This is our "Technical" voice. It provides clarity and readability. `body-lg` (1rem) is the standard for service descriptions, ensuring a comfortable, premium reading experience.
- **Hierarchy as Identity:** Use `secondary` (#735b20) gold specifically for `label-md` or `title-sm` to highlight "Excellence" or "Premium" markers, creating a visual rhythm of luxury.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "software-heavy" for a luxury renovation brand. We use light and shadow to mimic a physical showroom.

- **The Layering Principle:** Stack `surface-container-lowest` on top of `surface-container-low` to create a "soft lift." The difference in hex codes provides enough contrast to define the edge without a line.
- **Ambient Shadows:** When an element must float (e.g., a high-end project gallery card), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(28, 27, 27, 0.05)`. The shadow color should be a low-opacity version of `on-surface` (#1c1b1b).
- **The "Ghost Border" Fallback:** If a container requires definition against a similar background, use a "Ghost Border": `outline-variant` (#c1c8c9) at 15% opacity. It should be felt, not seen.

---

## 5. Components: The Premium Kit

### Buttons (The "Jewelry" of the UI)
*   **Primary:** Background `primary` (#082c31), text `on-primary`. Use a subtle 2px corner radius (`sm`: 0.125rem) to maintain a sharp, technical look.
*   **Secondary:** Ghost style. No background, `outline` border at 20% opacity, text `primary`. On hover, shift background to `primary-fixed-dim`.
*   **Tertiary:** Text-only in `secondary` (#735b20) with a `full` (9999px) rounded underline on hover.

### Chips & Tags
*   Use `surface-container-high` for technical specifications (e.g., "ISO Certified," "Copper Piping").
*   Use `secondary-container` with `on-secondary-container` text for "Luxury" or "Limited" status indicators.

### Cards & Lists (The "Anti-Grid" Approach)
*   **No Dividers:** Lists must never use horizontal lines. Use 24px - 32px of vertical padding to separate items.
*   **Image Cards:** Images should use the `lg` (0.5rem) rounding scale. Content inside cards should be inset significantly to allow the image to "breathe."

### Input Fields
*   **State:** Use `surface-container-low` as the fill. 
*   **Focus:** Transition the "Ghost Border" to `primary` at 100% opacity. 
*   **Labels:** Always use `label-md` in `on-surface-variant` for a clean, understated look.

---

## 6. Do's and Don'ts

### Do:
- **Use "White Space" as a Material:** Treat empty space as if it were expensive marble. It is a functional part of the design.
- **Asymmetric Balance:** If you have a large image on the right, balance it with a small, high-authority `title-sm` in Gold on the left.
- **Micro-interactions:** Use slow, elegant transitions (300ms - 500ms) for hover states to evoke a sense of calm and luxury.

### Don't:
- **No Heavy Shadows:** Never use `black` or `dark grey` shadows. They make the "cleanliness" of the brand feel "dirty."
- **No Standard Grids:** Avoid the "three-column icon row" trope. Instead, try a staggered list or a single large-scale focus area.
- **No High-Contrast Borders:** Never use a 100% opaque border to separate content. If the background colors are too close, increase the padding rather than adding a line.

### Accessibility Note:
While we utilize "Ghost Borders" and subtle tonal shifts, ensure that interactive elements maintain a 4.5:1 contrast ratio for `on-surface` text. Technical precision must never come at the cost of usability.```