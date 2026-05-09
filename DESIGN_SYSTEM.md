# BZarq Design System

## Overview

**BZarq** is an architecture studio based in Argentina, founded by two partners:
- **Dylan Zajac**
- **Sebastian Brzezinski**

The studio focuses on three core service pillars:
1. **Obras Nuevas** — New construction projects
2. **Remodelaciones** — Renovation and remodeling
3. **Proyectos** — Architectural design projects

### Project Types
The studio has worked across a wide range of typologies:
- Edificios (Propiedad Horizontal / apartment buildings)
- Locales comerciales (commercial retail spaces)
- Remodelación de viviendas (residential renovations)
- Consultorios (medical/professional offices)

### Brand Positioning
BZarq positions itself as an **architecture studio + real estate development** brand. The tone is sophisticated, minimal, and professional — aimed at high-end clients seeking design excellence and technical quality.

### Sources Provided
- **Logo file:** `uploads/BZARQ_Logo_02_Negro.png` (black wordmark, transparent background, 5761×3241px)
- No codebase, Figma, or existing website provided. Design system built from scratch based on brief and logo analysis.

---

## CONTENT FUNDAMENTALS

### Voice & Tone
- **Sober, professional, and authoritative** — BZarq speaks as expert architects, not salespeople.
- **Spanish-primary** — copy is written in Argentine Spanish (voseo may appear: "contactanos", "conocé nuestros proyectos").
- **Concise and direct** — short sentences, no filler. Less is more.
- **No emoji** — the brand is too refined for emoji in UI contexts.
- **Minimal punctuation ornamentation** — no exclamation marks, no ellipses for effect.

### Casing
- **Headings:** Sentence case or all-caps for short display labels/categories.
- **Navigation:** Title Case or all lowercase (matches the logo which is fully lowercase).
- **CTAs:** Short imperative verbs — "Ver proyectos", "Contactar", "Explorar".

### Copy Examples
- "Arquitectura de calidad. Proyectos que perduran."
- "Obras nuevas, remodelaciones y proyectos en toda la región."
- "Dos socios. Una visión. Resultados que hablan."
- "Conocé nuestro trabajo."
- Category labels: `OBRAS NUEVAS` · `REMODELACIONES` · `PROYECTOS`

### I vs. You
- **We/Nosotros** is used to speak as the studio: "Diseñamos espacios..."
- **Vos/Usted** used sparingly to address the client; informal when present.

---

## VISUAL FOUNDATIONS

### Color Palette
BZarq uses a **monochromatic, minimal palette**. The only brand colors are black, white, and a carefully chosen warm off-white/concrete tone.

| Role | Name | Value |
|---|---|---|
| Black | `--color-black` | `#0A0A0A` |
| Near-black | `--color-ink` | `#1A1A1A` |
| Dark gray | `--color-gray-700` | `#3A3A3A` |
| Mid gray | `--color-gray-400` | `#8A8A8A` |
| Light gray | `--color-gray-200` | `#D4D4D4` |
| Pale gray | `--color-gray-100` | `#EFEFEF` |
| Off-white | `--color-offwhite` | `#F7F5F2` |
| White | `--color-white` | `#FFFFFF` |
| Accent (warm stone) | `--color-accent` | `#C8B99A` |

### Typography
The logo uses a **geometric rounded sans-serif** — closest match is **DM Sans** or **Plus Jakarta Sans** on Google Fonts. Body text uses a clean grotesque. Display text may use a refined serif for editorial contrast.

- **Display / Headlines:** Plus Jakarta Sans, weight 700–800, tight tracking
- **Body:** Plus Jakarta Sans, weight 400–500, normal tracking
- **Labels/Caps:** Plus Jakarta Sans, weight 600, letter-spacing 0.12em, uppercase
- **Accent editorial (optional):** Cormorant Garamond, weight 300–400, for pull-quotes or hero text

