# OurCoordinates - Brand Design System

## Brand Overview

OurCoordinates sells personalized GPS coordinates jewelry. Customers choose a meaningful place - where they met, got engaged, took that trip - and the exact coordinates are hand-engraved onto premium bracelets and necklaces. The brand occupies the space between personal storytelling and luxury accessories.

**Brand Voice:** Premium, emotional, personal, nostalgic luxury.
**Tagline Concept:** Every place tells a story. Wear yours.

---

## Color Palette

### Primary Colors

| Token             | Hex       | Usage                                      |
|-------------------|-----------|--------------------------------------------|
| `--bg`            | `#0a0a0a` | Near-black background, primary canvas      |
| `--surface`       | `#1a1a1a` | Elevated dark surface, cards, overlays      |
| `--gold`          | `#d4af37` | Rich gold, primary accent, CTA highlights  |
| `--gold-muted`    | `#bfa265` | Muted gold, secondary accent, borders      |
| `--text-primary`  | `#f5f0e8` | Cream/bone white, primary readable text    |
| `--text-dim`      | `#b8b0a4` | Dimmed cream, secondary/caption text       |

### Extended Palette

| Token             | Hex       | Usage                                      |
|-------------------|-----------|--------------------------------------------|
| `--gold-glow`     | `rgba(212,175,55,0.15)` | Soft radial glow behind elements |
| `--gold-bright`   | `#e8c84a` | Bright gold for animated highlights        |
| `--warm-overlay`  | `rgba(212,175,55,0.08)` | Warm tint for nostalgia scenes  |
| `--shadow-deep`   | `rgba(0,0,0,0.7)` | Deep shadow for depth layers          |

### Usage Rules

- Background is always `#0a0a0a` - never pure black (`#000000`)
- Gold accents should appear on no more than 30% of any frame
- Cream text on dark background provides the primary contrast
- Muted gold for supporting elements, rich gold for focal points
- Radial gold glows behind key product imagery for premium feel

---

## Typography

### Font Stack

#### Display - Playfair Display (Italic)
- **Role:** Headlines, hero text, emotional statements
- **Weights:** 400 (Regular Italic), 700 (Bold Italic)
- **Style:** Always italic for this brand
- **Sizing:** 48-96px for hero, 36-48px for section headers
- **Letter-spacing:** -0.02em for headlines, normal for subheads
- **Line-height:** 1.1 for large display, 1.3 for smaller

```css
@font-face {
  font-family: 'Playfair Display';
  src: url('capture/assets/fonts/nuFRD-vYSZviVYUb_rj3ij__anPXDTnCjmHKM4nYO7KN_qiTbtY.ttf') format('truetype');
  font-weight: 400;
  font-style: italic;
}

@font-face {
  font-family: 'Playfair Display';
  src: url('capture/assets/fonts/nuFRD-vYSZviVYUb_rj3ij__anPXDTnCjmHKM4nYO7KN_k-UbtY.ttf') format('truetype');
  font-weight: 700;
  font-style: italic;
}
```

#### Body - Inter
- **Role:** Body copy, descriptions, UI text, supporting labels
- **Weights:** 300 (Light), 400 (Regular), 500 (Medium)
- **Style:** Normal (upright)
- **Sizing:** 16-24px for body, 14-16px for captions
- **Letter-spacing:** 0.01em for body, 0.08em for uppercase labels
- **Line-height:** 1.5 for body, 1.3 for labels

```css
@font-face {
  font-family: 'Inter';
  src: url('capture/assets/fonts/UcCO3FwrK3iLTeHuS_nVMrMxCp50SjIw2boKoduKmMEVuOKfMZg.ttf') format('truetype');
  font-weight: 300;
  font-style: normal;
}

@font-face {
  font-family: 'Inter';
  src: url('capture/assets/fonts/UcCO3FwrK3iLTeHuS_nVMrMxCp50SjIw2boKoduKmMEVuLyfMZg.ttf') format('truetype');
  font-weight: 400;
  font-style: normal;
}

@font-face {
  font-family: 'Inter';
  src: url('capture/assets/fonts/UcCO3FwrK3iLTeHuS_nVMrMxCp50SjIw2boKoduKmMEVuI6fMZg.ttf') format('truetype');
  font-weight: 500;
  font-style: normal;
}
```

#### Brand Accent - RM Neue (Italic)
- **Role:** Brand name, accent phrases, coordinates text, special callouts
- **Weights:** 300 (Light Italic), 600 (SemiBold Italic), 700 (Bold Italic)
- **Style:** Always italic
- **Sizing:** 20-40px for accent phrases, 14-18px for coordinates
- **Letter-spacing:** 0.04em for coordinates display, normal for accent text
- **Line-height:** 1.2

```css
@font-face {
  font-family: 'RM Neue';
  src: url('capture/assets/fonts/RMNeue-LightItalic.woff2') format('woff2');
  font-weight: 300;
  font-style: italic;
}

@font-face {
  font-family: 'RM Neue';
  src: url('capture/assets/fonts/RMNeue-SemiBoldItalic.woff2') format('woff2');
  font-weight: 600;
  font-style: italic;
}

@font-face {
  font-family: 'RM Neue';
  src: url('capture/assets/fonts/RMNeue-BoldItalic.woff2') format('woff2');
  font-weight: 700;
  font-style: italic;
}
```

### Typography Hierarchy

