# Tokens

Official token registry for the Playbook UI system. Use `--{mode}-token-name` where `{mode}` is `light`, `dark`, or `dynamic` based on context. Never use primitive tokens or hardcoded values.

---
## Color

### Text

- `--{mode}-text-primary`: Default body and heading text
- `--{mode}-text-secondary`: Supporting text — metadata, captions, subtitles
- `--{mode}-text-tertiary`: Low-emphasis text — placeholders, timestamps
- `--{mode}-text-status`: White contrast text on utility status-colored badge backgrounds (positive, negative, warning, alert, info)
- `--{mode}-text-inverse`: Text on surfaces that invert between modes — flips white↔black to maintain contrast (e.g. selected chip text in a segmented control)
- `--{mode}-text-disabled`: Text in disabled states
- `--{mode}-text-selected`: Text in selected state (Tabs, Navigation, Toggles)
- `--{mode}-text-unselected`: Text in unselected state (Tabs, Navigation, Segmented controllers, Toggles)
- `--{mode}-text-positive`: Positive/success status text
- `--{mode}-text-positive-hover`: Positive status text on hover
- `--{mode}-text-negative`: Negative/error status text
- `--{mode}-text-negative-hover`: Negative status text on hover
- `--{mode}-text-warning`: Warning status text
- `--{mode}-text-warning-inverse`: Warning text on inverted (dark) surfaces
- `--{mode}-text-warning-hover`: Warning status text on hover
- `--{mode}-text-alert`: Alert/critical status text (Live, Breaking, Updated Now)
- `--{mode}-text-alert-hover`: Alert status text on hover 
- `--{mode}-text-info`: Informational status text
- `--{mode}-text-info-hover`: Informational status text on hover
- `--{mode}-text-link-primary`: Primary hyperlink text
- `--{mode}-text-link-primary-hover`: Primary hyperlink on hover
- `--{mode}-text-link-primary-pressed`: Primary hyperlink on press
- `--{mode}-text-link-secondary`: Secondary hyperlink text — blue, brand-aligned
- `--{mode}-text-link-secondary-hover`: Secondary hyperlink on hover
- `--{mode}-text-link-secondary-pressed`: Secondary hyperlink on press

---

### Surface

- `--{mode}-surface-primary`: Main canvas / page background
- `--{mode}-surface-secondary`: Base background layer beneath the canvas
- `--{mode}-surface-tertiary`: Elevated containers — cards, panels, modals
- `--{mode}-surface-brand`: Brand-colored surface 
- `--{mode}-surface-status-positive`: Background for tinted positive/success states
- `--{mode}-surface-status-negative`: Background for tinted negative/error states
- `--{mode}-surface-status-warning`: Background for tinted warning states
- `--{mode}-surface-status-alert`: Background for tinted alert/critical states
- `--{mode}-surface-status-info`: Background for tinted informational states
- `--{mode}-surface-overlay-solid`: Used behind modals to darken or obscure its content (Modal backdrop)
- `--{mode}-surface-overlay-linear-full`: Darken or obscure the majority of an element (Video controls, Thumbnail, Video cards, Video player, Embed media)
- `--{mode}-surface-overlay-linear-half`: 0% to 50% from the bottom to the middle of the fill (Thumbnail, Video cards, Video player, Embed media)

---

### Utility

- `--{mode}-utility-border`: Default border for dividers and card edges (outline, Stroke)
- `--{mode}-utility-border-hover`: Border color on hover
- `--{mode}-utility-disabled`: Color for disabled UI elements other than text
- `--{mode}-utility-ui-background`: Default background fill for interactive form controls (checkbox, radio button, toggle)
- `--{mode}-utility-ui-background-hover`: UI element background on hover
- `--{mode}-utility-ui-background-disabled`: UI element background in disabled state
- `--{mode}-utility-ui-element-active`: Active/checked/selected state — applied when a form control is activated (e.g. checkbox checked, radio selected, toggle on)
- `--{mode}-utility-icon-primary`: Primary icon color, Used with `text/primary`
- `--{mode}-utility-icon-secondary`: Secondary/supporting icon color, Used with `text/secondary`
- `--{mode}-utility-status-positive`: Graphic color for positive status
- `--{mode}-utility-status-positive-hover`: Positive status icon on hover
- `--{mode}-utility-status-negative`: Graphic color for negative status
- `--{mode}-utility-status-negative-hover`: Negative status icon on hover
- `--{mode}-utility-status-warning`: Graphic color for warning status
- `--{mode}-utility-status-warning-hover`: Warning status icon on hover
- `--{mode}-utility-status-alert`: Graphic color for alert status
- `--{mode}-utility-status-alert-hover`: Alert status icon on hover
- `--{mode}-utility-status-info`: Graphic color for informational status
- `--{mode}-utility-status-info-hover`: Informational status icon on hover

---

### Brand

- `--{mode}-brand-primary`: Brand identity color — shifts per mode to maintain contrast (light: blue, dark/dynamic: white)
- `--{mode}-brand-secondary`: Secondary brand accent, adapts per mode (Blue 60→40→White 80)
- `--{mode}-brand-tertiary`: Tertiary brand tint, adapts per mode (Blue 80→80→White 65)

