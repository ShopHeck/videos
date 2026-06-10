# OurCoordinates - Cinematic Promo Storyboard

## Format & Specs

| Property     | Value                        |
|--------------|------------------------------|
| Dimensions   | 1080 x 1920 (9:16 portrait) |
| Duration     | ~20 seconds                  |
| FPS          | 30                           |
| Platform     | TikTok / X                   |
| Pacing       | Slow / Cinematic             |
| Architecture | Sub-compositions with CSS crossfade transitions |

## Narrative Arc

**Emotion (Nostalgia) -> Product (Beauty) -> Emotion (Happiness) -> Action (CTA)**

The viewer is taken on a journey: remembering a place that matters, seeing that memory transformed into wearable art (bracelets and necklaces only), feeling the joy of holding something personal, then being invited to get their own.

---

## Audio Timeline

| Time      | SFX                    | Purpose                          |
|-----------|------------------------|----------------------------------|
| 0.0s      | `impact-bass-1.mp3`   | Hook impact, first frame punch   |
| 2.5s      | `whoosh-cinematic.mp3` | Transition into nostalgia scene  |
| 7.0s      | `chime.mp3`           | Product reveal moment            |
| 12.0s     | `chime.mp3`           | Happiness emotional peak         |
| 16.0s     | `sparkle.mp3`         | CTA sparkle entrance             |

---

## Beat 1: The Hook (0s - 3s)

**Concept:** Golden GPS coordinates fade in character by character against deep black, pulling the viewer in with mystery and elegance.

**Sub-composition:** `compositions/beat-01-hook.html`

### Visual Layers

1. **Background** - Solid `#0a0a0a` with a slow-expanding radial gold glow at center
   - `radial-gradient(ellipse at 50% 50%, rgba(212,175,55,0.08) 0%, transparent 60%)`
   - Animate: scale 0.6 to 1.3 over 3s (continuous expansion)

2. **Depth Particles** - 4-6 tiny gold dots floating with parallax offset
   - Size: 2-4px circles, color `#d4af37` at 30% opacity
   - Motion: gentle drift upward at different speeds (parallax depth simulation)
   - Transform: translateY from 100px to -100px over 6s, staggered starts

3. **Coordinates Text** - Main focal element
   - Text: `40.7128 N, 74.0060 W` (example NYC coordinates)
   - Font: RM Neue 300 Italic, 22px, letter-spacing 0.04em
   - Color: `#bfa265` (muted gold)
   - Animation: GSAP SplitText stagger, each character fades in and slides up 10px
   - Stagger: 0.04s per character, power2.out easing
   - Text-shadow: `0 0 20px rgba(212,175,55,0.4)`

4. **Tagline** - Appears after coordinates settle
   - Text: "Every place tells a story"
   - Font: Playfair Display 400 Italic, 36px
   - Color: `#f5f0e8`
   - Animation: opacity 0 to 1, translateY 20px to 0, delay 1.5s, duration 0.8s

### Techniques
- GSAP character stagger (coordinates text)
- Radial glow pulse (background)
- Parallax depth particles (floating gold dots)
- Continuous motion: glow expands, particles drift, text breathes with subtle scale oscillation

### SFX
- `impact-bass-1.mp3` at 0.0s (sharp bass hit on first coordinate character)

### Transition Out
- CSS crossfade: opacity fade over 0.8s overlapping with Beat 2 entrance

---

## Beat 2: Nostalgia (3s - 7.5s)

**Concept:** A warm, golden-tinted scene evoking the feeling of remembering a meaningful place. The viewer sees coordinates being discovered - a moment of connection to somewhere special.

**Sub-composition:** `compositions/beat-02-nostalgia.html`

### Visual Layers

1. **Background Image** - `capture/assets/personalized-jewelry-for-wanderers.jpg`
   - Display: full-frame cover, slightly desaturated (filter: saturate(0.7))
   - Ken Burns: slow zoom from scale(1.0) to scale(1.15) over 4.5s
   - Warm overlay: `rgba(212,175,55,0.08)` blended on top

2. **Depth Overlay** - Dark vignette for text readability
   - `radial-gradient(ellipse at center, transparent 30%, rgba(10,10,10,0.6) 100%)`
   - Static layer, provides cinematic framing

