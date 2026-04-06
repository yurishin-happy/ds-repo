# Technical Setup

This document defines the technical environment and implementation standards for the Playbook UI system. AI must strictly follow these configurations when generating code.

## 1. CSS Architecture & Import Order
The color system follows a strict hierarchical dependency. **Primitive tokens must be loaded before semantic tokens.**
The files in `src /` contain the actual CSS variable declarations. Use these variables for all styling instead of hardcoding hex values.

```css
/* Import order in global CSS */
@import './src/color-primitive.css';
@import './src/color-semantic-light.css';
@import './src/color-semantic-dark.css';
@import './src/color-semantic-dynamic.css';
```

## Token Layering Logic

The color system is a two-layer architecture:

| Layer | Sourfce File | Purpose |
|---|---|---|
| Primitive | `src/color-primitive.css` | Raw palette |
| Semantic (light) | `src/color-semantic-light.css` | ALWAYS use in components |
| Semantic (dark) | `src/color-semantic-dark.css` | ALWAYS use in components |
| Semantic (dynamic) | `src/color-semantic-dynamic.css` | ALWAYS use in components |

## Mode switching

The UI adapts to different modes using the data-mode attribute.
- Target: Apply data-mode to the root container or <body>.
- Supported Modes: light, dark, dynamic.
- Mechanism: Apply the `data-mode` attribute to the container element to activate a theme. The CSS selector `[data-mode="light"]`, `[data-mode="dark"]`, and `[data-mode="dynamic"]` scope the semantic tokens automatically.

## How to use tokens in components

Reference semantic tokens via CSS custom properties. Never use raw hex values or primitive tokens.

## Token Naming Convention
All tokens must follow this semantic structure to ensure clarity:
--{mode}-{category}-{subcategory?}-{property}-{state?}


## Component Coding Standards

1. Do's
- Use CSS Custom Properties (var(--token-name)) for all styling.
- Use Tailwind CSS utility classes where applicable, mapping them to design tokens.
- Ensure all components are responsive and follow WCAG AA accessibility standards.
- If a required semantic token is missing in `tokens.md`, pause and ask first. Do not hardcode. 

2. Don'ts
- No Hardcoding: Never use Hex, RGB, or HSL values directly.
- No Primitive Directives: Do not use --white-100 or --blue-60 in component code.
- No Inline Styles: Avoid the style attribute; use CSS classes or Tailwind.