---

### Elevation

Semantic elevation tokens map directly to complete `box-shadow` values. Apply with `box-shadow`.

- `--{mode}-elevation-raised`: Cards, list items, raised surfaces — maps to Elevation 10
- `--{mode}-elevation-navigation`: Dropdowns, drawers, side panels — maps to Elevation 40
- `--{mode}-elevation-modal`: Modals, toasts, floating toolbars — maps to Elevation 50

---

### Table

- `--{mode}-table-base-background`: Table container background
- `--{mode}-table-base-border-primary`: Primary table border to visually separate header and body
- `--{mode}-table-base-border-secondary`: Secondary border in body row
- `--{mode}-table-header-row-background`: Header row background
- `--{mode}-table-header-text`: Header cell text color
- `--{mode}-table-header-text-hover`: Header cell text on hover
- `--{mode}-table-header-column-background-primary`: Primary header column background
- `--{mode}-table-header-column-background-secondary`: Secondary header column background
- `--{mode}-table-body-row-background-primary`: Odd/primary row background
- `--{mode}-table-body-row-background-secondary`: Even/secondary row background (zebra stripe)
- `--{mode}-table-body-row-background-hover`: Row background on hover
- `--{mode}-table-body-text-primary`: Primary body cell text
- `--{mode}-table-body-text-secondary`: Secondary/supporting body cell text
- `--{mode}-table-body-column-background-active`: Active/sorted column background
- `--{mode}-table-body-column-background-primary`: Primary body column background
- `--{mode}-table-body-column-background-secondary`: Secondary body column background

---

### Button

#### Loading

- `--{mode}-button-loading-background`: Background during loading state
- `--{mode}-button-loading-border`: Border during loading state
- `--{mode}-button-loading-icon-active`: Active dot in the sequential loading indicator
- `--{mode}-button-loading-icon-inactive`: Inactive dots in the sequential loading indicator

#### Disabled

- `--{mode}-button-disabled-background`: Background for all disabled buttons
- `--{mode}-button-disabled-border`: Border for all disabled buttons
- `--{mode}-button-disabled-text`: Text for all disabled buttons

#### Brand

> Reserved for rare brand moments only (e.g. subscribe, upsell). Use Prime for all standard actions.

- `--{mode}-button-brand-background`: Brand button background (default)
- `--{mode}-button-brand-border`: Brand button border (default)
- `--{mode}-button-brand-text`: Brand button text (default)
- `--{mode}-button-brand-background-hover`: Brand button background on hover
- `--{mode}-button-brand-border-hover`: Brand button border on hover
- `--{mode}-button-brand-text-hover`: Brand button text on hover
- `--{mode}-button-brand-background-pressed`: Brand button background on press
- `--{mode}-button-brand-border-pressed`: Brand button border on press
- `--{mode}-button-brand-text-pressed`: Brand button text on press

#### Prime / Primary

> Default button for most actions. Use this unless the context specifically calls for Brand, Destructive, or a lower-emphasis variant.

- `--{mode}-button-prime-primary-background`: Primary action button background (default)
- `--{mode}-button-prime-primary-border`: Primary action button border (default)
- `--{mode}-button-prime-primary-text`: Primary action button text (default)
- `--{mode}-button-prime-primary-background-hover`: Primary action button background on hover
- `--{mode}-button-prime-primary-border-hover`: Primary action button border on hover
- `--{mode}-button-prime-primary-text-hover`: Primary action button text on hover
- `--{mode}-button-prime-primary-background-pressed`: High-emphasis button background on press
- `--{mode}-button-prime-primary-border-pressed`: High-emphasis button border on press
- `--{mode}-button-prime-primary-text-pressed`: High-emphasis button text on press

#### Prime / Secondary

- `--{mode}-button-prime-secondary-background`: Medium-emphasis button background (default)
- `--{mode}-button-prime-secondary-border`: Medium-emphasis button border (default)
- `--{mode}-button-prime-secondary-text`: Medium-emphasis button text (default)
- `--{mode}-button-prime-secondary-background-hover`: Medium-emphasis button background on hover
- `--{mode}-button-prime-secondary-border-hover`: Medium-emphasis button border on hover
- `--{mode}-button-prime-secondary-text-hover`: Medium-emphasis button text on hover
- `--{mode}-button-prime-secondary-background-pressed`: Medium-emphasis button background on press
- `--{mode}-button-prime-secondary-border-pressed`: Medium-emphasis button border on press
- `--{mode}-button-prime-secondary-text-pressed`: Medium-emphasis button text on press

#### Prime / Tertiary

