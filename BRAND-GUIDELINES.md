# DB Water Heater Service
## Brand Guidelines & Logo System

**Version:** 1.0
**Last Updated:** January 2, 2026
**Company:** Doughty Brothers Construction
**License:** 714897

---

## Brand Philosophy

Good choice. The badge as the primary mark + DB droplet as the favicon is exactly what we recommend for a serious home-services brand.

**Brand Character:**
- Traditional
- Rugged
- Trustworthy
- Licensed-trade aesthetic
- Not playful, not modern-tech

**Brand Promise:** "This guy shows up, fixes it right, and leaves."

---

## 1. Logo System Overview

We maintain a minimal, production-ready logo system with four core assets:

### A. Primary Logo (Badge)
- **Used in:** site header, homepage hero, footer
- **Shape:** shield/badge
- **Icon:** DB water droplet
- **Text:** secondary, below or integrated

### B. Icon Logo (Droplet Only)
- **Used for:** favicon, mobile browser tab, social preview
- **Shape:** water droplet with "DB"
- **No text**

### C. Horizontal Lockup (Optional)
- **Used if:** header space is tight
- **Layout:** Badge icon + text to the right

### D. Favicon Set
- 32×32 PNG
- 48×48 PNG
- 180×180 PNG (Apple touch)
- SVG master

---

## 2. Visual Design Specification

### Brand Name (Exact Text)

**DB Water Heater Service**

Do not abbreviate further on the logo.

### Tone & Aesthetic

- Traditional
- Rugged
- Trustworthy
- Licensed-trade aesthetic
- Not playful, not modern-tech

Think: "This guy shows up, fixes it right, and leaves."

### Color Palette (Strict)

#### Primary Blue
```
HEX: #0B4FA2
RGB: 11, 79, 162
Used for: shield fill, droplet fill
```

#### Dark Navy
```
HEX: #0A1F33
RGB: 10, 31, 51
Used for: outlines, background contrast
```

#### White
```
HEX: #FFFFFF
RGB: 255, 255, 255
Used for: DB letters, text, outlines
```

**Color Rules:**
- No gradients unless subtle and minimal
- Flat colors preferred
- High contrast required for legibility

### Typography (Logo Text)

**Style:** Bold, condensed sans-serif
**Case:** All caps
**Feel:** Industrial

**Recommended Font Families:**
- Montserrat SemiBold
- Inter Bold
- Oswald
- Archivo

**Avoid:**
- Script fonts
- Rounded fonts
- Serif fonts

---

## 3. Asset-by-Asset Specifications

### A. Primary Logo — Badge (MAIN LOGO)

**Structure:**
- Outer shield/badge shape
- Inside: large water droplet
- Inside droplet: bold "DB"
- Below or across badge: "WATER HEATER SERVICE" (smaller)

**Rules:**
- Icon must dominate
- Text must be secondary
- Must read clearly at small sizes
- No tools (no wrench) — keep it clean

**Deliverables:**
- `logo-badge.svg` (master)
- `logo-badge.png` (transparent, ~1200px wide)
- `logo-badge-dark.png` (for light backgrounds, if needed)

**File Location:**
```
assets/logo/logo-badge.svg
assets/logo/logo-badge.png
assets/logo/logo-badge-dark.png
```

**Usage:**
- Header (top left)
- Homepage hero
- Footer

**Implementation:**
```html
<header>
  <img src="/assets/logo/logo-badge.svg"
       alt="DB Water Heater Service logo"
       class="logo">
</header>
```

```css
.logo {
  height: 56px;
  width: auto;
}
```

---

### B. Icon Logo — DB Water Droplet (FAVICON)

**Structure:**
- Water droplet only
- "DB" centered inside
- No text
- High contrast

**Rules:**
- Must be legible at 16×16
- No fine detail
- Flat colors

**Deliverables:**
- `icon-droplet.svg` (master)
- `favicon-32.png` (32×32)
- `favicon-48.png` (48×48)
- `apple-touch-icon.png` (180×180)

**File Location:**
```
assets/logo/icon-droplet.svg
assets/logo/favicon-32.png
assets/logo/favicon-48.png
assets/logo/apple-touch-icon.png
```

**Usage:**
- Browser tabs
- Mobile bookmarks
- PWA icons

**Implementation:**
```html
<head>
  <link rel="icon" href="/assets/logo/favicon-32.png" sizes="32x32">
  <link rel="icon" href="/assets/logo/favicon-48.png" sizes="48x48">
  <link rel="apple-touch-icon" href="/assets/logo/apple-touch-icon.png">
</head>
```

---

### C. Horizontal Logo (OPTIONAL)

**Structure:**
- Droplet icon on left
- Text on right: "DB WATER HEATER SERVICE"

**Deliverables:**
- `logo-horizontal.svg`
- `logo-horizontal.png`

**File Location:**
```
assets/logo/logo-horizontal.svg
assets/logo/logo-horizontal.png
```

**Usage:**
- Optional header variant
- Social previews
- Email signatures

---

## 4. Website Integration

### Header Implementation

```html
<header>
  <nav>
    <div class="logo">
      <img src="/assets/logo/logo-badge.svg"
           alt="DB Water Heater Service logo"
           width="200"
           height="60">
    </div>
    <div class="nav-phone">
      <a href="tel:+14154245964" class="phone-link">(415) 424-5964</a>
    </div>
  </nav>
</header>
```

### Favicon Implementation

```html
<head>
  <link rel="icon" href="/assets/logo/favicon-32.png" sizes="32x32">
  <link rel="icon" href="/assets/logo/favicon-48.png" sizes="48x48">
  <link rel="apple-touch-icon" href="/assets/logo/apple-touch-icon.png">
  <link rel="icon" type="image/svg+xml" href="/assets/logo/icon-droplet.svg">
</head>
```

