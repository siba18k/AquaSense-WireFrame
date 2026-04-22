```markdown
# Design System Specification: Technical Fluidity

## 1. Overview & Creative North Star
**The Creative North Star: "The Clinical Vanguard"**

This design system transcends standard utility to position water quality monitoring as a high-precision, editorial experience. We are moving away from the "utility dashboard" trope and toward a "digital laboratory" aesthetic. By blending the technical rigor of IoT data with the airy elegance of modern minimalism, we create an environment that feels both authoritative and effortless.

The layout strategy rejects the rigid, boxed-in grids of legacy enterprise software. Instead, we embrace **Intentional Asymmetry** and **Tonal Depth**. By utilizing overlapping layers and extreme typographic contrast, we guide the user’s eye through complex data sets with the grace of a premium broadsheet, ensuring the university’s data feels not just accessible, but vital.

---

## 2. Colors: Tonal Architecture
The palette is rooted in a deep, institutional blue, but its power comes from how we layer its derivatives.

### The "No-Line" Rule
**Traditional 1px borders are strictly prohibited for sectioning.** To define boundaries, designers must use background color shifts. For example, a `surface-container-low` card should sit atop a `surface` background. If you feel the need to draw a line, you haven't used your surface tokens effectively.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of semi-translucent materials.
*   **Base:** `surface` (#f9f9ff)
*   **Structural Sections:** `surface-container-low` (#f2f3fd)
*   **Interactive Cards:** `surface-container-highest` (#e0e2ec)
*   **Floating Elements:** `surface-container-lowest` (#ffffff)

### The "Glass & Gradient" Rule
To evoke a "futuristic IoT" feel, primary actions and hero data visualizations should utilize subtle linear gradients. Transitioning from `primary` (#005bbf) to `primary-container` (#1a73e8) adds a "liquid" soul to the interface. For floating navigation or modals, apply **Glassmorphism**: use a semi-transparent `surface` color with a `24px` backdrop blur to allow the data beneath to bleed through softly.

---

## 3. Typography: The Editorial Tech Scale
We utilize a dual-font strategy to balance technical precision with readability.

*   **Display & Headlines (Space Grotesk):** This is our "Technical Soul." Its geometric construction feels engineered. Use `display-lg` (3.5rem) for hero metrics (e.g., pH levels) to create a bold, "data-as-art" focal point.
*   **Body & Labels (Inter):** Our "Functional Workhorse." Inter provides maximum legibility at small scales for sensor logs and timestamps.
*   **The Contrast Rule:** Use `headline-lg` in `on-surface` (#191c23) immediately adjacent to `body-sm` in `outline` (#727785). This high-contrast scale communicates professional hierarchy without the need for bolding everything.

---

## 4. Elevation & Depth: Tonal Layering
We do not use shadows to create "pop"; we use them to create "atmosphere."

*   **The Layering Principle:** Depth is achieved by stacking. An "Elevated" state is simply a shift from `surface-container-high` to `surface-container-lowest`.
*   **Ambient Shadows:** If a floating element (like a FAB) requires a shadow, it must be an "Ambient Glow." Use a 32px blur, 0px offset, and 6% opacity of the `on-surface` color. It should feel like a soft hum, not a heavy drop-shadow.
*   **The "Ghost Border" Fallback:** If a container must be defined against an identical background, use a `1px` stroke of `outline-variant` at **15% opacity**. It should be felt, not seen.

---

## 5. Components: Precision Primitives

### Buttons
*   **Primary:** Gradient fill (`primary` to `primary-container`), `full` roundedness, no border. Text in `on-primary` (#ffffff).
*   **Tertiary:** No background. Use `title-sm` typography in `primary` color.
*   **State:** On hover/tap, increase the gradient intensity; do not use a dark overlay.

### Data Cards (Primary Component)
*   **Structure:** No dividers. Use `xl` (1.5rem) corner radius. 
*   **Header:** Title in `title-md`, Metric in `display-sm`.
*   **Separation:** Use `surface-container-highest` for the card body and `surface-container-low` for the "footer" or metadata area of the card to create a nested look.

### Status Indicators
*   **Alerts:** Use `tertiary` (#bb1712) for critical failures. Apply a `tertiary-container` (#df3429) soft glow behind the text to signify urgency without the "harshness" of a flat red box.
*   **Safe States:** Use `primary` (#005bbf). Avoid "Success Green" to maintain the signature blue-wash brand identity unless it is a legal requirement.

### Input Fields
*   **Styling:** Minimalist "Underline" style or a subtle `surface-variant` fill. 
*   **Focus:** Transition the `outline` color to `primary` with a 2px stroke. Never use a "glow" around inputs; keep them sharp and clinical.

### Modern IoT Sliders
*   Custom-track sliders using `primary-fixed-dim` for the inactive track and `primary` for the active state. The thumb should be a `surface-container-lowest` circle with an Ambient Shadow.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use extreme white space. If a screen feels "full," remove a container background and use typography to define the space.
*   **Do** use `spaceGrotesk` for all numerical data. Numbers are the stars of this application.
*   **Do** utilize "Tonal Nesting"—a light gray card inside a slightly darker gray section creates a premium, tactile feel.

### Don't:
*   **Don't** use 100% black (#000000). Use `on-surface` (#191c23) to keep the "Technical Fluidity" soft and approachable.
*   **Don't** use standard `0.5rem` rounded corners for large cards. Go bold with `xl` (1.5rem) to emphasize the modern, friendly tech aesthetic.
*   **Don't** use dividers or "HR" lines to separate list items. Use a 16px vertical gap (`spacing-4`) and background color shifts instead.

---
*Director's Final Note: Precision is not the absence of beauty; it is the most refined form of it. Keep the data clinical, but the interface ethereal.*```