### Backgrounds
- Primary: `--color-white` or `--color-offwhite` (#F7F5F2) — clean, warm, concrete-like
- Section dividers: thin `1px` lines in `--color-gray-200`
- Dark sections: `--color-ink` (#1A1A1A) for high-contrast hero or footer blocks
- **No gradients.** No textures. No patterns.
- Photography: Full-bleed architectural photography (b&w or desaturated warm tones preferred)

### Spacing
- Base unit: `8px`
- Scale: 4, 8, 12, 16, 24, 32, 48, 64, 96, 128px
- Section padding: 96–128px vertical
- Content max-width: 1280px

### Borders & Dividers
- `1px solid` lines in `--color-gray-200` used sparingly as section dividers
- No card borders — prefer whitespace and shadow-free separation
- **No box shadows** on cards; separation achieved through background color contrast

### Corner Radii
- UI elements: `0px` (square) — architectural, precise
- Only exception: pill buttons if used (rare), `999px`

### Animation & Motion
- **Fade-in on scroll** — elements appear with `opacity 0 → 1`, `transform: translateY(20px) → 0`
- Duration: `600ms`, easing: `cubic-bezier(0.25, 0.1, 0.25, 1)`
- **No bounces, no spring physics** — everything is measured and controlled
- Hover states: `opacity: 0.75` on images; color transitions `200ms ease`
- No page transitions

### Hover & Press States
- Links: underline appears on hover (not present by default)
- Buttons: background darkens slightly, `transition 200ms`
- Images: subtle `opacity: 0.85` on hover, no scale/zoom

### Imagery
- **Full-bleed architecture photos** — exterior shots, interiors, construction progress
- Color treatment: desaturated, slightly warm/cool neutral — never oversaturated
- B&W photography is preferred for editorial sections
- No stock illustration, no hand-drawn elements

### Cards
- No border, no shadow
- Background: `--color-white` or `--color-offwhite`
- Separation via whitespace + thin line dividers
- Project cards: image top, minimal label + title below

### Layout
- CSS Grid for project galleries
- Flexbox for nav and inline elements
- Asymmetric layouts preferred — e.g. 60/40 splits for hero sections
- Navigation: sticky top bar, full-width, very minimal

### Logo Usage
- Black on white/light backgrounds (primary)
- White version needed for dark backgrounds (to be created)
- Minimum clear space: 1× logo height on all sides
- Never stretch, rotate, or add color

---

## ICONOGRAPHY

BZarq does **not** use a traditional icon set. The brand's architectural minimalism means UI affordances are expressed through:
- **Typography labels** (e.g., "→", "↗" unicode arrows used sparingly as directional cues)
- **Thin-stroke SVG icons** from **Lucide Icons** (CDN-available) when navigation or UI controls require iconography
- Icon style: `stroke-width: 1.5`, no fill, color inherits from text
- Icon size: 20×20px in nav/UI; 24×24px standalone
- **No emoji** in brand contexts

### Available Assets
- `assets/BZARQ_Logo_Negro.png` — Black wordmark on transparent background

---

## FILE INDEX

```
/
├── README.md                          ← This file
├── SKILL.md                           ← Agent skill definition
├── colors_and_type.css                ← CSS variables for color + typography
├── assets/
│   └── BZARQ_Logo_Negro.png          ← Black logo wordmark
├── preview/
│   ├── colors-primary.html           ← Primary color swatches
│   ├── colors-semantic.html          ← Semantic color roles
│   ├── type-display.html             ← Display typography specimen
│   ├── type-body.html                ← Body & label type specimen
│   ├── type-scale.html               ← Full type scale
│   ├── spacing-tokens.html           ← Spacing scale tokens
│   ├── spacing-usage.html            ← Spacing in use
│   ├── logo-brand.html               ← Logo display card
│   ├── components-buttons.html       ← Button states
│   ├── components-nav.html           ← Navigation bar
│   ├── components-cards.html         ← Project cards
│   └── components-forms.html         ← Form inputs
└── ui_kits/
    └── website/
        ├── README.md                  ← Website UI kit notes
        ├── index.html                 ← Interactive website prototype
        ├── Header.jsx                 ← Navigation header component
        ├── Hero.jsx                   ← Hero section component
        ├── ProjectGrid.jsx            ← Project gallery grid
        ├── Footer.jsx                 ← Footer component
        └── Shared.jsx                 ← Shared styles & utilities
```
