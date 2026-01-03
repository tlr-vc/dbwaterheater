# Doughty Brothers Water Heater Website

Conversion-optimized static website for dbwaterheater.com - Professional water heater installation and service in Vacaville, CA.

## Project Structure

```
dbwaterheater/
├── index.html                              # Homepage (8 conversion sections)
├── style.css                               # Main stylesheet (~770 lines)
├── favicon.svg                             # Site favicon
├── robots.txt                              # SEO - allow all
├── sitemap.xml                             # All pages with priorities
├── assets/
│   ├── logo/
│   │   └── logo.svg                        # Company logo
│   └── photos/
│       ├── IMG_0117.jpg                    # Installation photo 1
│       ├── IMG_0120.jpg                    # Installation photo 2
│       └── IMG_0123.jpg                    # Installation photo 3
├── services/
│   ├── water-heater-replacement.html       # Tank replacement service
│   ├── tankless-water-heater-installation.html  # Tankless service
│   └── emergency-no-hot-water.html         # Emergency service
├── legal/
│   └── privacy.html                        # Privacy policy
├── BRAND-GUIDELINES.md                     # Logo system & brand specifications
├── CLAUDE.md                               # Detailed project documentation
└── README.md                               # This file
```

## Documentation

- **BRAND-GUIDELINES.md** - Complete logo system, color palette, typography, and usage guidelines
- **CLAUDE.md** - Technical documentation, content guidelines, and maintenance procedures
- **README.md** - This file (quick start and deployment)

## Deployment

This site is hosted on **CloudFlare Pages** and automatically deploys from the `main` branch.

### CloudFlare Pages Configuration
- **Build command:** (none - static HTML)
- **Build output directory:** `/` (root)
- **Root directory:** `/` (root)
- **Branch:** main

Any push to the main branch triggers an automatic deployment.

## Local Development

Open `index.html` in your browser, or use a local server:

```bash
# Python 3
python -m http.server 8000

# Node.js (with npx)
npx serve
```

Then visit `http://localhost:8000` in your browser.

## Before Going Live - CRITICAL UPDATES

### 1. Update Contact Information (All 5 HTML Files)

Each HTML file has a comment block at the top. Update these placeholders:

```html
<!--
CONTACT INFORMATION - Update Here
Phone: (XXX) XXX-XXXX              ← Replace with actual number
Phone (tel format): +1XXXXXXXXXX   ← Replace with actual number
Email: contact@dbwaterheater.com   ← Update if different
License: [LICENSE_NUMBER]          ← Add license number
-->
```

**Find/Replace in each file:**
- Find: `tel:+1XXXXXXXXXX` → Replace with: `tel:+1YOURNUMBER`
- Find: `(XXX) XXX-XXXX` → Replace with: `(555) 123-4567`
- Find: `[LICENSE_NUMBER]` → Replace with actual license

**Files to update:**
1. `index.html`
2. `services/water-heater-replacement.html`
3. `services/tankless-water-heater-installation.html`
4. `services/emergency-no-hot-water.html`
5. `legal/privacy.html`

### 2. Replace Placeholder Assets

**Logo:**
- File: `/assets/logo/logo.svg`
- Current: Text-only placeholder
- Replace with: Actual company logo (SVG preferred, PNG acceptable)

**Photos:**
- Files: `/assets/photos/install-*.svg`
- Current: 3 gray placeholder SVGs
- Replace with: Real installation photos (JPG or WebP)
- Minimum: 3 photos
- Recommended: 6-8 photos
- Dimensions: 400x300px or larger

**Favicon:**
- File: `/favicon.svg`
- Current: Simple "DB" text
- Replace with: Logo-based or custom favicon

### 3. Test Before Launch

**Mobile Testing:**
- [ ] Test `tel:` links on actual phone
- [ ] Test `sms:` links on actual phone
- [ ] Verify sticky bottom bar appears (mobile only)
- [ ] Check bar doesn't cover content

**Desktop Testing:**
- [ ] All internal links work
- [ ] Images display correctly
- [ ] Responsive at 320px, 768px, 1024px, 1440px

**SEO Validation:**
- [ ] HTML validates (https://validator.w3.org/)
- [ ] JSON-LD validates (https://search.google.com/test/rich-results)
- [ ] Open Graph works (https://developers.facebook.com/tools/debug/)
- [ ] robots.txt accessible
- [ ] sitemap.xml accessible

## Site Features

### Conversion Optimization
- **Dual CTAs**: Call Now + Text Us on every page
- **Sticky Mobile Bar**: Always-visible CTAs on mobile
- **Transparent Pricing**: $2,000-$2,500 for tank installs
- **Same-Day Service**: Emphasized throughout
- **Service Area**: Vacaville, CA + 65-mile radius

### SEO Implementation
- JSON-LD LocalBusiness schema on homepage
- Unique meta tags and Open Graph per page
- Sitemap with all 5 pages
- Canonical URLs
- Mobile-first responsive design

### Performance
- **Zero JavaScript**: Pure HTML/CSS
- **System Fonts**: No external font loading
- **Single CSS File**: Minimal HTTP requests
- **Optimized Images**: width/height attributes prevent layout shift
- **Expected Lighthouse Score**: 95-100 across all metrics

## Page Overview

### Homepage
8 sections optimized for conversions:
1. Hero with same-day messaging
2. Service tiles (3 cards)
3. Pricing & payment terms
4. How it works (3 steps)
5. Photo gallery
6. Service area with city list
7. FAQ (7 questions)
8. Bottom CTA

### Service Pages (3 Total)
Each service page includes:
- Service-specific hero
- "When to Call" or benefits list
- 5 FAQs related to that service
- Links to other services
- Dual CTAs top and bottom

### Legal Page
- Simple privacy policy
- Set to `noindex, nofollow`

## Technology Stack

- **HTML5**: Semantic markup
- **CSS3**: Custom properties, Grid, Flexbox
- **No JavaScript**: Maximum performance
- **No Build Process**: Simple deployment
- **No External Dependencies**: Everything self-contained

## Documentation

See `/CLAUDE.md` for detailed documentation including:
- Phone number management
- Service page template
- FAQ content guidelines
- Asset specifications
- Pre-launch checklist

## License

© 2026 Doughty Brothers Water Heater. All rights reserved.
