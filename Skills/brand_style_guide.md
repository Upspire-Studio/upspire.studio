# Upspire Studio Brand & Style Guidelines

This document defines the visual identity, voice, and design principles for Upspire Studio. It is optimized for AI tools to maintain consistency across all outputs.

---

## Brand Identity

### Name
**Upspire Studio**

### Tagline
"Helping leaders turn ideas into experiences that people enjoy using."

### Positioning
Upspire Studio is a consulting practice and holding company that operates at the intersection of strategy, technology, and creative services. We serve mission-driven organizations and leaders who care about impact over scale.

### Brand Personality
- **Thoughtful** — We consider implications before acting
- **Direct** — Clear communication without jargon or hype
- **Curious** — Always exploring, learning, iterating
- **Craftsman-like** — Quality and care in every detail
- **Grounded** — Rooted in community and values

---

## Color Palette

### Primary Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Background | `#fafafa` | 250, 250, 250 | Page backgrounds, light surfaces |
| Text | `#1a1a1a` | 26, 26, 26 | Primary body text, headings |
| Text Muted | `#666666` | 102, 102, 102 | Secondary text, descriptions, labels |
| Accent | `#2d3436` | 45, 52, 54 | Emphasis, decorative elements |
| Border | `#e0e0e0` | 224, 224, 224 | Dividers, card borders, subtle lines |
| Card Background | `#ffffff` | 255, 255, 255 | Cards, elevated surfaces |

### Color Usage Rules
- Use **Text** (`#1a1a1a`) for all primary content
- Use **Text Muted** (`#666666`) for supporting text, descriptions, and labels
- Use **Border** (`#e0e0e0`) for subtle separation between sections
- Avoid bright or saturated colors — the palette is intentionally muted and sophisticated
- Never use pure black (`#000000`) for text

### CSS Variables
```css
:root {
    --color-bg: #fafafa;
    --color-text: #1a1a1a;
    --color-text-muted: #666;
    --color-accent: #2d3436;
    --color-border: #e0e0e0;
}
```

---

## Typography

### Font Families

| Type | Font Stack | Usage |
|------|------------|-------|
| Sans-serif | `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif` | Body text, UI elements, labels |
| Serif | `Georgia, 'Times New Roman', serif` | Headlines, project names, emphasis |

### Type Scale

| Element | Font | Size | Weight | Line Height | Notes |
|---------|------|------|--------|-------------|-------|
| Body | Sans-serif | 17px | 400 | 1.7 | Default paragraph text |
| H1 (Hero) | Serif | clamp(2rem, 5vw, 3rem) | 400 | 1.3 | Main page headline |
| H2 (Section) | Sans-serif | 0.85rem | 600 | — | Uppercase, letter-spacing: 0.1em |
| H3 (Card/Service) | Serif | 1.4rem | 400 | — | Service and card titles |
| Logo | Sans-serif | 1.5rem | 600 | — | Letter-spacing: -0.02em |
| Small Text | Sans-serif | 0.9rem | 400 | — | Footer, captions |
| Links/Tags | Serif | 1.1rem | 400 | — | Project lists, elsewhere links |

### Typography Rules
- **Never use bold serif text** — serif fonts should always be weight 400
- Section headers (H2) are always **uppercase** with wide letter-spacing
- Use serif fonts for **names, titles, and emphasis** — they add warmth
- Use sans-serif for **functional text** — body copy, descriptions, UI
- Maximum line width for body text: **520-600px** for readability

### CSS Variables
```css
:root {
    --font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
    --font-serif: Georgia, 'Times New Roman', serif;
}
```

---

## Spacing & Layout

### Container
- Max width: **800px**
- Horizontal padding: **24px**
- Centered with `margin: 0 auto`

### Section Spacing
| Breakpoint | Padding |
|------------|---------|
| Mobile (<640px) | 60px top/bottom |
| Desktop (≥640px) | 80px top/bottom |

### Component Spacing
| Element | Spacing |
|---------|---------|
| Section header to content | 24px |
| Paragraph spacing | 20px |
| Grid gap (services) | 40px |
| Grid gap (cards) | 24px |
| List item gap | 16px |
| Tag/link gap | 16px vertical, 32px horizontal |

### Grid Layouts
- **Services grid**: 1 column mobile, 2 columns desktop
- **Project cards**: 1 column mobile, 2 columns desktop
- **Tags/links**: Flex wrap with gaps

---

