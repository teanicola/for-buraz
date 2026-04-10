# Style Guide: FOR BURAZ Landing Page

## Design Philosophy

The visual language is **neo-noir cinema meets Bosnian cultural identity**. Think Chinatown's sun-bleached Florida gold and Godfather's candlelit amber shadows — but set in Florida, with Islamic green as the distinctive cultural accent. The page should feel like a film poster that scrolls: dark, cinematic, confident, unhurried.

**References:** Chinatown (1974), The Godfather (1972), lookbook.pdf

---

## Color Palette

### Primary (Noir Foundation)
| Name | Hex | Usage |
|---|---|---|
| Deep Black | `#1A1008` | Page background — warm black, not pure #000 |
| Venetian Shadow | `#2C2418` | Card backgrounds, secondary surfaces |
| Warm Amber | `#C68E17` | Primary accent — headlines highlights, stat numbers, hover states |
| Sun-Bleached Gold | `#D4A843` | Secondary accent — labels, dividers, borders |
| Dusty Cream | `#E8D5A3` | Body text (high readability on dark bg) |

### Accent (Cultural Identity)
| Name | Hex | Usage |
|---|---|---|
| Quran Green | `#006B3F` | CTA buttons, key highlights, "invest" actions |
| Deep Mosque Green | `#1B5E20` | Green gradient undertones, hover states on green elements |

### Supporting
| Name | Hex | Usage |
|---|---|---|
| Maroon | `#6B1C2A` | Florida silhouette tint, subtle background radials |
| Navy | `#1B2340` | Background gradient accents, atmospheric depth |
| Muted Gray | `#8A8A8A` | Tertiary text, captions, metadata |
| Deep Sepia | `#704214` | Borders, horizontal rules, subtle warmth |