- `--{mode}-button-prime-tertiary-background`: Low-emphasis button background (default)
- `--{mode}-button-prime-tertiary-border`: Low-emphasis button border (default)
- `--{mode}-button-prime-tertiary-text`: Low-emphasis button text (default)
- `--{mode}-button-prime-tertiary-background-hover`: Low-emphasis button background on hover
- `--{mode}-button-prime-tertiary-border-hover`: Low-emphasis button border on hover
- `--{mode}-button-prime-tertiary-text-hover`: Low-emphasis button text on hover
- `--{mode}-button-prime-tertiary-background-pressed`: Low-emphasis button background on press
- `--{mode}-button-prime-tertiary-border-pressed`: Low-emphasis button border on press
- `--{mode}-button-prime-tertiary-text-pressed`: Low-emphasis button text on press

#### Destructive

- `--{mode}-button-destructive-primary-background`: Destructive action button background (default)
- `--{mode}-button-destructive-primary-border`: Destructive action button border (default)
- `--{mode}-button-destructive-primary-text`: Destructive action button text (default)
- `--{mode}-button-destructive-primary-background-hover`: Destructive button background on hover
- `--{mode}-button-destructive-primary-border-hover`: Destructive button border on hover
- `--{mode}-button-destructive-primary-text-hover`: Destructive button text on hover
- `--{mode}-button-destructive-primary-background-pressed`: Destructive button background on press
- `--{mode}-button-destructive-primary-border-pressed`: Destructive button border on press
- `--{mode}-button-destructive-primary-text-pressed`: Destructive button text on press

#### Toggle / Unselected

- `--{mode}-button-toggle-unselected-background`: Toggle button background in unselected state
- `--{mode}-button-toggle-unselected-border`: Toggle button border in unselected state
- `--{mode}-button-toggle-unselected-text`: Toggle button text in unselected state
- `--{mode}-button-toggle-unselected-background-hover`: Unselected toggle background on hover
- `--{mode}-button-toggle-unselected-border-hover`: Unselected toggle border on hover
- `--{mode}-button-toggle-unselected-text-hover`: Unselected toggle text on hover
- `--{mode}-button-toggle-unselected-background-pressed`: Unselected toggle background on press
- `--{mode}-button-toggle-unselected-border-pressed`: Unselected toggle border on press
- `--{mode}-button-toggle-unselected-text-pressed`: Unselected toggle text on press

#### Toggle / Selected

- `--{mode}-button-toggle-selected-background`: Toggle button background in selected state
- `--{mode}-button-toggle-selected-border`: Toggle button border in selected state
- `--{mode}-button-toggle-selected-text`: Toggle button text in selected state
- `--{mode}-button-toggle-selected-background-hover`: Selected toggle background on hover
- `--{mode}-button-toggle-selected-border-hover`: Selected toggle border on hover
- `--{mode}-button-toggle-selected-text-hover`: Selected toggle text on hover
- `--{mode}-button-toggle-selected-background-pressed`: Selected toggle background on press
- `--{mode}-button-toggle-selected-border-pressed`: Selected toggle border on press
- `--{mode}-button-toggle-selected-text-pressed`: Selected toggle text on press

#### Pinned

- `--{mode}-button-pinned-background`: Pinned/saved button background (default)
- `--{mode}-button-pinned-border`: Pinned/saved button border (default)
- `--{mode}-button-pinned-text`: Pinned/saved button text (default)
- `--{mode}-button-pinned-background-hover`: Pinned button background on hover
- `--{mode}-button-pinned-border-hover`: Pinned button border on hover
- `--{mode}-button-pinned-text-hover`: Pinned button text on hover
- `--{mode}-button-pinned-background-pressed`: Pinned button background on press
- `--{mode}-button-pinned-border-pressed`: Pinned button border on press
- `--{mode}-button-pinned-text-pressed`: Pinned button text on press

#### Odds

- `--{mode}-button-odds-background`: Betting odds button background (default)
- `--{mode}-button-odds-border`: Betting odds button border (default)
- `--{mode}-button-odds-text`: Betting odds button text (default)
- `--{mode}-button-odds-background-hover`: Odds button background on hover
- `--{mode}-button-odds-border-hover`: Odds button border on hover
- `--{mode}-button-odds-text-hover`: Odds button text on hover
- `--{mode}-button-odds-background-pressed`: Odds button background on press
- `--{mode}-button-odds-border-pressed`: Odds button border on press
- `--{mode}-button-odds-text-pressed`: Odds button text on press

#### Icon

- `--{mode}-button-icon-background`: Icon button background (default)
- `--{mode}-button-icon-border`: Icon button border (default)
- `--{mode}-button-icon-background-hover`: Icon button background on hover
- `--{mode}-button-icon-border-hover`: Icon button border on hover
- `--{mode}-button-icon-background-pressed`: Icon button background on press
- `--{mode}-button-icon-border-pressed`: Icon button border on press
- `--{mode}-button-icon-icon`: Icon color inside icon button

---

## Rules

- Use only tokens listed above. If a token is missing, flag it — do not invent values.
- Replace `{mode}` with `light`, `dark`, or `dynamic` based on the active `data-mode` context.
- Never reference primitive tokens (e.g. `--white-100`, `--neutral-90`) directly in components.
- Never hardcode hex, rgb, or hsl values.