### Footer Implementation

```html
<footer>
  <div class="footer-logo">
    <img src="/assets/logo/logo-badge.svg"
         alt="DB Water Heater Service"
         width="120"
         height="36">
  </div>
  <p><strong>Doughty Brothers Water Heater</strong></p>
  <p>Licensed & Insured • License: 714897</p>
</footer>
```

---

## 5. Logo Usage Guidelines

### DO:
✅ Use the badge logo as the primary mark
✅ Use the droplet icon for favicon and small applications
✅ Maintain adequate clear space around the logo
✅ Use approved colors only
✅ Ensure high contrast on all backgrounds
✅ Scale proportionally

### DO NOT:
❌ No cartoon plumbers
❌ No flames
❌ No gradients everywhere
❌ No drop shadows
❌ No slogans inside the logo
❌ Do not stretch or distort
❌ Do not rotate
❌ Do not change colors
❌ Do not add effects (shadows, glows, bevels)

**Note:** Slogans belong in copy, not the mark.

---

## 6. Clear Space & Minimum Size

### Clear Space
Maintain minimum clear space equal to the height of the "D" in "DB" on all sides of the logo.

### Minimum Sizes

**Digital:**
- Primary badge: 120px wide minimum
- Icon droplet: 16px minimum (favicon)

**Print:**
- Primary badge: 1 inch wide minimum
- Business card: 0.75 inch minimum

---

## 7. Color Applications

### On White Background
- Use primary blue (#0B4FA2) logo
- Full color version

### On Dark Background
- Use white logo with blue droplet
- Or all-white version for maximum contrast

### On Photography
- Ensure sufficient contrast
- Add subtle background overlay if needed
- White version preferred on busy backgrounds

---

## 8. File Organization

```
/assets/logo/
├── logo-badge.svg              # Primary logo (master)
├── logo-badge.png              # Primary logo (raster)
├── logo-badge-dark.png         # Dark version
├── logo-horizontal.svg         # Horizontal lockup
├── logo-horizontal.png         # Horizontal lockup (raster)
├── icon-droplet.svg            # Icon only (master)
├── favicon-32.png              # 32×32 favicon
├── favicon-48.png              # 48×48 favicon
└── apple-touch-icon.png        # 180×180 Apple touch
```

---

## 9. Co-Branding & Partner Logos

When co-branding with manufacturers (Rheem, Bradford White, etc.):
- DB logo maintains primary position (top left)
- Partner logos appear in footer or "Authorized Dealer" section
- DB logo should be equal or larger in size
- Maintain clear separation between marks

---

## 10. Social Media Specifications

### Profile Images
- Use: icon-droplet.svg
- Format: 400×400 PNG
- Background: White or primary blue

### Cover Images
- Use: logo-badge.svg centered
- Add tagline: "Same-Day Water Heater Installation • Vacaville, CA"
- Format: Platform-specific dimensions

### Post Graphics
- Logo: Top-left corner, 80px height
- Maintain brand colors
- Include contact info: (415) 424-5964

---

## 11. Print Applications

### Business Cards
- Logo: Top-left, ~1 inch wide
- Include: Name, License 714897, phone, email

### Vehicle Signage
- Logo: Large and prominent
- Phone number: Highly visible
- "Licensed & Insured • Lic. 714897"

### Uniforms
- Embroidered droplet icon on left chest
- Company name optional on back

---

## 12. Next Steps for Logo Generation

Choose one option:

### Option 1: Generate All Assets Now
Generate complete logo system:
- Badge logo (SVG + PNG)
- Droplet icon (SVG + PNG)
- Favicon set (32, 48, 180)
- Horizontal lockup

### Option 2: Generate Badge + Droplet Only
Start with core assets:
- Primary badge logo
- Droplet favicon
- Refine before creating variants

### Option 3: Refine Specification First
Adjust before generation:
- Shape refinement
- Text layout
- Weight adjustments

---

## 13. Brand Assets Checklist

**Status: COMPLETED** ✅ (January 2, 2026)

Current Assets:
- [x] Primary badge logo (PNG) - `logo-badge.png` (707×716, 264KB)
- [x] Droplet icon (PNG) - `icon-droplet.png` (416×560, 81KB)
- [x] Favicon 32×32 - `favicon-32.png` (2KB)
- [x] Favicon 48×48 - `favicon-48.png` (3KB)
- [x] Apple touch icon 180×180 - `apple-touch-icon.png` (18KB)
- [x] Horizontal lockup (PNG) - `logo-horizontal.png` (666×235, 86KB)

Future Assets (Optional):
- [ ] Primary badge logo (SVG) - for print/scaling
- [ ] Badge logo dark variant (PNG)
- [ ] Droplet icon (SVG) - for print/scaling
- [ ] Horizontal lockup (SVG) - for print/scaling

**Note:** All PNG assets extracted from professional composite design. SVG versions can be generated later for print applications (vehicle wraps, large signage) if needed.

---

## Contact Information

**Business Name:** Doughty Brothers Water Heater
**Phone:** (415) 424-5964
**Email:** dbwaterheater@gmail.com
**License:** 714897
**Service Area:** Vacaville, CA & 65-mile radius
**Website:** https://dbwaterheater.com

---

## Document History

**v1.0 - January 2, 2026**
- Initial brand guidelines document
- Logo system specifications
- Usage guidelines established
- Website integration instructions

---

*These brand guidelines are maintained as part of the DB Water Heater website project. For questions or updates, refer to CLAUDE.md for project documentation.*
