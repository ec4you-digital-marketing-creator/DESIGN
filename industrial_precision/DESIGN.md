# Design System Strategy: Industrial Authority

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Industrial Architect."** 

This system moves beyond standard corporate templates to create a digital environment that feels as solid and precise as a manufacturing floor, yet as sophisticated as a high-end editorial journal. We achieve this through a "Monolithic Layout" strategy—using large-scale, high-contrast typography and intentional asymmetry to break the monotony of the standard grid. By overlapping elements and utilizing deep, tonal layering, we communicate power, precision, and unwavering institutional trust.

## 2. Colors: Tonal Depth & The Crimson Anchor
The palette is anchored by a commanding Deep Red, used strategically to draw the eye to key actions and authoritative statements.

*   **Primary Core:** `primary` (#870000) and `primary_container` (#b30000) act as the brand's heartbeat. Use these for high-impact CTAs and semantic highlights.
*   **Neutral Foundation:** The background uses `surface` (#f9f9f9) and `surface_container_lowest` (#ffffff) to maintain a clean, high-trust industrial aesthetic.

### Visual Rules for Surface Integrity:
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Definition must be achieved through background shifts. A `surface_container_low` section sitting against a `surface` background provides all the separation required.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers. A card (`surface_container_lowest`) should sit atop a section background (`surface_container_low`) to create a natural "lift" through color value rather than structural lines.
*   **The "Glass & Gradient" Rule:** For floating headers or overlays (like text on team photos), use Glassmorphism. Apply `surface` at 80% opacity with a `20px` backdrop-blur to allow underlying industrial imagery to bleed through subtly.
*   **Signature Textures:** For Hero sections, use a subtle linear gradient from `primary` to `primary_container` at a 135-degree angle to provide a premium, metallic depth that flat color cannot replicate.

## 3. Typography: Editorial Authority
The typography pairing contrasts a rigid, authoritative heading font with a highly legible, modern sans-serif.

*   **Display & Headlines (Work Sans):** These are the "Lead Headlines." Use `display-lg` (3.5rem) for hero statements. The bold, wide stance of Work Sans conveys industrial strength.
*   **Body & Labels (Inter):** Inter provides the "Technical Specification" feel—precise, neutral, and highly readable.
*   **Hierarchy as Identity:** Use `headline-lg` in `primary` (#870000) for section titles to immediately establish brand presence. Captions and labels should use `label-md` in `on_surface_variant` to provide a subtle, secondary layer of information.

## 4. Elevation & Depth: Tonal Layering
In this design system, shadows are a last resort. Depth is a product of tonal contrast.

*   **The Layering Principle:** Stack `surface-container` tiers. A `surface_container_highest` element on a `surface` background creates immediate focus without visual clutter.
*   **Ambient Shadows:** Where floating elements are required (e.g., a modal or mobile nav), use a "Soft Ambient" shadow: `0px 20px 40px rgba(26, 28, 28, 0.06)`. The shadow color must be a tint of `on_surface` (#1a1c1c), never pure black.
*   **The "Ghost Border" Fallback:** If a container requires a border for accessibility, use the `outline_variant` token at 15% opacity. This creates a "suggestion" of a boundary rather than a hard cage.

## 5. Components

### Cards & Grid Layouts
*   **Industrial Grid:** Use asymmetrical masonry layouts for galleries. Large "Anchor Cards" should span 2 columns, while "Detail Cards" span 1.
*   **Separation:** Forbid the use of divider lines. Use `16` (4rem) spacing from the scale to separate content blocks.
*   **Team Photos:** Images must be treated with a slight desaturation or a consistent color grade. Overlays should use the "Glassmorphism" rule to house names and titles in the bottom-left corner.

### Buttons
*   **Primary:** `primary` (#870000) background with `on_primary` text. Border-radius: `sm` (0.125rem) to maintain a sharp, industrial edge.
*   **Secondary:** `surface_container_highest` background with `on_surface` text. No border.

### Input Fields
*   **Structure:** Use "Underline Only" or "Soft Surface" styles. Avoid the four-sided box. Use `surface_container_high` as the background with a 2px bottom stroke in `primary` only when focused.

### Technical Data Chips
*   **Style:** Use `surface_variant` with `label-sm` text. These should feel like small "part numbers" or metadata tags on an engineering drawing.

## 6. Do's and Don'ts

### Do:
*   **DO** use whitespace as a structural element. Let the content breathe to convey a premium "editorial" feel.
*   **DO** overlap elements (e.g., a title half-sitting on an image) to create a custom, high-end look.
*   **DO** use the `primary` color for emphasis, but keep the majority of the UI in the Neutral Foundation to maintain the "Industrial" trust.

### Don't:
*   **DON'T** use standard 1px borders or heavy drop shadows. They make the UI look like a template.
*   **DON'T** use rounded corners larger than `md` (0.375rem). Soft, circular UI clashes with the "Industrial Architect" North Star.
*   **DON'T** use vibrant blue or green for non-semantic purposes. Stick to the red and neutral palette to protect brand authority.