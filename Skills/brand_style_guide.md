# Upspire Studio Brand & Style Guidelines

This document defines the visual identity, voice, and design principles for Upspire Studio. It is optimized for AI tools to maintain consistency across all outputs.

---

## Brand Identity

### Name
**Upspire Studio**

### Tagline
"Helping leaders turn ideas into experiences that people enjoy using."

### Positioning
Upspire Studio is a consulting practice and holding company that operates at the intersection of strategy, technology, and creative services. We serve mission-driven organizations and leaders who care about impact over scale. Think of it as an on-call CIO, CTO, and CPO who loves to roll up their sleeves.

### Brand Personality
- **Confident & unhurried** — Doesn't need to oversell. The work speaks.
- **Direct** — Clear communication without jargon or hype
- **Curious** — Always exploring, learning, iterating
- **Craftsman-like** — Quality and care in every detail
- **Grounded** — Rooted in community and values
- **Empowerment over dependency** — The explicit goal is to not be needed forever

---

## The Mark

The Upspire Studio mark is an ascending arc of five nodes — each larger and brighter than the last — tracing a path from bottom-left to top-right. The smallest nodes are obsidian at low opacity; they grow in size and presence until arriving at the apex: a fully-saturated spark (#C5D94B).

The form references generative particle systems (a nod to the generative art practice), progressive momentum, and the act of lifting ideas into reality. The arc is the "spire" in Upspire.

### Mark SVG (canonical)
```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48">
  <path d="M10,40 C14,28 24,20 38,10" fill="none" stroke="#1A1917" stroke-width="0.8" opacity="0.12"/>
  <circle cx="10" cy="40" r="3"   fill="#1A1917" opacity="0.20"/>
  <circle cx="18" cy="33" r="4"   fill="#1A1917" opacity="0.35"/>
  <circle cx="27" cy="24" r="5"   fill="#1A1917" opacity="0.55"/>
  <circle cx="34" cy="17" r="6"   fill="#1A1917" opacity="0.78"/>
  <circle cx="40" cy="9"  r="7.5" fill="#C5D94B"/>
</svg>
```

### Mark on dark backgrounds (white nodes)
```xml
<path ... stroke="white" opacity="0.10"/>
<circle ... fill="white" opacity="0.18"/> <!-- cx=10 -->
<circle ... fill="white" opacity="0.30"/> <!-- cx=18 -->
<circle ... fill="white" opacity="0.50"/> <!-- cx=27 -->
<circle ... fill="white" opacity="0.72"/> <!-- cx=34 -->
<circle cx="40" cy="9" r="7.5" fill="#C5D94B"/> <!-- apex always spark -->
```

### Mark on spark background (dark nodes, full apex)
```xml
<path ... stroke="#1A1917" opacity="0.18"/>
<circle ... fill="#1A1917" opacity="0.18/0.32/0.52/0.75"/>
<circle cx="40" cy="9" r="7.5" fill="#1A1917"/> <!-- apex is full obsidian on spark -->
```

### Minimum sizes
- 40px and above: full 5-node mark with connector arc
- 24px: drop smallest node (cx=10), remove arc
- Favicon/16px: top 3 nodes only

---

## Color Palette

### Primary Colors

| Name | Hex | Usage |
|------|-----|-------|
| Obsidian | `#1A1917` | Primary. Logo, body text, dark surfaces, nav, app icon background |
| Char | `#2E2C2A` | Secondary dark. Cards on dark, elevated surfaces |
| Spark | `#C5D94B` | Accent. Mark apex, CTAs, highlights, active states |
| Dusk | `#74717F` | Secondary text, labels, captions, eyebrows |
| Dusk Light | `#C2C0CC` | Subtle text on dark, reversed secondary |
| Phosphor | `#F2F7D4` | Light spark tint. Hover states, spark-tinted backgrounds |
| Parchment | `#F2EEE6` | Page background. Warm, considered — the default canvas |
| Mid | `#5A5865` | Body text on light backgrounds |
| Muted | `#9A98A4` | Placeholder, disabled, very secondary text |
| White | `#FFFFFF` | Pure white for cards and elevated surfaces |

### Color Usage Rules
- **Parchment** (`#F2EEE6`) is the primary page background — warm and considered
- **Obsidian** (`#1A1917`) for all primary text on light backgrounds
- **Spark** (`#C5D94B`) is a highlight color — use sparingly for maximum impact
- The spark color is chartreuse/yellow-green and pops on both light and dark surfaces
- Never use pure black (`#000000`) for text

### CSS Variables
```css
:root {
    --obsidian:   #1A1917;
    --obsidian-m: #2E2C2A;
    --spark:      #C5D94B;
    --spark-d:    #8A9A2E;
    --spark-l:    #F2F7D4;
    --dusk:       #74717F;
    --dusk-l:     #C2C0CC;
    --parchment:  #F2EEE6;
    --white:      #FFFFFF;
    --mid:        #5A5865;
    --muted:      #9A98A4;
    --rule:       rgba(26,25,23,0.1);
    --color-bg:   #F2EEE6;
    --color-text: #1A1917;
    --color-text-muted: #74717F;
    --color-accent: #C5D94B;
    --color-border: rgba(26,25,23,0.1);
}
```

---

## Typography

### Font Families

| Type | Font | Stack | Usage |
|------|------|-------|-------|
| Serif | Cormorant Garamond | `'Cormorant Garamond', Georgia, 'Times New Roman', serif` | Display, headlines, hero text, editorial moments |
| Sans-serif | Syne | `'Syne', 'Segoe UI', system-ui, sans-serif` | UI, navigation, labels, body, functional text |

Both fonts loaded from Google Fonts:
```html
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400;1,500&family=Syne:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### Type Scale

| Element | Font | Size | Weight | Notes |
|---------|------|------|--------|-------|
| Display | Cormorant Garamond | 56px | 300 | Hero, cover titles |
| H1 | Cormorant Garamond | 36px | 300 | Main page headline |
| H2 (Section) | Syne | 22px | 700 | letter-spacing: -0.02em |
| H3 (Card) | Cormorant Garamond | 20px | 400 | Service and card titles |
| Body | Syne | 15–17px | 400 | line-height: 1.7–1.8 |
| Label / Eyebrow | Syne | 11px | 600 | uppercase, letter-spacing: 0.16em |
| Logo wordmark | Syne | variable | 600 | letter-spacing: -0.02em |

### Typography Rules
- **Never bold serif** — Cormorant Garamond is always weight 300 or 400 (italic adds elegance)
- Section eyebrows/labels: Syne, 11px, uppercase, wide letter-spacing, Dusk color
- H1/hero: Cormorant Garamond light (300), generous line-height (1.0–1.3)
- Maximum body text line width: **520–600px** for readability
- Use `font-style: italic` on Cormorant for editorial warmth

---

## Spacing & Layout

### Container
- Max width: **800px**
- Horizontal padding: **24px** mobile, **48px** desktop
- Centered with `margin: 0 auto`

### Section Spacing
| Breakpoint | Padding |
|------------|---------|
| Mobile (<640px) | 60px top/bottom |
| Desktop (≥640px) | 80px top/bottom |

### Component Spacing
| Element | Spacing |
|---------|---------|
| Section label to content | 24px |
| Paragraph spacing | 20px |
| Grid gap (services) | 40px |
| Grid gap (cards) | 24px |
| List item gap | 16px |

### Grid Layouts
- **Services grid**: 1 column mobile, 2 columns desktop
- **Project cards**: 1 column mobile, 2 columns desktop
- **Tags/links**: Flex wrap with gaps

---

## Components

### Cards
```css
.card {
    padding: 24–32px;
    background: #fff;
    border: 1px solid rgba(26,25,23,0.1);
    border-radius: 12px;
}
.card:hover {
    border-color: #1A1917;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
}
```

### Buttons
| Variant | Background | Text | Border |
|---------|-----------|------|--------|
| Primary | `#1A1917` | `#FFFFFF` | none |
| Accent | `#C5D94B` | `#1A1917` | none |
| Ghost | transparent | `#1A1917` | 1.5px `#1A1917` |

### Pills / Tags
- Obsidian pill: `background: #1A1917; color: #C5D94B` — primary service label
- Spark pill: `background: #F2F7D4; color: #5A6818` — secondary/highlight
- Parchment pill: `background: #F2EEE6; color: #2E2C2A; border: 1px solid rgba(26,25,23,0.12)`

### Section Labels (Eyebrows)
```css
.section-label {
    font-family: var(--f-sans);
    font-size: 11px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #74717F;
    border-bottom: 1px solid rgba(26,25,23,0.1);
    padding-bottom: 10px;
    margin-bottom: 24px;
}
```

---

## Voice & Tone

### Writing Principles

1. **Direct over clever** — Say what you mean. No buzzwords, no superlatives.
2. **First person singular** — Use "I" not "we" — this is a personal practice.
3. **Active voice** — "I help leaders turn ideas into experiences."
4. **Concrete over abstract** — Specific examples beat vague claims. "422K+ subscribers" not "large audience."
5. **Honest about limitations** — "My goal is to not be engaged any longer than necessary."
6. **Confident & unhurried** — Doesn't oversell. The portfolio speaks.

### Vocabulary

**Use:** clarity, intention, craft, impact, systems thinking, patterns, iteration, mission-driven, build, create, help, empower

**Avoid:** disrupt, revolutionize, game-changing, synergy, leverage, best-in-class, passionate (show don't tell)

### Formatting Conventions
- **Headlines**: Sentence case, no period
- **Descriptions**: Complete sentences with periods
- **Lists**: Parallel structure, consistent punctuation
- **Numbers**: Use numerals for stats (422K, 150,000+)

---

## Brand Assets

All brand assets live in the `/brand/` folder.

### File Structure
```
brand/
  source/         SVG source files — authoritative, vector, editable
  png/            PNG exports at production dimensions
  jpg/            JPG exports (social media optimized, 92% quality)
```

### Available Assets

| File | Dimensions | Use |
|------|-----------|-----|
| `source/upspire-mark-transparent.svg` | 800×800 | Mark only, transparent background |
| `source/upspire-favicon-source.svg` | 512×512 | App icon (dark bg, rounded rect) |
| `source/upspire-square-parchment.svg` | 800×800 | Mark on parchment — LinkedIn, profile pics |
| `source/upspire-square-obsidian.svg` | 800×800 | Mark on obsidian — dark mode profile, Instagram |
| `source/upspire-square-spark.svg` | 800×800 | Mark on spark — bold accent variant |
| `source/upspire-lockup-parchment.svg` | 1200×400 | Full logo on parchment — email headers, docs |
| `source/upspire-lockup-obsidian.svg` | 1200×400 | Full logo on dark — dark email, presentations |
| `source/upspire-lockup-spark.svg` | 1200×400 | Full logo on spark — bold variant |
| `source/upspire-og.svg` | 1200×630 | OG / social share card (source) |
| `png/upspire-square-*.png` | 800×800 | PNG squares for social profiles |
| `png/upspire-lockup-*.png` | 1200×400 | PNG lockups |
| `png/upspire-og.png` | 1200×630 | OG share card (also at `/og-image.png`) |
| `jpg/upspire-square-*.jpg` | 800×800 | JPG squares (92% quality) |
| `jpg/upspire-lockup-*.jpg` | 1200×400 | JPG lockups |
| `jpg/upspire-og.jpg` | 1200×630 | JPG OG card |

### Favicon & App Icons

| File | Size | Use |
|------|------|-----|
| `favicon.svg` | scalable | Modern browsers (Chrome, Firefox, Safari) |
| `favicon.ico` | 16+32px | Legacy browsers, default fallback |
| `icons/favicon-16x16.png` | 16×16 | Browser tab fallback |
| `icons/favicon-32x32.png` | 32×32 | Browser tab, taskbar |
| `apple-touch-icon.png` | 180×180 | iOS homescreen, Safari bookmarks |
| `icons/android-chrome-192x192.png` | 192×192 | Android homescreen, PWA |
| `icons/android-chrome-512x512.png` | 512×512 | Android splash screen, PWA |

---

## Do's and Don'ts

### Do
- Use parchment (`#F2EEE6`) as the default page background
- Use spark (`#C5D94B`) sparingly — it carries maximum impact when restrained
- Use Cormorant Garamond for display/hero text, Syne for everything functional
- Use the mark's ascending arc to reinforce the "upspire" idea of lifting/momentum
- Pair the mark with italic serif for editorial warmth
- Use generous whitespace — it's a feature, not a gap to fill
- Write in first person, directly

### Don't
- Bold serif text — Cormorant should always be light or regular weight
- Use saturated or bright colors beyond spark
- Add decorative elements without purpose
- Write in marketing-speak or use superlatives
- Crowd the layout
- Use underlines for links (use bottom-borders instead)
- Change the apex node color — it is always `#C5D94B` (Spark) except on spark backgrounds

---

## File Reference

### Current Implementation
- **Website**: `index.html`
- **Styles**: `styles.css`
- **Mark SVG**: `upspire-mark.svg`
- **Favicon SVG**: `favicon.svg`
- **PWA Manifest**: `site.webmanifest`
- **OG Image**: `og-image.png`
- **Brand Assets**: `brand/`
- **Biography**: `Skills/biography_backstory.md`
- **Brand Guide**: `Skills/brand_style_guide.md` (this file)

### Quick Reference for AI Tools

```
Background:   #F2EEE6  (parchment)
Text:         #1A1917  (obsidian)
Text Muted:   #74717F  (dusk)
Accent:       #C5D94B  (spark — use sparingly)
Border:       rgba(26,25,23,0.1)
Mid text:     #5A5865

Display Font: Cormorant Garamond, weight 300/400, italic for warmth
UI Font:      Syne, weight 400–700
Section Labels: Syne 11px uppercase, letter-spacing 0.16em

Max Width:    800px
Section Padding: 60–80px
Card Radius:  12px

Mark viewBox: 0 0 48 48
Apex node:    cx=40 cy=9 r=7.5 fill=#C5D94B (always)
```