| Level    | Font              | Weight | Size   | Color          |
|----------|-------------------|--------|--------|----------------|
| Hero     | Playfair Display  | 700i   | 72-96px| `--text-primary` |
| Headline | Playfair Display  | 400i   | 48-60px| `--text-primary` |
| Subhead  | RM Neue           | 600i   | 28-36px| `--gold`         |
| Body     | Inter             | 400    | 18-22px| `--text-primary` |
| Caption  | Inter             | 300    | 14-16px| `--text-dim`     |
| Coords   | RM Neue           | 300i   | 16-20px| `--gold-muted`   |
| CTA      | Inter             | 500    | 20-28px| `--bg` on gold   |

---

## Component Styles

### Buttons / CTA

- Background: `--gold` with subtle gradient to `--gold-muted`
- Text: `--bg` (dark text on gold background)
- Font: Inter 500, 18-24px, uppercase, letter-spacing 0.06em
- Border-radius: 2px (nearly square, premium feel)
- Padding: 16px 40px
- Hover/active: brightness(1.1) with subtle scale(1.02)

### Product Cards

- Background: `--surface` with 1px border `rgba(212,175,55,0.2)`
- Image: full-bleed with object-fit cover
- Text overlay: gradient from transparent to `rgba(10,10,10,0.9)`
- Caption: Inter 300, cream text below image

### Coordinates Display

- Font: RM Neue 300 Italic
- Color: `--gold-muted`
- Letter-spacing: 0.04em
- Subtle text-shadow: `0 0 20px rgba(212,175,55,0.3)`
- Animate in with character-by-character stagger (GSAP SplitText pattern)

### Radial Gold Glow

- `radial-gradient(ellipse at center, rgba(212,175,55,0.12) 0%, transparent 70%)`
- Used behind product images and key text moments
- Animated: scale from 0.8 to 1.2 with opacity pulse

### Background Texture

- Base: solid `--bg` (#0a0a0a)
- Optional subtle noise: `url(noise.svg)` at 3-5% opacity
- Depth layers: multiple absolute-positioned divs with parallax offsets

---

## Motion Principles

### Pacing

- Slow, cinematic transitions (0.8-1.2s between scenes)
- GSAP timelines with easeInOut curves (power2.inOut, power3.inOut)
- Nothing should feel rushed - this is luxury, not hype
- Continuous subtle motion even in "still" moments

### Techniques

| Technique       | Usage                                    | Duration    |
|-----------------|------------------------------------------|-------------|
| Ken Burns       | Product image reveals, background layers | 4-6s cycles |
| Parallax        | Depth separation, text over imagery      | Continuous  |
| GSAP Stagger    | Text reveals, coordinates animation      | 0.6-1.2s    |
| Radial Glow     | Emphasis on product, emotional peaks     | 2-3s pulse  |
| Scale Drift     | Subtle zoom on static elements           | 4-8s cycles |
| Crossfade       | Scene transitions via CSS animation      | 0.8-1.0s    |

### Animation Curves

- Entries: `power2.out` (smooth arrival)
- Exits: `power2.in` (gentle departure)
- Emphasis: `power3.inOut` (dramatic but elegant)
- Continuous: `sine.inOut` (perpetual motion loops)

### SFX Timing

- `impact-bass-1.mp3` (2.12s): Hook moment, first frame impact
- `whoosh-cinematic.mp3` (5.54s): Scene transitions, builds anticipation
- `chime.mp3` (2.5s): Product reveal moment, emotional peak
- `sparkle.mp3` (1.8s): CTA appearance, final flourish

---

## Iteration Guide

### Brand Rules (Non-Negotiable)

1. Products shown: ONLY Coordinates Bracelets and Coordinates Necklaces. NO rings.
2. Background never lighter than `#1a1a1a` - this is a dark, premium brand.
3. Gold accents must feel earned - not splashed everywhere.
4. Playfair Display is always italic. Never upright.
5. RM Neue is always italic. Used only for brand accent moments.
6. CTA must include the current offer: BUY 1 GET 1 FREE + FREE SHIPPING.
7. Every frame must have motion - nothing static, nothing dead.
8. Coordinates text uses the RM Neue Light Italic with gold-muted color.

### Visual Mood

- Think: luxury watch commercial meets personal love letter
- Dark, intimate, warm gold tones
- Close-up textures of engraved metal
- Emotional connection through warm lighting and soft focus
- Premium minimalism - less is more, let the gold breathe

### Image Assets Available

| File | Description | Best Use |
|------|-------------|----------|
| `hero-12.jpg` - `hero-15.jpg` | Hero product shots | Product showcase beats |
| `personalized-jewelry-for-wanderers.jpg` | Lifestyle/wanderer shot | Nostalgia/emotion scene |
| `img-9343-1500x.jpg` | Product detail close-up | Texture/quality moment |
| `coordinates-jewelry-collection-443934-15.jpg` | Collection overview | Multi-product display |
| `ourcoordinates-logo-image-our-coordinate.png` | Brand logo | CTA/closing frame |
| `2e40d462-2602-4c27-a2bc-208220c60fa0.jpeg` | Silver bracelet engraved | Product detail |

### Do Not

- Use pure white text (#ffffff) - always use cream (#f5f0e8)
- Show rings or any non-bracelet/necklace jewelry
- Use fast cuts or high-energy pacing
- Use neon, electric, or saturated accent colors
- Make the video feel like a generic product slideshow
- Use sharp corners on overlays (use 2px radius minimum)