3. **Gold Light Leak** - Animated warm glow from top-right
   - Radial gradient: `rgba(212,175,55,0.15)` positioned at 80% 20%
   - Animation: opacity pulses 0.5 to 1.0 over 3s, slight position drift

4. **Emotion Text** - Nostalgic headline
   - Text: "Remember that place?"
   - Font: Playfair Display 700 Italic, 52px
   - Color: `#f5f0e8`
   - Position: centered, upper third
   - Animation: GSAP fromTo - opacity 0 to 1, y: 30 to 0, duration 1s, power2.out
   - Subtle continuous float: translateY oscillates 3px with sine.inOut over 4s

5. **Coordinates Whisper** - Small coordinates beneath headline
   - Text: "34.0195 N, 118.4912 W"
   - Font: RM Neue 300 Italic, 16px, letter-spacing 0.06em
   - Color: `#bfa265` at 70% opacity
   - Animation: fade in 0.6s after headline, staggered characters

### Techniques
- Ken Burns slow zoom (background image)
- Parallax: text layer moves at different rate than background (translateY offset on scroll-time)
- GSAP stagger on coordinates text
- Radial gold glow animation (light leak)
- Continuous motion: Ken Burns never stops, light leak pulses, text floats

### SFX
- `whoosh-cinematic.mp3` starts at 2.5s (carries through transition and into this beat)

### Transition Out
- CSS crossfade: 1.0s overlap with Beat 3, background dims as products emerge

---

## Beat 3: Product Showcase (7.5s - 12s)

**Concept:** The coordinates become real - beautiful bracelets and necklaces are revealed with premium lighting. Each piece shown as wearable art. Only bracelets and necklaces - no other jewelry types.

**Sub-composition:** `compositions/beat-03-product.html`

### Visual Layers

1. **Background** - Solid `#0a0a0a` with subtle gradient shift
   - Subtle vertical gradient: `#0a0a0a` to `#1a1a1a` (bottom to top)
   - Creates slight depth without distraction

2. **Product Image A** - `capture/assets/hero-12.jpg`
   - Position: centered, takes ~70% of frame height
   - Ken Burns: scale(1.0) to scale(1.08), slight pan left-to-right over 4.5s
   - Border: none, clean full-bleed look
   - Entrance: scale(0.95) to scale(1.0), opacity 0 to 1, duration 0.8s

3. **Product Image B** - `capture/assets/hero-14.jpg`
   - Crossfades in at 2.2s into this beat (replaces Image A)
   - Same Ken Burns treatment but opposite direction (right-to-left pan)
   - Smooth CSS crossfade between A and B over 0.8s

4. **Gold Accent Frame** - Thin gold border that traces in
   - 1px border in `#d4af37` at 40% opacity
   - Inset: 40px from edges
   - Animation: draws in from corners using clip-path or border-image reveal
   - Duration: 1.5s, power3.inOut

5. **Product Label** - Subtle text overlay
   - Text: "Coordinates Bracelet" then crossfades to "Coordinates Necklace"
   - Font: Inter 400, 16px, uppercase, letter-spacing 0.1em
   - Color: `#f5f0e8` at 80% opacity
   - Position: bottom center, 80px from bottom
   - Animation: fade and slide, synced with image crossfade

6. **Radial Glow** - Behind product images
   - `radial-gradient(ellipse at 50% 50%, rgba(212,175,55,0.1) 0%, transparent 50%)`
   - Pulses subtly with the product transitions

### Techniques
- Ken Burns zoom and pan (product images)
- CSS crossfade between multiple products (image swap at midpoint)
- GSAP border draw animation (gold accent frame)
- Parallax depth: glow layer moves slower than product image
- Continuous motion: Ken Burns never stops, glow pulses, label breathes

### SFX
- `chime.mp3` at 7.0s (melodic reveal as first product appears)

### Transition Out
- CSS crossfade: 0.8s overlap, gold glow intensifies as it bridges to happiness scene

---

## Beat 4: Happiness (12s - 16s)

**Concept:** The emotional payoff - the finished product arrives and brings pure joy. Warm gold light explodes outward, suggesting the feeling of holding something deeply personal. The viewer feels the delight of receiving their coordinates jewelry.

**Sub-composition:** `compositions/beat-04-happiness.html`

### Visual Layers

