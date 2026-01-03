# Doughty Brothers Water Heater - Project Documentation

## Project Overview
Static HTML website for dbwaterheater.com - conversion-optimized marketing site focused on turning "no hot water" searches into phone calls and texts.

## Business Details
- **Company Name**: Doughty Brothers Water Heater (plural)
- **Service Area**: Vacaville, CA + ~65 mile radius (Solano, Napa, Yolo, Contra Costa, parts of Sacramento)
- **Key Personnel**: Lyle - expert contractor
- **Value Proposition**: High quality expert service with low overhead, passing savings to customers
- **Business Model**: Small shop operation emphasizing expertise and affordability
- **Pricing**: Tank installs $2,000-$2,500; Tankless quoted after assessment
- **Payment Terms**: 50% upfront, balance on completion

## Technical Details
- **Hosting**: CloudFlare Pages
- **Deployment**: Direct from this git repository (main branch)
- **Technology**: Static HTML/CSS (no build process, no JavaScript)
- **Repository**: https://github.com/tlr-vc/dbwaterheater
- **Framework**: None (pure HTML/CSS for maximum performance)

## Site Structure

```
/
├── index.html              # Homepage with 8 conversion-focused sections
├── style.css               # Single stylesheet (~700 lines, well-organized)
├── favicon.svg             # Simple "DB" favicon
├── robots.txt              # SEO - allow all
├── sitemap.xml             # All 5 pages with priorities
├── /assets/
│   ├── /logo/
│   │   └── logo.svg        # Placeholder logo
│   └── /photos/
│       ├── install-1.svg   # Placeholder photos
│       ├── install-2.svg
│       └── install-3.svg
├── /services/
│   ├── water-heater-replacement.html
│   ├── tankless-water-heater-installation.html
│   └── emergency-no-hot-water.html
└── /legal/
    └── privacy.html
```

## Pages Overview

### Homepage (`/index.html`)
8 sections in this order:
1. Hero - Same-day service, dual CTAs (Call + Text)
2. Quick Offer Tiles - 3 cards linking to service pages
3. Pricing & Terms - Transparent pricing ($2k-$2.5k)
4. How It Works - 3-step process
5. Photo Gallery - Placeholder images
6. Service Area - Vacaville + cities list
7. FAQ - 7 realistic questions
8. Bottom CTA - Repeat dual CTAs

### Service Pages
All 3 follow identical structure:
- Service hero (H1 + intro + dual CTAs)
- "When to Call" section (bulleted list)
- Service-specific FAQ (5 questions)
- Related services (links to other 2 pages)
- Bottom CTA (dual CTAs)
- Sticky mobile bar

### Legal Page
- Simple privacy policy
- `noindex, nofollow` meta tag

## Key Features

### Conversion Optimization
- **Primary CTA**: Call Now (tel: links)
- **Secondary CTA**: Text Us (sms: links)
- **Sticky Mobile Bar**: Fixed bottom bar on mobile only (<768px)
  - Always visible for easy access
  - Two buttons side-by-side
  - Adds body padding to prevent content hiding

### SEO Implementation
- **JSON-LD Schema**: LocalBusiness on homepage only
  - Service area: GeoCircle, 65-mile radius
  - Price range: $2000-$2500
  - Contact info, address
- **Open Graph Tags**: All pages
- **Meta Descriptions**: Unique per page, 150-160 chars
- **Canonical URLs**: All use https://dbwaterheater.com/
- **Title Format**: `[Service] [Location] | [Brand]`
- **Sitemap**: All 5 pages with priority weights

### Mobile-First Design
- Responsive breakpoints: 767px, 1023px
- Mobile bar only shows <768px
- Single-column layouts on mobile
- Touch-friendly 48px button heights
- System fonts (no external resources)

## Phone Number Management

**CRITICAL**: Phone numbers must be updated before going live.

Each HTML file has a comment block at the top:
```html
<!--
CONTACT INFORMATION - Update Here
Phone: (XXX) XXX-XXXX
Phone (tel format): +1XXXXXXXXXX
Email: contact@dbwaterheater.com
License: [LICENSE_NUMBER]

To update phone number:
1. Update this comment
2. Find/replace: tel:+1XXXXXXXXXX
3. Find/replace display: (XXX) XXX-XXXX
-->
```

### Update Process:
1. Open each HTML file
2. Find/replace `tel:+1XXXXXXXXXX` with actual tel format
3. Find/replace `(XXX) XXX-XXXX` with display format
4. Update email if needed
5. Add license number

Files to update:
- index.html
- services/water-heater-replacement.html
- services/tankless-water-heater-installation.html
- services/emergency-no-hot-water.html
- legal/privacy.html

