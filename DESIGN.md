# Design System Specification: The Clinical Sanctuary

## 1. Overview & Creative North Star
The visual identity for Hangzhou Ya Yi Dental transcends the standard "medical" aesthetic to embrace a concept we call **"The Clinical Sanctuary."** 

In high-end dentistry, trust is built through a balance of clinical precision and hospitality-driven warmth. This design system utilizes a **Sophisticated Minimalist** approach: precise alignment, balanced whitespace, and a "matte" layering technique that mimics high-end materials—brushed steel, muted slate, and cool cyan accents. We are curating a digital environment that feels as grounded and professional as the Hangzhou facility itself.

## 2. Colors & Tonal Architecture
The palette shifts from generic medical blues to a refined, muted spectrum of slate and cyan, executed through depth and subtle tonal shifts.

*   **The "No-Line" Rule:** To maintain a premium, seamless feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined through background color shifts. For example, a `surface-container-low` section should sit directly against a `surface` background derived from our neutral base (#76777a).
*   **Surface Hierarchy & Nesting:** Treat the UI as a physical space. 
    *   Use `surface-container-lowest` for the primary content cards to provide maximum contrast against the muted neutral background. 
    *   Use `surface-container-high` for interactive utility panels. 
    *   Nesting follows a logical "recession"—inner elements should feel like they are resting softly upon their parent containers.
*   **The "Glass & Matte" Rule:** To avoid a "bootstrap" look, use Glassmorphism for floating navigation bars. Use the `surface` color at 70% opacity with a `backdrop-filter: blur(20px)`.
*   **Signature Textures:** Apply a subtle linear gradient to primary actions. Transition from the primary blue (#8fbbe5) to its lighter container variant at a 135-degree angle. This mimics the way light hits a matte medical surface.

## 3. Typography: The Authority of Manrope
We use **Manrope** across all scales. It is a modern sans-serif that balances geometric shapes with organic terminal endings, bridging the gap between "medical tech" and "human warmth."

*   **Display Scale (`display-lg` to `display-sm`):** Reserved for high-impact brand moments. Use these with decreased letter-spacing (-0.02em) to create a tight, editorial feel.
*   **Headline & Title:** These are your "Trust Anchors." Use `headline-md` for section titles. Ensure they have clear margin clearance to maintain the system's "Normal" spacing density (Level 2).
*   **Body & Labels:** `body-lg` is our standard for readability. For dental technicalities or insurance details, use `body-md`. `label-sm` should be reserved for tertiary metadata, always using the `on-surface-variant` to maintain hierarchy.

## 4. Elevation & Depth: Tonal Layering
Depth is achieved through tonal steps rather than heavy shadows, reflecting a clean, dust-free environment.

*   **The Layering Principle:** Stack `surface-container` tiers to create hierarchy. A patient’s dental record should be on `surface-container-lowest`, while the dashboard background remains the base `surface`.
*   **Ambient Shadows:** If an element must float (e.g., a "Book Now" FAB), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(143, 187, 229, 0.08);`. Note the muted blue tint in the shadow to match our primary color (#8fbbe5).
*   **The "Ghost Border" Fallback:** If accessibility requires a container edge, use the `outline-variant` at **15% opacity**.

## 5. Components

### Buttons & Interaction
*   **Primary:** Gradient fill (#8fbbe5 to container), `md` (Level 2) roundedness. No border.
*   **Secondary:** Muted grey-blue (#69798a) background. This provides a professional, non-intrusive alternative.
*   **Tertiary/Ghost:** No background. Use primary (#8fbbe5) text with a subtle underline on hover.

### Input Fields & Controls
*   **Fields:** Use `surface_container_low` as the background fill. Upon focus, transition the background to `surface_container_lowest` and add a 1px "Ghost Border" using the primary color at 40% opacity.
*   **Checkboxes/Radios:** Use Level 2 rounding for checkboxes—avoid sharp 90-degree corners. Use primary for the selected state.

### Cards & Lists
*   **Forbid Dividers:** Do not use horizontal lines between list items. Use Level 2 vertical padding and a subtle background hover state to define rows.
*   **Medical Record Cards:** Use a moderate corner radius (Level 2) for containers to evoke a modern, precise feel.

### Specialized Components
*   **Availability Chips:** Use the secondary palette for "Available" slots and the bright tertiary cyan (#9efaf9) for "Limited" slots. The cyan provides a sense of digital clarity and modern hygiene that aligns with a state-of-the-art clinical environment.
*   **The Treatment Timeline:** A vertical track using `outline_variant` dots and `primary` accents to visualize a patient's journey.

## 6. Do's and Don'ts

### Do
*   **Maintain Balance:** Use Level 2 spacing to ensure the interface feels efficient yet uncrowded.
*   **Tone-on-Tone:** Use the neutral grey palette (#76777a) to create sophisticated background transitions.
*   **Prioritize Legibility:** Ensure `on_surface` text always meets a 4.5:1 contrast ratio against the background tiers.

### Don't
*   **No Heavy Borders:** Never use a 100% opaque `outline` color to box in content.
*   **No High-Saturation Accents:** Stick to the muted primary and secondary tones; avoid bright "safety" blues or reds.
*   **No Pure Black:** Never use #000000. Use the `on_background` derived from our neutral seed to keep the palette soft and medical-grade.