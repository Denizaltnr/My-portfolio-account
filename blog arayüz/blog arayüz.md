# Design System Document: The Neural Architect

## 1. Overview & Creative North Star
**Creative North Star: "The Neural Architect"**
This design system is built to reflect the intersection of high-level artificial intelligence and precision engineering. It moves away from the "template" look of standard developer portfolios by embracing an editorial, high-performance aesthetic. We achieve this through **intentional asymmetry**, where content is balanced by negative space rather than rigid grids, and **atmospheric depth**, where the UI feels like a luminous terminal floating in a void.

The goal is to move beyond "Modern Dark Mode" into a space of "Synthetic Precision"—using glassmorphism and glowing accents to suggest a digital environment that is alive, processing, and premium.

## 2. Colors & Surface Philosophy
The palette is rooted in deep, light-absorbing indigos and charcoals, contrasted by "Electric" and "Cyber" accents that simulate bioluminescent data streams.

### Surface Hierarchy & Nesting
To create a high-end feel, we treat the screen as a 3D space. 
- **The "No-Line" Rule:** 1px solid borders for sectioning are strictly prohibited. Boundaries must be defined through background shifts. For example, a project gallery sits in a `surface_container_low` (#131b2e) section against a `surface` (#0b1326) background.
- **Nesting Layers:** Use the `surface_container` tiers to create "nested" depth. 
    - Base Level: `surface_dim` (#0b1326)
    - Section Level: `surface_container_low` (#131b2e)
    - Component/Card Level: `surface_container` (#171f33)
    - Elevated/Floating Level: `surface_container_highest` (#2d3449)

### The "Glass & Gradient" Rule
Standard containers should be replaced with Glassmorphic surfaces for floating elements.
- **Recipe:** Use a semi-transparent `surface_bright` (#31394d) with a `backdrop-blur` of 12px to 20px.
- **Signature Textures:** Apply a linear gradient from `primary` (#c0c1ff) to `secondary` (#5de6ff) at 15% opacity as a subtle background fill for interactive cards to give them a "powered-on" soul.

## 3. Typography
We utilize **Inter** to convey a technical yet sophisticated tone. The hierarchy is designed to feel like a high-end tech journal.

- **Display Scale:** Use `display-lg` (3.5rem) for hero statements. Apply a slight negative letter-spacing (-0.02em) to make it feel "tight" and engineered.
- **The Technical Label:** Use `label-md` or `label-sm` in all-caps with +10% letter-spacing for metadata, categories, and tags. This creates a "system-output" feel that balances the softer `body-lg` text.
- **Contrast:** Pair `headline-lg` (2rem) in `primary_fixed` with `body-md` in `on_surface_variant` (#c7c4d7). The reduced contrast on body text prevents eye strain and emphasizes the "glow" of the headlines.

## 4. Elevation & Depth
Depth is achieved through light and layering, not heavy-handed shadows.

- **The Layering Principle:** Stack `surface_container_lowest` (#060e20) cards on top of `surface_container_low` (#131b2e) backgrounds to create a "sunken" or "embedded" feel.
- **Ambient Shadows:** For floating elements, use a diffuse shadow. 
    - **Color:** `on_primary_fixed_variant` (#2f2ebe) at 8% opacity.
    - **Blur:** 40px to 60px. This mimics the ambient glow of an LED in a dark room.
- **The "Ghost Border":** If a container requires definition, use a 1px border using `outline_variant` (#464554) at **15% opacity**. This creates a "thin glowing border" effect that feels high-performance rather than structural.

## 5. Components

### Buttons
- **Primary:** Use a gradient fill (Electric Blue #00D2FF to Cyber Purple #9D50BB). Apply `rounded-md` (0.75rem). Text should be `on_primary_fixed` (#07006c).
- **Secondary (Glass):** `surface_bright` at 20% opacity with a `ghost border`. 
- **Interaction:** On hover, increase the opacity of the ghost border to 40% and add a subtle 10px outer glow using the `secondary` (#5de6ff) color.

### Cards & Projects
- **No Dividers:** Separate content using the `xl` (1.5rem) spacing scale.
- **Style:** Use `surface_container` with a backdrop blur. Add a single "light leak" in the top-right corner using a very faint gradient of `tertiary` (#edb1ff).

### Input Fields
- **Background:** `surface_container_lowest`.
- **State:** On focus, the `ghost border` transitions from `outline_variant` to a full `secondary` (#5de6ff) glow. 
- **Typography:** Placeholder text should use `label-md` in `outline` (#908fa0).

### Chips (Tags)
- **Style:** Small, pill-shaped (`full` roundedness).
- **Color:** Background `surface_variant` (#2d3449) with `label-sm` text in `primary_fixed_dim`. No border.

### Feature Component: The "Pulse" Loader
For AI-related processing states, use a 2px high horizontal bar using the `secondary` to `tertiary` gradient, with a localized `secondary_fixed` glow that travels across the bar.

## 6. Do's and Don'ts

### Do:
- **Do** use `surface_bright` for subtle highlights on top edges of containers to simulate a light source from above.
- **Do** lean into asymmetrical layouts—place a `display-md` headline on the left and a small `body-sm` description on the far right.
- **Do** use `on_surface_variant` for secondary information to maintain a clear visual hierarchy.

### Don't:
- **Don't** use 100% white (#FFFFFF). Always use `on_background` (#dae2fd) or `primary_fixed` (#e1e0ff) to maintain the cinematic, low-light atmosphere.
- **Don't** use standard shadows. If it looks like a "drop shadow," it's too heavy.
- **Don't** use sharp corners. Everything must use the `md` (0.75rem) or `lg` (1rem) roundedness to feel approachable and modern.
- **Don't** use dividers or lines to separate list items. Use vertical space or alternating `surface_container` subtle shifts.