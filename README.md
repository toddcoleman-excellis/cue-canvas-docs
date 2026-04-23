# CUE Canvas — Design System Documentation

Component library and design token reference for **CUE Back Office**, the enterprise B2B SaaS platform built by [Excellis Interactive](https://excellisinteractive.com).

CUE Back Office is a flexible web-based platform used for CRM, catalog management, customer management, warehousing, order management, and other logistics. CUE Canvas is the design system that powers its user interface.

---

## What's in this repo

```
cue-canvas-docs/
├── index.html              — Documentation home / component overview
├── tokens.css              — All CUE Canvas design tokens as CSS custom properties
├── base.css                — Reset, typography, shared layout, and docs styles
├── components/             — Individual component documentation pages
│   └── accordion.html
├── icons/                  — Icon reference page (Material Icons)
└── assets/                 — Static assets
```

---

## Design tokens

All colors, spacing, radii, and typography values are defined as CSS custom properties in `tokens.css`. Every component stylesheet references these tokens rather than hardcoded values, which means the entire UI can be reskinned for a different brand by updating token values in one place.

Token names map directly to variable names in the CUE Back Office Figma source library.

**Example:**
```css
/* Figma: Components/Accordion/bg-accordion */
--bg-accordion: #ffffff;

/* Figma: System/Content/content-body-link */
--content-body-link: #03618d;
```

---

## Icons

CUE Canvas uses **Google Material Icons** (filled style) throughout. Icons are loaded via the Google Fonts CDN:

```html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />
```

Usage pattern:
```html
<!-- Decorative icon — hidden from screen readers -->
<span class="material-icons" aria-hidden="true">add</span>

<!-- Meaningful icon — label lives on the parent interactive element -->
<button aria-label="Expand section">
  <span class="material-icons" aria-hidden="true">expand_more</span>
</button>
```

---

## Spacing

CUE Canvas uses a **4px base grid**. All spacing, padding, and sizing values are multiples of 4.

| Token | Value | Figma |
|-------|-------|-------|
| `--space-xxs` | 2px | Padding-XXS |
| `--space-xs` | 4px | Padding-XS |
| `--space-s` | 8px | Padding-S |
| `--space-m` | 12px | Padding-M |
| `--space-l` | 16px | Padding-L (Default) |
| `--space-xl` | 24px | Padding-XL |
| `--space-xxl` | 28px | Padding-XXL |

---

## Using components

Each component page in `/components` includes:

- **Live rendered example** — interactive in the browser
- **HTML** — semantic, framework-agnostic markup
- **CSS** — styles using CSS custom properties from `tokens.css`
- **JS** — vanilla JavaScript for any interaction, no dependencies
- **Design tokens** — table mapping each CSS variable to its Figma token and usage
- **Accessibility** — ARIA attributes, keyboard patterns, and focus management

Components are framework-agnostic and can be consumed by Angular, React, or any other stack. Advanced interactions use vanilla JavaScript only.

---

## Figma source library

All components and tokens originate from the **CUE Back Office Source Library 2026** Figma file. Designers work in Figma; this documentation reflects the implemented state of those components in code.

---

## Status

This documentation is actively being built out. Component status is indicated on the overview page.

| Status | Meaning |
|--------|---------|
| ✅ Ready | Documented with full HTML, CSS, JS, tokens, and accessibility |
| 🚧 In progress | Being actively documented |
| 🕐 Coming soon | Planned but not yet started |

---

## Built by

**Excellis Interactive** — Business and technology consulting, King of Prussia, PA.  
We build enterprise digital commerce software and custom applications with a foundational commitment to usability and user-centered design.

[excellisinteractive.com](https://excellisinteractive.com)
