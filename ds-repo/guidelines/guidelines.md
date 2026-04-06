# Playbook UI Design System Guidelines

## Product Context

This is a **Sports media entertainment** product with a **modern, bold, youthful** UI style.
"This guideline serves as the definitive standard for implementing the Playbook UI system using React and Tailwind CSS."

## File Mapping
Design tokens are defined in `tokens.md`, while their corresponding values are implemented in the .css files within the `src/ directpry` (e.g., `src/color-primitives.css`)

- **Density**: Breathable for mobile app — generous whitespace, compact but not cramped, Compact for website - display as much information as possible like a physical newspaper 

- **Surface strategy**: **Layered structure**
    | Layer | Token | Usage |
    |------|-------------|------|
    | Layer 1 | surface-secondary | Bottom - Base Background |
    | Layer 2 | surface-primary | Middle - Canvas |
    | Layer 3 | surface-tertiary | Top - Cards |

- **Mode**:
    | Mode | When to Use |
    |------|-------------|
    | **Light** | Standard light UI |
    | **Dark** | Standard dark UI |
    | **Dynamic** | UI is placed over video players, hero images, or live broadcast backgrounds |
    In Dynamic mode, UI elements must ensure legibility against unpredictable backgrounds using semi-transparent overlays or automatic contrast adjustments.

- **Color palette**: 
    1. **Neutral-First Design**
    2. **Brand Color**: Reserve `surface-brand` strictly to avoid 'Sea of Blue' - use it for subscribe button, or celebration highlights etc
    3. **Semantic Mapping**: Status colors (Positive, Negative, Warning, Alert, Info) must be used semantically
    4. **Translucent tokens** — for overlays only, not primary content

- **Corner style**:
    1. Micro Softness (8px / `border-radius-8`): Use for small, interactive elements (e.g., Badges, Toggles, Chips, Form Fields, Inputs)
    2. Component Softness (12px / `border-radius-12`): Use for medium-sized internal containers (e.g., Panels, Blocks, Inner Sections)
    3. Structural Softness (24px / `border-radius-24`): Use for large layout containers (e.g., Main Cards, Page Sections, Layout Containers)
    4. Full Roundness (9999px / `border-radius-full`): Use for pill-shaped interaction points (e.g., Buttons, Avatars)

## Reading order

**MUST READ before writing any code:**
1. This file (`guidelines.md`) — product character, rules, and workflows
2. `setup.md` — token architecture, CSS import order, and coding standards
3. `tokens.md` - token registry; the complete list of available token names
3. `foundations/` — when and why to use them; decision logic and design intent
4. `components/guidelines.md` — full component catalog before touching any component

**Read on-demand:**
- `components/{name}.md` — read BEFORE using that component
- `composition/` — read when building page layouts or combining components

## Workflows

### Before using a component
1. Check `components/guidelines.md` for the component catalog
2. Read `components/{name}.md` for the specific component
3. Follow all rules, valid props, and usage notes in the guidelines file
4. Do NOT write code using a component until you have read its guidelines file

### Before using an icon
1. Check `icon-discovery.md` for available icons
2. Do NOT guess icon names — verify the icon exists first
3. If an icon doesn't exist, pick a different one and verify

### When building a layout
1. Read `composition/layouts.md` for page structure patterns
2. Read `composition/surfaces.md` for layering and background rules
3. Start with `SidebarNavigation` — every desktop page includes it
4. Apply spacing tokens — never hardcode pixel values

## Rules

- Always use design system components over raw HTML elements (Do not hard code)
- Use bold contrast colors
- All spacing must use design system tokens - never hardcode pixel values
- Complexity is revealed progressively — hide occasional controls behind expand, hover, or click
- Meet WCAG AA requirements - Exceptions: disabled elements, decorative elements, logos