## Asset Placeholders

### Logo (`/assets/logo/logo.svg`)
- Current: Simple SVG with "Doughty Brothers" text
- Replace with: Actual company logo (SVG preferred, PNG acceptable)
- Dimensions: 200x60px (adjust if needed)

### Photos (`/assets/photos/*.svg`)
- Current: 3 gray placeholder SVGs
- Replace with: Actual installation photos
- Recommended: 6-8 photos total
- Format: JPG or WebP
- Dimensions: 400x300px minimum
- Must have: width/height attributes for CLS prevention

### Favicon (`/favicon.svg`)
- Current: Blue square with "DB" text
- Replace with: Logo-based favicon or custom design

## Service Page Template

All service pages follow this pattern:

```html
<!-- Service Hero -->
<section class="service-hero">
  <h1>[Service Name] in Vacaville, CA</h1>
  <p class="service-intro">[2-3 sentences about service]</p>
  <div class="hero-cta-group">
    [Call + Text CTAs]
  </div>
</section>

<!-- When to Call / Why Choose -->
<section class="when-to-call">
  <h2>[When to Call for X / Why Choose X]</h2>
  <ul class="when-list">
    [4-6 bullet points]
  </ul>
</section>

<!-- FAQ -->
<section class="faq-section">
  <h2>[Service] Questions</h2>
  <div class="faq-list">
    [5 <details> elements with Q&As]
  </div>
</section>

<!-- Related Services -->
<section class="related-services">
  [Links to other 2 service pages]
</section>

<!-- Bottom CTA -->
<section class="bottom-cta">
  [Repeat dual CTAs]
</section>
```

To add a 4th service page:
1. Copy any existing service page
2. Update H1, intro, content
3. Update meta tags (title, description, canonical, OG)
4. Update related services links
5. Add to sitemap.xml

## FAQ Content Guidelines

FAQs are written to address common objections and questions:

**Homepage FAQs**: General water heater questions
- Installation time
- Permits
- Tank vs tankless
- Same-day availability
- Warranty
- Haul-away
- Sizing

**Service Page FAQs**: Service-specific questions
- Water Heater Replacement: Lifespan, sizing, permits, warranty, haul-away
- Tankless Installation: Cost, gas vs electric, retrofit, energy savings, maintenance
- Emergency Service: Response time, after-hours, diagnosis, repair vs replace, same-day

## Pre-Launch Checklist

Before deploying to production:

### Content
- [ ] Update phone number in all 5 HTML files
- [ ] Update email address if different
- [ ] Add license number
- [ ] Replace logo SVG with actual logo
- [ ] Replace photo placeholders with real photos (3+ minimum)
- [ ] Update copyright year if needed

### Testing
- [ ] Test all `tel:` links on mobile device
- [ ] Test all `sms:` links on mobile device
- [ ] Verify mobile bar appears on mobile (<768px)
- [ ] Verify mobile bar doesn't cover content
- [ ] Test all internal links (service pages, home, privacy)
- [ ] Verify responsive design at 320px, 375px, 768px, 1024px
- [ ] Check all images display correctly
- [ ] Validate HTML (W3C validator)
- [ ] Test JSON-LD schema (Google Rich Results Test)
- [ ] Verify Open Graph tags work (Facebook Sharing Debugger)
- [ ] Check robots.txt accessible
- [ ] Check sitemap.xml accessible
- [ ] Verify favicon displays

### SEO
- [ ] All pages have unique title tags
- [ ] All pages have unique meta descriptions
- [ ] Canonical URLs correct on all pages
- [ ] JSON-LD validates
- [ ] Sitemap lists all pages

## Performance Notes

Site is optimized for Core Web Vitals:

**LCP (Largest Contentful Paint):**
- System fonts load instantly
- No external resources
- Critical CSS inline (optional)

**FID (First Input Delay):**
- Zero JavaScript
- All interactions are native links

**CLS (Cumulative Layout Shift):**
- All images have width/height
- No dynamic content injection
- Mobile bar uses fixed positioning

Expected Lighthouse scores: 95-100 across all categories

## Deployment

Cloudflare Pages Configuration:
- **Build command**: (none)
- **Build output directory**: `/`
- **Root directory**: `/`
- **Branch**: main

Any push to main branch triggers automatic deployment.

## Future Enhancements

Post-launch opportunities:
- Add customer testimonials section
- Add real install photo gallery
- Create Google Business Profile
- Add simple contact form (Formspree)
- Add analytics (Plausible or similar)
- Add blog/articles for SEO
- Add video testimonials
- Add financing information page