## Components

### Cards
```css
.card {
    padding: 24px;
    background: #fff;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
}

.card:hover {
    border-color: #2d3436;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
}
```

### Links
- **Default**: Text color with subtle bottom border (`#e0e0e0`)
- **Hover**: Border darkens to text color
- **Never use underlines** — use bottom borders instead
- Transition: `0.2s` for smooth state changes

### Lists (Bullet Points)
- Custom bullets: 6px circles in accent color
- Left padding: 20px
- Bullets positioned at `top: 10px` to align with text

### Section Dividers
- Use `border-bottom: 1px solid #e0e0e0` between sections
- Last section has no bottom border

---

## Voice & Tone

### Writing Principles

1. **Direct over clever**
   - Say what you mean clearly
   - Avoid marketing speak and buzzwords
   - No superlatives or hype ("revolutionary", "game-changing")

2. **First person singular**
   - Use "I" not "we" — this is a personal practice
   - Exception: "We" is acceptable when describing collaborative work

3. **Active voice**
   - "I help leaders turn ideas into experiences"
   - Not: "Leaders are helped to turn ideas into experiences"

4. **Concrete over abstract**
   - Specific examples beat vague claims
   - "422K+ subscribers" not "large audience"
   - "From Xbox to ActionSprout" not "major companies"

5. **Honest about limitations**
   - "My goal is to not be engaged any longer than necessary"
   - Acknowledge trade-offs and constraints

### Vocabulary

**Use:**
- Clarity, intention, craft, impact
- Systems thinking, patterns, iteration
- Mission-driven, regenerative, thoughtful
- Build, create, help, empower

**Avoid:**
- Disrupt, revolutionize, game-changing
- Synergy, leverage, optimize (unless technical)
- Best-in-class, world-class, leading
- Passionate (show, don't tell)

### Formatting Conventions

- **Headlines**: Sentence case, no period
- **Descriptions**: Complete sentences with periods
- **Lists**: Parallel structure, consistent punctuation
- **Numbers**: Use numerals for stats (422K, 150,000+)

---

## Imagery & Visual Style

### Photography
- Not currently used on the website
- If added: Natural, candid, warm tones
- Avoid: Stock photo aesthetics, overly polished corporate imagery

### Icons & Graphics
- Minimal use — typography and whitespace carry the design
- If needed: Simple, line-based, monochromatic
- Decorative bullet points: Small circles (6px)

### Whitespace
- Generous whitespace is a feature, not a bug
- Let content breathe
- Resist the urge to fill empty space

---

## Do's and Don'ts

### Do
- Use plenty of whitespace
- Keep typography simple and readable
- Use muted colors consistently
- Write in first person, directly
- Show expertise through specifics, not claims
- Maintain visual hierarchy through type scale
- Use subtle hover states and transitions

### Don't
- Add decorative elements without purpose
- Use bright or saturated colors
- Bold serif text
- Write in marketing-speak
- Crowd the layout
- Use underlines for links (use borders)
- Add animations or motion effects

---

## File Reference

### Current Implementation
- **Website**: `index.html`
- **Styles**: `styles.css`
- **Biography**: `Skills/biography_backstory.md`
- **Brand Guide**: `Skills/brand_style_guide.md` (this file)

### CSS Custom Properties (Full Reference)
```css
:root {
    --color-bg: #fafafa;
    --color-text: #1a1a1a;
    --color-text-muted: #666;
    --color-accent: #2d3436;
    --color-border: #e0e0e0;
    --font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
    --font-serif: Georgia, 'Times New Roman', serif;
    --max-width: 800px;
}
```

---

## AI Implementation Notes

When generating content or designs for Upspire Studio:

1. **Always reference this guide** for colors, typography, and voice
2. **Prioritize readability** over visual complexity
3. **Use the established type hierarchy** — don't invent new sizes
4. **Maintain the muted, sophisticated color palette**
5. **Write in Shawn's voice** — direct, thoughtful, specific
6. **Avoid adding features** not established in the current design
7. **When in doubt, simplify** — less is more

### Quick Reference for AI Tools

```
Background: #fafafa
Text: #1a1a1a
Text Muted: #666666
Border: #e0e0e0
Accent: #2d3436

Body Font: System sans-serif, 17px
Headlines: Georgia serif, weight 400
Section Labels: Sans-serif, 0.85rem, uppercase

Max Width: 800px
Section Padding: 60-80px
```