### Usage Rules
- Background is always `Deep Black` (#1A1008), never pure black
- Primary text is `Dusty Cream` (#E8D5A3) at 90% opacity for body, 100% for headings
- `Warm Amber` (#C68E17) is the dominant accent — used for section labels, stat numbers, cast role labels, blockquote borders
- `Quran Green` (#006B3F) is reserved for CTAs and investment-related elements only — it should feel special and intentional, not overused
- `Maroon` and `Navy` are atmospheric — used in low-opacity radial gradients and Florida silhouette tints, never as text colors
- Dividers use `Deep Sepia` (#704214) at 30% opacity, fading to transparent at edges

---

## Typography

### Display Font: Morrison
- **File:** `assets/fonts/Morrison-Regular.otf` (loaded via @font-face)
- **Usage:** Film title (hero), section headings (h2), cast names, stat numbers, team member names
- **Weight:** Regular only (no bold available)
- **Fallback:** `Georgia, 'Times New Roman', serif`
- **Character:** Elegant, cinematic serif with classic film-poster energy

### Body Font: Avenir (System Stack)
- **Stack:** `'Avenir', 'Avenir Next', 'Helvetica Neue', Helvetica, Arial, sans-serif`
- **Usage:** Body text, labels, captions, navigation, metadata
- **Note:** Avenir TTC file cannot be used in browsers. Rely on system font availability (ships with macOS). The fallback stack ensures cross-platform readability.

### Type Scale
| Element | Font | Size | Weight | Letter-spacing | Transform |
|---|---|---|---|---|---|
| Hero title | Morrison | `clamp(3.5rem, 10vw, 8rem)` | normal | 0.06em | — |
| Section heading (h2) | Morrison | `clamp(2rem, 5vw, 3rem)` | normal | — | — |
| Section label | Avenir | 0.65rem | normal | 0.4em | uppercase |
| Body text | Avenir | 1.05rem | normal | — | — |
| Cast name | Morrison | 1.3rem | normal | — | — |
| Cast role | Avenir | 0.8rem | normal | 0.2em | uppercase |
| Stat number | Morrison | 3rem | normal | — | — |
| Stat label | Avenir | 0.75rem | normal | 0.2em | uppercase |
| Blockquote | Avenir | 1.05rem | normal (italic) | — | — |
| Accolade pill | Avenir | 0.8rem | normal | 0.05em | — |

### Line Heights
- Headings: 1.0–1.2
- Body text: 1.6–1.8
- Blockquotes: 1.8

---

## Components

### 1. Hero
- Full viewport height (`100vh`), centered content
- Film title in Morrison at maximum scale
- Subtitle labels in Avenir uppercase with wide letter-spacing
- Florida silhouette (white PNG) positioned bottom-right at ~6% opacity
- Atmospheric radial gradients (maroon + navy) behind content
- Scroll indicator at bottom

### 2. Section Label
- Small uppercase text in `Sun-Bleached Gold`
- Sits above each section heading
- Format: `THE STORY` / `THE CAST` / `THE OPPORTUNITY`

### 3. Cast Card
- Dark card (`Venetian Shadow` background)
- 1px border in cream at 8% opacity, gold at 30% on hover
- Contains: headshot photo (top), name (Morrison), role (Avenir uppercase gold), credits (Avenir italic muted), IMDB link
- Grid layout: 3 across on desktop, 2 on tablet, 1 on mobile

### 4. Stat Block
- Large number in Morrison + `Warm Amber`
- Small label underneath in Avenir uppercase + `Muted Gray`
- Used for: diaspora count, budget, ROI multiples, comparable film grosses

### 5. Director Quote Block
- Left border: 2px solid `Warm Amber`
- Background: subtle navy gradient fading to transparent
- Italic body text
- Citation in gold, non-italic

### 6. Comparable Film Card
- Film title, budget, gross revenue, ROI multiple
- Visual bar or ratio indicator showing budget-to-gross scale
- Source attribution at bottom

### 7. Revenue Projection Table
- Three-column layout: Basic / Good / Excellent
- Styled as dark table with gold headers
- Key numbers highlighted in `Warm Amber`

### 8. Team Member Card
- Name (Morrison), role (Avenir uppercase gold), bio paragraph
- Optional: headshot photo

### 9. Accolade Pill
- Inline badge/tag for script recognition
- Background: `Warm Amber` at 8% opacity
- Border: `Warm Amber` at 20%
- Text: `Warm Amber`

### 10. CTA Button
- Background: `Quran Green` (#006B3F)
- Text: `Dusty Cream`, uppercase Avenir, wide letter-spacing
- Hover: `Deep Mosque Green` (#1B5E20)
- Used sparingly — investment inquiry, contact, crowdfunding

### 11. Vimeo Embed
- Full-width responsive container (16:9 aspect ratio)
- Thin border in `Deep Sepia` at 20%
- Placed after story/cast intro, before financial sections

### 12. Divider
- Horizontal rule: 1px `Deep Sepia` at 30%, gradient fade to transparent at edges
- Florida silhouette break: centered image at ~8% opacity, 160px tall

### 13. Footer
- Centered, very small uppercase text
- `Muted Gray` at 40% opacity
- "Confidential" notice

---

## Layout

- **Max content width:** 900px, centered
- **Section padding:** 6rem vertical, 2rem horizontal (desktop); 4rem / 1.5rem (mobile)
- **Breakpoints:** 640px (mobile), 900px (tablet)

---

## Imagery

### Florida Silhouettes
Available in 6 colors. Primary usage:
- **White** (`Florida_6.png`): Hero background, low opacity
- **Maroon** (`Florida_1.png`): Section break decorative
- **Navy** (`Florida_2.png`): Section break decorative
- **Green** (`Florida_3.png`): Could be tinted to Quran green for CTA areas

### Cast Headshots
- Needed for each cast member card
- Preferred: high-contrast black & white or warm-toned portraits to match noir aesthetic
- Fallback: dark silhouette placeholder with name overlay

### Sizzle Reel
- Vimeo URL: `https://vimeo.com/sabinavajraca/forburazsizzle`
- Embedded as responsive iframe in 16:9 container
