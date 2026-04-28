# AGUI Design System

## About AGUI

AGUI is an AI and automation consulting firm that helps non-technical businesses and individuals adopt AI to improve personal and professional productivity. Their tagline is **"La IA explicada en tu idioma"** — *AI explained in your language* — which captures their core mission: demystifying artificial intelligence and making it accessible.

**Brand Positioning:** AGUI sits at the intersection of human intelligence and advanced technology. Their visual identity concept is **"Inteligencia que Conecta"** — Intelligence that Connects.

**Personality:** Innovative · Intelligent · Interconnected · Agile · Visionary

---

## Sources

- `uploads/ChatGPT Image Feb 27, 2026, 08_24_13 PM.png` — Primary logo (color, light background)
- `uploads/ChatGPT Image Feb 27, 2026, 08_25_25 PM.png` — Primary logo (white, dark background)
- Brand manual provided as text (Manual de Identidad de Marca: AGUI)

No Figma link or codebase was provided. This design system was built from the brand manual and logo assets.

---

## CONTENT FUNDAMENTALS

### Language
- Primary language is **Spanish**. All UI, marketing copy, and communications are in Spanish.
- Secondary language is English (technical docs, international contexts).

### Tone & Voice
- **Approachable but expert.** AGUI speaks plainly — not jargon-heavy — so non-technical people feel welcomed. They are the "translator" between complex AI and real people.
- **Empowering.** Copy focuses on what users *can do* and *achieve*, not on features or technology for its own sake.
- **Direct and confident.** Short sentences. No fluff. Lead with the benefit.
- First person plural ("nosotros") for the brand; second person singular informal ("tú") for the user — keeping it personal and approachable.

### Casing
- Sentence case for all headings and UI labels (not Title Case)
- All-caps only for the brand name "AGUI" and acronyms

### Emoji
- **Not used** in brand materials or UI. The brand is professional and clean.

### Copy Examples (from brand)
- "La IA explicada en tu idioma"
- "Inteligencia que Conecta"
- "Automatizaciones e IA para empresas y personas no técnicas"

---

## VISUAL FOUNDATIONS

### Colors
See `colors_and_type.css` for full CSS variable definitions.

**Primary**
- Cian Vibrante: `#2CD3F2` — Technology & innovation
- Violeta Vibrante: `#A13AEB` — Advanced intelligence & future
- Gris Texto: `#4D5156` — Body text & stability

**Secondary**
- Gris Claro: `#F1F3F4` — Backgrounds, rest areas
- Azul Cobalto: `#1E3A8A` — Depth & professionalism
- Coral Suave: `#F87171` — CTAs & accents

**Gradient:** Cyan → Violet (`#2CD3F2` → `#A13AEB`), always left-to-right or top-to-bottom. This is the brand's most recognizable visual element.

### Typography
Font family: **Inter** (Google Fonts). Clean, modern geometric sans-serif.

- H1: Inter Bold, 48px, `#4D5156`
- H2: Inter SemiBold, 32px, `#4D5156`
- H3: Inter Medium, 24px, `#4D5156`
- Body: Inter Regular, 16–18px, `#4D5156`

Substitution note: Inter is the official brand font per the brand manual.

### Backgrounds
- Default: White `#FFFFFF` or Gris Claro `#F1F3F4`
- Dark surfaces: Azul Cobalto `#1E3A8A` or near-black `#2D2F33`
- Subtle neural-network dot pattern on Gris Claro backgrounds (low opacity, ~5%)
- Headers and cards may use soft cyan→violet gradient overlays

### Cards
- Background: White with subtle box shadow (`0 2px 16px rgba(0,0,0,0.07)`)
- Border radius: 12px
- Optional: thin 1px border `rgba(44,211,242,0.2)` for technology-feel
- No colored left-border accents

### Borders
- Subtle: `1px solid rgba(0,0,0,0.08)` on light backgrounds
- Brand accent: `1px solid rgba(44,211,242,0.3)`

### Shadows
- Card shadow: `0 2px 16px rgba(0,0,0,0.07)`
- Elevated: `0 8px 32px rgba(0,0,0,0.12)`
- No heavy drop shadows

### Corner Radii
- Buttons: 8px
- Cards: 12px
- Large containers/modals: 16px
- Pills/tags: 999px

### Animation
- Easing: `cubic-bezier(0.4, 0, 0.2, 1)` (standard material-style ease)
- Duration: 150ms for micro-interactions, 300ms for page transitions
- Style: Subtle fades + slight upward translate on enter. No bounces. Professional.

### Hover States
- Buttons: slightly darker or gradient-shifted; subtle scale(1.02)
- Links: color shift toward cyan `#2CD3F2`
- Cards: shadow deepens, slight translateY(-2px)

### Press States
- Buttons: scale(0.98) + darken 5%

### Iconography
- Style: Thin-stroke line icons with circular node endpoints — matching the brain isotipo
- No icon font bundled; use Lucide Icons (CDN) as the closest match to the brand's line-icon style
- No emoji as icons
- See ICONOGRAPHY section below

### Imagery
- Minimal, high-resolution photography
- Themes: modern tech interfaces, people collaborating, servers/devices
- Color treatment: subtle cyan→violet gradient overlay to tie into brand
- Depth of field with subject isolation
- Avoid clichéd stock photos

---

## ICONOGRAPHY

The brand's icon style derives from the brain isotipo: **thin strokes, geometric nodes, clean circuits**. Icons should feel like they belong to the same neural-network visual language.

### Icon System
- **Lucide Icons** (https://unpkg.com/lucide@latest) — thin-stroke SVG icons. Best match for AGUI's line-weight and geometric style.
- Usage: `<i data-lucide="brain"></i>` with the Lucide JS loader
- Stroke width: 1.5px to match isotipo weight
- Color: inherits text color or explicit brand colors

### Key Brand Icons (from isotipo)
- Brain/neural motif for AI concepts
- Network nodes for connectivity
- Circuit paths for automation
- Rocket/bolt for speed/agility

### Asset Files
- `assets/logo-color.png` — Logo completo color, fondo transparente (uso principal en fondos claros)
- `assets/logo-white.png` — Logo completo blanco, fondo transparente (fondos oscuros y gradientes)
- `assets/isotipo-color.png` — Solo el cerebro con gradiente cian→violeta (favicon, avatar, app icon)

---

## FILE INDEX

```
README.md                   ← This file; brand overview & guidelines
colors_and_type.css         ← CSS custom properties for colors & typography
SKILL.md                    ← Agent skill definition
assets/
  logo-color.png           ← Logo completo color (fondos claros)
  logo-white.png            ← Logo completo blanco (fondos oscuros)
  isotipo-color.png         ← Cerebro solo, gradiente (favicon, avatar)
preview/
  colors-primary.html       ← Primary color swatches
  colors-secondary.html     ← Secondary & accent colors
  colors-gradient.html      ← Brand gradient
  type-scale.html           ← Typography scale specimen
  type-specimens.html       ← Type style specimens
  components-buttons.html   ← Button components
  components-cards.html     ← Card components
  components-badges.html    ← Badges & tags
  components-inputs.html    ← Form inputs
  spacing-tokens.html       ← Spacing, radius, shadow tokens
  brand-logo.html           ← Logo usage
  brand-pattern.html        ← Neural network pattern
ui_kits/
  web/
    index.html              ← AGUI marketing website prototype
    Header.jsx
    Hero.jsx
    Services.jsx
    Footer.jsx
```
