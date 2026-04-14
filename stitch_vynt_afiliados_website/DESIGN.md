# Design System Strategy: VYNT Afiliados

## 1. Creative North Star: "The Neon Architect"
The design system is built on the concept of **"The Neon Architect."** It rejects the cluttered, noisy aesthetic of traditional "get rich quick" affiliate programs in favor of a sophisticated, high-performance architectural style. We achieve a "premium startup" feel by treating the interface as a dark, high-tech void where light (Neon Green) is used as a precise tool for navigation and focus.

**The signature shift:** We move away from the "flat box" layout. Instead, we use asymmetrical white space, massive high-impact typography, and a layering system that feels like looking through layers of obsidian and frosted glass.

---

## 2. Color & Tonal Depth
The palette is rooted in absolute depth, using `#0e0e0e` as a canvas to make the Neon Green (`primary`) feel like it’s vibrating.

### The "No-Line" Rule
Traditional 1px borders are strictly prohibited for sectioning. To separate content blocks, use a **Background Shift**:
*   **Hero Section:** `surface` (#0e0e0e)
*   **Secondary Feature Section:** `surface-container-low` (#131313)
*   **Tertiary Content:** `surface-container` (#1a1919)
The transition between these subtle grays creates a sophisticated "editorial" flow that 1px lines cannot match.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack. 
*   **Base:** `surface`
*   **Cards/Containers:** `surface-container-high` (#201f1f) or `surface-container-highest` (#262626)
*   **Hover States:** When a card is engaged, shift its background color one level up the hierarchy (e.g., from `high` to `highest`) rather than adding a border.

### The "Glass & Gradient" Rule
To inject "soul" into the tech aesthetic:
*   **Glassmorphism:** For floating navbars or modals, use `surface-container` at 70% opacity with a `24px` backdrop-blur. 
*   **Signature Gradients:** Use a subtle linear gradient on primary CTAs: `primary` (#8eff71) to `primary-container` (#2ff801). This prevents the neon from looking "flat" and adds a liquid, premium feel.

---

## 3. Typography: The Editorial Edge
The typography system uses **Inter** for structural clarity and **Space Grotesk** for technical utility.

*   **Display (The Hook):** `display-lg` (3.5rem) should be used sparingly for "Hero" statements. Use tight letter-spacing (-0.04em) and `Font-Weight: 800` to create an aggressive, American-startup impact.
*   **Headlines (The Story):** `headline-lg` (2rem) and `md` (1.75rem). These act as the anchors for your sections. Ensure they have significant leading (line-height) to allow the text to "breathe."
*   **Labels (The Data):** All `label-md` and `label-sm` elements must use **Space Grotesk**. The monospaced-adjacent feel of Space Grotesk reinforces the "automation and chatbot" nature of the agency, making data points feel like "code."

---

## 4. Elevation & Depth
Depth is not a shadow; depth is a **Tonal Layer.**

*   **The Layering Principle:** Place `surface-container-lowest` cards on top of a `surface-container-low` section. The slight "dip" in darkness creates a natural, recessed look that feels modern and architectural.
*   **Ambient Shadows:** For "Floating" elements (like a floating conversion card), use a shadow with a `64px` blur, 0px offset, and 6% opacity of the `on-surface` color. It should feel like a soft glow, not a hard drop-shadow.
*   **The "Ghost Border" Fallback:** If a border is required for clarity (e.g., input fields), use the `outline-variant` (#494847) at **15% opacity**. This creates a "suggestion" of a boundary without interrupting the dark-mode immersion.

---

## 5. Component Logic

### Buttons (The "Power" Units)
*   **Primary:** Solid `primary` (#8eff71) with `on-primary` (#0d6100) text. Border-radius: `md` (0.375rem). On hover, add a subtle glow (Box-shadow: 0 0 20px rgba(142, 255, 113, 0.4)).
*   **Secondary:** `Ghost Border` (15% opacity) with `primary` colored text. No background fill.

### Cards (The "Obsidian" Containers)
*   **Styling:** Forbid divider lines within cards. Use `spacing-lg` (vertical white space) to separate the card header from the body.
*   **Interaction:** On hover, a card should scale slightly (1.02x) and the background should shift to `surface-bright`.

### Inputs (The "Command" Line)
*   **Style:** Background: `surface-container-highest`. Border: `none`. 
*   **Focus State:** A 1px bottom-border of `primary` neon green. This mimics a terminal or command-line interface, fitting the "automation" theme.

### Additional Signature Component: The "Profit Tracker" Chip
*   A custom component using `secondary-container` background with `on-secondary-fixed` text. Used to highlight "Lucrative" stats (e.g., "60% Commission"). It should feel like a high-end status pill found in a dashboard.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical layouts. Push a headline to the far left and the body text to the center-right to create "Editorial Tension."
*   **Do** use the `primary` Neon Green only for high-value actions or critical data points. Overusing it will fatigue the user.
*   **Do** ensure all "Glass" elements have a `backdrop-filter: blur(20px)` to maintain readability over background noise.

### Don't:
*   **Don't** use standard #000000 blacks. Use the `surface` (#0e0e0e) for a softer, more professional depth.
*   **Don't** use dividers or horizontal rules. If you feel the need for a line, use white space instead.
*   **Don't** use generic icons. Use thin-stroke (1.5px) geometric icons that match the `outline` color.