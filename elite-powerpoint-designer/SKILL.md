---
name: elite-powerpoint-designer
description: Create world-class PowerPoint presentations with professional design, consistent branding, sophisticated animations, and polished visual hierarchy. Use when users request presentations, slide decks, pitches, reports, or want to convert markdown to professionally designed PowerPoint with Apple/Microsoft/Google-level quality.
---

# Elite PowerPoint Designer

Transform content into world-class presentations with the design quality of Apple keynotes, Microsoft product launches, and Google I/O.

## Core Design Philosophy

1. **Minimalism First** - Remove everything that doesn't serve a clear purpose
2. **Bold & Clear** - Large typography, high contrast, confident colors
3. **Visual Hierarchy** - Guide attention through size, color, and spacing
4. **Consistent Branding** - Every element follows the design system
5. **Purposeful Motion** - Animations only where they add clarity

## Brand Styles

**1. Tech Keynote (Apple/Tesla Style)**
- Colors: Deep blacks, whites, accent blue (#0071E3)
- Typography: SF Pro Display (72-96pt title)
- Style: Minimalist, premium, product-focused

**2. Corporate Professional (Microsoft/IBM Style)**
- Colors: Navy (#003366), steel blue (#0078D4)
- Typography: Segoe UI (54-72pt title)
- Style: Trustworthy, data-driven, enterprise-ready

**3. Creative Bold (Google/Airbnb Style)**
- Colors: Bright primaries, gradients
- Typography: Montserrat (64-84pt title)
- Style: Energetic, innovative, design-forward

**4. Financial Elite (Goldman Sachs/McKinsey Style)**
- Colors: Charcoal (#2C3E50), gold accent (#D4AF37)
- Typography: Garamond (serif, elegant)
- Style: Sophisticated, authoritative

**5. Startup Pitch (Y Combinator Style)**
- Colors: High contrast black/white with brand accent
- Typography: Inter or Roboto
- Style: Energetic, data-driven, founder-friendly

## Workflow

1. **Analyze Content & Select Style** — Match content type to brand style
2. **Parse Content & Map to Templates** — Detect slide types from markdown structure
3. **Apply Design System** — Typography hierarchy, spacing, color application
4. **Apply Professional Polish** — Transitions (1-2 types max), animations
5. **Consistency Validation** — Font, color, spacing, alignment checks

## Animation Rules

**Tier 1: Always Safe**
- Fade (0.6s), Push (0.4s), Morph (0.8s)

**Tier 2: Use Sparingly**
- Zoom (0.5s), Reveal (0.6s)

**Tier 3: Avoid**
- Ferris Wheel, Curtains, Dissolve, Origami — Never use

## Quality Checklist

- [ ] All slides use design system colors
- [ ] Typography follows hierarchy (max 4 font sizes)
- [ ] One main idea per slide
- [ ] No "walls of text" (max 6 lines body)
- [ ] Transitions consistent (1-2 types only)
- [ ] No distracting motion

## Requirements

**MCP Server:** Office-PowerPoint-MCP-Server
```bash
npx @smithery/cli install @gongrzhe/office-powerpoint-mcp-server
pip install python-pptx pillow pyyaml
```