1. **Background** - Dark base with expanding gold burst
   - Base: `#0a0a0a`
   - Gold burst: radial-gradient expanding from center
   - Animation: radial gradient scale from 0 to 1.5 over 2s, then settles at 1.2
   - Color: `rgba(212,175,55,0.12)` at peak, fading to `rgba(212,175,55,0.06)`

2. **Product Detail** - `capture/assets/img-9343-1500x.jpg`
   - Close-up of engraved coordinates on jewelry
   - Ken Burns: very slow zoom in, scale(1.0) to scale(1.06)
   - Soft warm filter: brightness(1.05) saturate(0.9)
   - Position: fills frame, object-fit cover

3. **Gold Particle Burst** - Celebratory sparkle particles
   - 12-16 small gold circles (3-6px)
   - Animation: burst outward from center point in all directions
   - GSAP stagger: 0.02s between particles, power2.out
   - Particles drift outward and fade over 2s
   - Color: mix of `#d4af37` and `#e8c84a`

4. **Emotion Text** - Joy headline
   - Text: "Yours. Forever."
   - Font: Playfair Display 700 Italic, 64px
   - Color: `#f5f0e8`
   - Animation: scale(0.9) to scale(1.0), opacity 0 to 1, duration 0.8s, power3.out
   - Continuous: subtle glow pulse on text-shadow

5. **Coordinates Beneath** - Personal touch
   - Text: "48.8566 N, 2.3522 E"
   - Font: RM Neue 600 Italic, 20px
   - Color: `#d4af37`
   - Animation: fades in 0.5s after headline, slides up 10px
   - Text-shadow: `0 0 30px rgba(212,175,55,0.5)` (stronger glow for emphasis)

### Techniques
- Radial gold burst animation (celebratory energy)
- GSAP stagger particle burst (sparkle effect)
- Ken Burns on product detail (continuous motion)
- Scale entrance on typography (dramatic reveal)
- Continuous motion: particles drift, glow pulses, image zooms, text breathes

### SFX
- `chime.mp3` at 12.0s (emotional peak chime, same melodic tone as product reveal but feels like resolution)

### Transition Out
- CSS crossfade: 0.8s, gold glow concentrates toward center as CTA emerges

---

## Beat 5: CTA (16s - 20s)

**Concept:** Clean, bold call to action. The offer is irresistible - BUY 1 GET 1 FREE plus FREE SHIPPING. Brand logo anchors trust. Everything converges to the action moment.

**Sub-composition:** `compositions/beat-05-cta.html`

### Visual Layers

1. **Background** - Rich dark with gold gradient accent
   - Base: `#0a0a0a`
   - Accent: thin horizontal gold gradient line at vertical center
   - `linear-gradient(to right, transparent, rgba(212,175,55,0.3), transparent)`
   - Animation: width expands from 0% to 100% over 1.2s, then gently pulses opacity

2. **Brand Logo** - `capture/assets/ourcoordinates-logo-image-our-coordinate.png`
   - Position: top third, centered
   - Size: 200px width, auto height
   - Animation: opacity 0 to 1, scale(0.95) to scale(1.0), duration 0.6s
   - Subtle continuous: very gentle scale oscillation (1.0 to 1.01, sine.inOut, 3s)

3. **Offer Headline** - Primary CTA text
   - Text: "BUY 1 GET 1 FREE"
   - Font: Inter 500, 36px, uppercase, letter-spacing 0.04em
   - Color: `#d4af37`
   - Position: center
   - Animation: GSAP fromTo - y: 40 to 0, opacity 0 to 1, duration 0.7s, delay 0.3s
   - Continuous: subtle gold glow pulse on text-shadow

4. **Shipping Line** - Secondary offer text
   - Text: "+ FREE SHIPPING"
   - Font: Inter 400, 22px, uppercase, letter-spacing 0.06em
   - Color: `#f5f0e8`
   - Position: directly below offer headline, 16px gap
   - Animation: same as headline but 0.2s later delay

5. **Urgency Accent** - Subtle scarcity framing
   - Text: "Limited Time"
   - Font: Inter 300, 14px, uppercase, letter-spacing 0.1em
   - Color: `#bfa265` at 70% opacity
   - Position: below shipping line, 24px gap
   - Animation: fades in last, 0.8s after beat starts

