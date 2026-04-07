# Color

Playbook UI uses a **neutral-first** palette. Brand blue is reserved for intentional brand moments only. All color must come from semantic tokens — never primitives or hex values.

For the full token list, see `tokens.md`.

---

## Decision Trees

### Mode

```
Page-level (pick one):
│
├─ Standard light UI?                                → data-mode="light"
├─ Standard dark UI?                                 → data-mode="dark"
└─ On other colors?                                  → data-mode="dynamic"

Component-level override (within any page):
│
└─ Component sits on a team color, brand color,
   or image/media background?                        → data-mode="dynamic"
    └─ Apply on that component only.
       The rest of the page mode stays unchanged.
```

### Surface

```
surface-primary is the default — most components live here.

Which surface token?
│
├─ Article section, page panel, or main content area?   → surface-primary  ← default
├─ Page floor visible as a gutter or gap between        → surface-secondary
│   content sections?
├─ Chip, score box, or small container elevated         → surface-tertiary
│   on top of a primary surface?
├─ Modal or dialog box?                                 → surface-tertiary
├─ Subscribe / brand CTA surface?                       → surface-brand
├─ Behind a modal or popover?                           → surface-overlay-solid
├─ Darkening most of an image/video?                    → surface-overlay-linear-full
└─ Subtle fade at the bottom of media?                  → surface-overlay-linear-half
```

### Text

```
Which text token?
│
├─ Headlines, body, labels?              → text-primary
├─ Metadata, timestamps, captions?       → text-secondary
├─ Placeholders, disabled?               → text-tertiary
├─ On a status badge background?         → text-status
├─ Flips contrast between modes?         → text-inverse
│   (e.g. selected chip in segmented control)
└─ Status message inline?                → text-positive / negative / warning / alert / info
```

### Status

```
Which status token?
│
├─ Icon or graphic indicator?            → utility-status-{positive|negative|warning|alert|info}
├─ Tinted background behind status?      → surface-status-{positive|negative|warning|alert|info}
└─ Text inside a status badge?           → text-status (always white)
```

### Button

```
Which button token?
│
├─ Most actions (default)?               → button-prime-primary
├─ Secondary / lower emphasis?           → button-prime-secondary or prime-tertiary
├─ Delete / irreversible action?         → button-destructive-primary
├─ Subscribe / upsell / brand CTA?       → button-brand  ← use sparingly
├─ Disabled state?                       → button-disabled
├─ Save / bookmark?                      → button-pinned
├─ Betting odds?                         → button-odds
└─ Icon only?                            → button-icon
```

### Form Controls

```
Which utility token for form controls?
│
├─ Default (unchecked / unselected / off)?   → utility-ui-background
├─ Hover on default state?                   → utility-ui-background-hover
├─ Checked / selected / on?                  → utility-ui-element-active
└─ Disabled (any state)?                     → utility-ui-background-disabled
```

### Elevation

```
Which elevation token?
│
├─ Card or list item?                    → elevation-raised
├─ Dropdown, drawer, side panel?         → elevation-navigation
└─ Modal, toast, floating toolbar?       → elevation-modal
```

---

## Rules

- **Neutral first** — default to surface-primary / text-primary before reaching for anything else. When both options exist, prefer the neutral variant over the brand-colored one (e.g. `text-link-primary` over `text-link-secondary`)
- **Brand is rare** — `surface-brand` and `button-brand` are for subscribe/upsell only, not general UI
- **Prime is the default button** — always start with `button-prime-primary`, escalate only when needed
- **Never use primitive tokens in components** — `--white-100`, `--neutral-90`, etc. are off-limits
- **Never hardcode hex values**
- **Overlays belong on media** — use linear scrims for images/video, solid overlay for modal backdrops only
- **`text-inverse` is mode-aware** — it flips white↔black to maintain contrast when the surface changes between modes
