# ZOEY TRAN — Brand Specification for Web Development

## Brand Identity Overview

Zoey Tran's brand lives at the intersection of corporate sophistication and spiritual warmth. The visual identity blends editorial elegance with celestial/nature imagery, using warm gradients, grainy textures, and collage-style elements. The overall feeling should be: grounded, warm, elevated, and slightly mystical — never cold, corporate-sterile, or generic wellness.

---

## COLOR PALETTE

### Light Colors
| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Pearl** | `#F9F3E8` | rgb(249, 243, 232) | Primary background — substitute for white. NEVER use pure white (#FFFFFF) |
| **Peach** | `#FAE9DB` | rgb(250, 233, 219) | Card backgrounds, section backgrounds, gradient start color |
| **Light Gold** | `#E0CA98` | rgb(224, 202, 152) | Accent highlights, gradient midtones, decorative elements |
| **Periwinkle** | `#BBB8CD` | rgb(187, 184, 205) | Card backgrounds (alternating with peach), cool accent, gradient end color |

### Mid-Value Color
| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Rosy Taupe** | `#C6958F` | rgb(198, 149, 143) | Borders, subtle accents, hover states, decorative midtones |

### Dark / Bright Colors
| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Terracotta** | `#893C23` | rgb(137, 60, 35) | PRIMARY brand color — headings, logo, primary CTA buttons, links |
| **Indigo** | `#3D304F` | rgb(61, 48, 79) | Section divider banners, deep accents, secondary headings, footer |
| **Amber** | `#BA8637` | rgb(186, 134, 55) | Warm accent, decorative details, hover states |

### Text Color
| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Charcoal** | `#382C28` | rgb(56, 44, 40) | ALL body text — substitute for black. NEVER use pure black (#000000) |

### Color Rules
- Light and dark colors can mix together for legibility
- Never place two light colors together (e.g., peach text on pearl background)
- Never place two dark colors together (e.g., terracotta text on indigo background)
- Terracotta is the dominant brand color — use it for primary headings and CTAs
- Indigo is used for section dividers and deep-accent areas
- Pearl replaces white everywhere — backgrounds, cards, light surfaces
- Charcoal replaces black everywhere — body text, fine print, dark text

---

## TYPOGRAPHY

### Heading Font — Feature Display Condensed
- **Web substitute:** Playfair Display (Google Fonts) — closest available match for the art nouveau, elegant serif style
- **Usage:** Large section headings, hero statement, venture names
- **Styles:** Can be used in uppercase OR lowercase. Italics for emphasis and elegance
- **CSS:** `font-family: 'Playfair Display', serif;`

### Subheading / Body Font — Rebond Grotesque  
- **Web substitute:** DM Sans (Google Fonts) — clean, modern geometric sans-serif
- **Usage:** Subheadings in ALL CAPS with letter-spacing. Body copy in regular weight
- **Subheading style:** All caps, wide letter-spacing (0.15em–0.2em), lighter weight
- **Body style:** Regular weight, normal case, comfortable line-height (1.6–1.8)
- **CSS:** `font-family: 'DM Sans', sans-serif;`

### Button / Callout Font — Courier Prime
- **Web:** Courier Prime IS available on Google Fonts — use directly
- **Usage:** CTA buttons, callout text, secondary subheaders, navigation labels, small caps sections
- **Style:** All caps with letter-spacing (0.1em–0.15em) for buttons and callouts
- **CSS:** `font-family: 'Courier Prime', monospace;`

### Type Hierarchy
```
LARGE HEADING          → Playfair Display, 48-72px, Terracotta or Indigo
  Italic subheading    → Playfair Display Italic, 32-48px, Terracotta
SMALL CAPS SUBHEADING  → DM Sans, ALL CAPS, 12-14px, letter-spacing 0.15em, Charcoal or Rosy Taupe
Body copy              → DM Sans, 16-18px, regular, Charcoal, line-height 1.7
BUTTON / CTA           → Courier Prime, ALL CAPS, 12-14px, letter-spacing 0.1em
Fine print / footnote  → DM Sans, 13-14px, Rosy Taupe
```

---

## GRADIENT TEXTURES

Gradients are a core part of the brand. They should feel warm, organic, and slightly imperfect — like watercolor or film grain, NOT like clean CSS linear gradients.

### Primary Gradient Combinations
1. **Peach → Light Gold** (warm, golden — for hero sections)
2. **Peach → Periwinkle** (warm-to-cool — for pull quotes, testimonials)
3. **Rosy Taupe → Indigo** (deep, dramatic — for section dividers)
4. **Pearl → Peach** (subtle, soft — for general backgrounds)
5. **Light Gold → Amber** (warm, rich — for accent sections)
6. **Periwinkle → Peach → Light Gold** (multi-stop — for full-width atmospheric sections)

### Gradient Implementation
- Use CSS gradients as base but add a **grain/noise texture overlay** for the organic feel
- Apply grain via a pseudo-element or overlay div with a noise SVG/PNG at ~5-10% opacity
- Gradients should feel atmospheric and blended, not sharp or geometric
- Use `background-blend-mode` or layered backgrounds for depth
- Consider radial gradients or asymmetric gradient angles (135deg, 160deg) over straight horizontal/vertical

### CSS Example for Grain Gradient
```css
.gradient-section {
  background: linear-gradient(135deg, #FAE9DB 0%, #BBB8CD 100%);
  position: relative;
}
.gradient-section::after {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,..."); /* noise texture */
  opacity: 0.08;
  mix-blend-mode: overlay;
  pointer-events: none;
}
```

---

## LOGOS & BRAND MARKS

### Primary Logo
- "ZOEY TRAN" wordmark in Feature Display Condensed (Playfair Display on web)
- Minimum size: 2" wide (don't go smaller)
- Can be used in ANY color from the palette
- Terracotta on Pearl is the default treatment
- Indigo on Pearl for darker sections
- Pearl/cream on Indigo or Terracotta backgrounds for reversed treatment
- Do NOT distort — only scale proportionally

### Secondary Logo / Monogram
- "ZT" circular badge with decorative script
- Use for: favicon, small placements, mobile nav, footer icon
- Typically in Terracotta, Indigo, or Amber

### Logo Clearance
- All logos need generous white space around them
- Don't crowd logos near text or edges
- Minimum clearance: roughly the height of the "Z" on all sides

---

## IMAGERY & COLLAGE ELEMENTS

The brand uses celestial/nature collage elements as visual motifs. These appear in social content and can be used as decorative accents on the website.

### Collage Motifs (for decorative use)
- **Crystals** — clear quartz, amethyst (connects to energy/healing work)
- **Moon** — crescents and full moons in terracotta/amber tones (cycles, transformation)
- **Butterflies** — blue morpho butterflies (transformation, beauty)
- **Mountains** — terracotta/warm-toned mountain silhouettes (grounding, journey)
- **Flowers** — dahlias, organic florals (growth, unfolding)
- **Saturn/planets** — celestial bodies (cosmic connection, bigger picture)

### Photography Style
- Warm, natural light — golden hour preferred
- Editorial quality — not stock photo sterile
- Soft focus backgrounds with sharp subject
- Earthy, warm color grading that matches the palette
- Intimate, authentic feel — not overly posed
- Settings: nature, modern minimalist interiors, wellness spaces

### Image Treatment on Web
- Photos should have a slight warm color grade to match brand tones
- Consider a subtle grain overlay on photos for consistency
- Use rounded corners sparingly (8-12px max) — the brand leans more editorial than bubbly
- Alternating card backgrounds (peach/periwinkle) for grid layouts

---

## LAYOUT & COMPOSITION PRINCIPLES

### From the Brand Examples (Pages 11-12 of guidelines)
- **Strong typographic hierarchy** — large display headings dominate, with small all-caps subheadings
- **Texture as atmosphere** — gradient textures used as full backgrounds, not just accents
- **Collage-style layering** — images, text, and decorative elements overlap and layer
- **Asymmetric compositions** — content doesn't always center; editorial-style offset layouts
- **Generous whitespace** — sections breathe, content isn't cramped
- **Full-bleed gradient sections** — some sections span the full viewport width with gradient backgrounds

### Web-Specific Layout Notes
- Hero: Full-viewport-height with gradient background and logo
- Section dividers: Full-width indigo banners with Courier Prime all-caps text
- Cards: Clean, minimal borders — rely on background color (peach/periwinkle) for differentiation
- The overall layout should feel like an editorial magazine page, not a typical SaaS landing page
- Use subtle entrance animations (fade-up on scroll) for sections — keep them gentle, not bouncy

---

## SECTION-SPECIFIC DESIGN NOTES

### Hero Section
- Full viewport height, gradient background (peach → pearl → light gold)
- Grain texture overlay
- Logo centered at top
- Tagline in Courier Prime, all caps, wide letter-spacing, Rosy Taupe
- Hero statement in Playfair Display Italic, large, Terracotta
- Credential line in DM Sans, small, Charcoal
- "Let's Connect" CTA button: Courier Prime, all caps, Terracotta bg with Pearl text (or outlined)

### Section Dividers
- Full-width banners in Indigo (#3D304F) background
- Text in Pearl (#F9F3E8), Courier Prime, all caps, letter-spaced
- Used for: "Ways to Enter the Space", "What I'm Building"

### Service Cards
- Two-column grid on desktop, stacked on mobile
- Pearl background with subtle border or shadow
- Service name in Playfair Display, Terracotta
- Tagline in Playfair Display Italic, smaller
- Pricing in Courier Prime
- Description in DM Sans body

### Testimonial Cards
- Three-column grid on desktop, stacked on mobile
- Alternating backgrounds: Peach (#FAE9DB) and Periwinkle (#BBB8CD)
- Large decorative quotation mark in Terracotta or Amber (Playfair Display, 72px+)
- Quote text in Playfair Display Italic
- Name in DM Sans bold, Charcoal
- Title in DM Sans regular, Rosy Taupe

### Pull Quote
- Full-width section with Peach → Periwinkle gradient + grain overlay
- Centered text in Playfair Display Italic, Indigo, ~28-36px
- Generous vertical padding (100px+)

### Ventures Table/Grid
- Clean rows or cards, not a literal HTML table
- Venture name in Playfair Display, Terracotta
- Type badge in Courier Prime, all caps, small
- Description in DM Sans
- Status in Courier Prime, Amber or Rosy Taupe
- Stacks vertically on mobile

### Contact Form
- Pearl background
- Input fields with Rosy Taupe borders, DM Sans text
- Send button: Terracotta background, Pearl text, Courier Prime all caps
- Thank you message: Playfair Display Italic, Terracotta
- Mailto link in DM Sans, Terracotta, below the form

### Sticky CTA Button
- Appears bottom-right after scrolling past hero
- Terracotta background, Pearl text, Courier Prime
- Subtle shadow for elevation
- Smooth fade-in animation
- Links to #connect

---

## THINGS TO NEVER DO

- Never use pure white (#FFFFFF) — use Pearl (#F9F3E8)
- Never use pure black (#000000) — use Charcoal (#382C28)
- Never use generic fonts (Inter, Roboto, Arial, system-ui)
- Never use sharp, clean gradients without grain texture
- Never use harsh drop shadows — keep shadows soft and warm-toned
- Never make it look like a generic wellness template or SaaS landing page
- Never use bright/saturated blues, greens, or reds outside the defined palette
- Never distort the logo
- Never crowd the logo with other elements