6. **Gold Border Frame** - Elegant container
   - 1px border, color `#d4af37` at 25% opacity
   - Inset: 60px from all edges
   - Animation: draws in from all four corners simultaneously, 1s duration
   - Creates premium framing around entire CTA block

7. **Sparkle Accents** - Final polish
   - 4 small sparkle points at corners of the border frame
   - Color: `#e8c84a`
   - Animation: scale 0 to 1 and back, staggered at frame corners
   - Creates a twinkling premium finish

### Techniques
- GSAP stagger text entrance (headline then subtext)
- Border draw animation (gold frame traces in from corners)
- Radial glow on CTA text (subtle pulsing emphasis)
- Sparkle scale animations (corner accents)
- Continuous motion: logo breathes, text glows pulse, sparkles twinkle, line pulses

### SFX
- `sparkle.mp3` at 16.0s (bright ascending whoosh as CTA appears)

### Transition Out
- Hold final frame for 0.5s with all elements visible (no exit transition - video ends on CTA)

---

## Transition Architecture

All transitions use CSS crossfade (opacity-based) rather than shader effects, matching the elegant and understated brand tone.

| From     | To       | Duration | Method                                    |
|----------|----------|----------|-------------------------------------------|
| Beat 1   | Beat 2   | 0.8s     | Opacity crossfade, Beat 1 fades as Beat 2 enters |
| Beat 2   | Beat 3   | 1.0s     | Opacity crossfade with background dim     |
| Beat 3   | Beat 4   | 0.8s     | Opacity crossfade, gold glow bridges      |
| Beat 4   | Beat 5   | 0.8s     | Opacity crossfade, glow concentrates      |

### Implementation Pattern

```css
.beat {
  position: absolute;
  inset: 0;
  opacity: 0;
  animation: crossfade-in var(--beat-duration) ease-in-out var(--beat-start) forwards;
}

@keyframes crossfade-in {
  0% { opacity: 0; }
  5% { opacity: 1; }
  90% { opacity: 1; }
  100% { opacity: 0; }
}
```

Each sub-composition is layered with `position: absolute` and the master composition controls their opacity timing.

---

## Master Timeline

| Time   | Event                              | Beat  |
|--------|------------------------------------|-------|
| 0.0s   | Impact bass hit, coordinates start | 1     |
| 0.8s   | Full coordinates visible           | 1     |
| 1.5s   | Tagline fades in                   | 1     |
| 2.2s   | Crossfade begins to Beat 2        | 1->2  |
| 3.0s   | Nostalgia scene fully visible      | 2     |
| 3.5s   | "Remember that place?" appears     | 2     |
| 4.5s   | Coordinates whisper fades in       | 2     |
| 6.5s   | Crossfade begins to Beat 3        | 2->3  |
| 7.5s   | Product image A revealed           | 3     |
| 7.0s   | Chime SFX for product              | 3     |
| 8.0s   | Gold border starts drawing         | 3     |
| 9.7s   | Crossfade to product image B       | 3     |
| 11.2s  | Crossfade begins to Beat 4        | 3->4  |
| 12.0s  | Gold burst explodes, chime plays   | 4     |
| 12.5s  | "Yours. Forever." appears          | 4     |
| 13.0s  | Coordinates beneath fade in        | 4     |
| 15.2s  | Crossfade begins to Beat 5        | 4->5  |
| 16.0s  | Sparkle SFX, CTA enters           | 5     |
| 16.3s  | Brand logo visible                 | 5     |
| 16.6s  | "BUY 1 GET 1 FREE" slides in      | 5     |
| 16.8s  | "+ FREE SHIPPING" follows          | 5     |
| 17.5s  | Border frame completes             | 5     |
| 18.0s  | Sparkle corner accents fire        | 5     |
| 20.0s  | Video ends on CTA hold frame       | 5     |

---

## Technical Notes

- All sub-compositions are 1080x1920 HTML files in `compositions/`
- Master `index.html` layers them with absolute positioning and CSS animation timing
- GSAP timelines register to `window.__timelines` with `paused: true`
- HyperFrames playback controller advances timelines frame-by-frame
- Images use relative paths from project root: `capture/assets/filename.jpg`
- Font files loaded via @font-face from `capture/assets/fonts/`
- SFX files referenced from `sfx/` directory in hyperframes.json audio tracks
