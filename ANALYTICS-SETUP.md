# Analytics Setup Guide

This guide will help you set up Google Analytics 4 and Google Search Console for the DB Water Heater website.

## Google Analytics 4 Setup

### Step 1: Create Google Analytics Account

1. Go to https://analytics.google.com/
2. Sign in with your Google account
3. Click "Start measuring" or "Admin" (gear icon)
4. Click "Create Property"

### Step 2: Configure Your Property

1. **Property name:** `DB Water Heater`
2. **Reporting time zone:** Select `United States - Pacific Time`
3. **Currency:** USD - US Dollar
4. Click "Next"

### Step 3: About Your Business

1. **Industry category:** Select "Home & Garden" or "Business Services"
2. **Business size:** Select "Small" (1-10 employees)
3. Click "Next"

### Step 4: Business Objectives

1. Select:
   - Generate leads
   - Examine user behavior
2. Click "Create"
3. Accept the Terms of Service

### Step 5: Get Your Measurement ID

1. You'll be prompted to set up a data stream
2. Choose **Web**
3. **Website URL:** `https://dbwaterheater.com`
4. **Stream name:** `DB Water Heater Website`
5. Click "Create stream"
6. **Copy your Measurement ID** (it starts with `G-` followed by letters and numbers, like `G-ABC123XYZ`)

### Step 6: Update All HTML Files

Replace `G-XXXXXXXXXX` with your real Measurement ID in these 5 files:

1. `/index.html` (line ~43-48)
2. `/services/water-heater-replacement.html` (line ~43-48)
3. `/services/tankless-water-heater-installation.html` (line ~43-48)
4. `/services/emergency-no-hot-water.html` (line ~43-48)
5. `/legal/privacy.html` (line ~14-19)

**Find and replace:**
- Old: `G-XXXXXXXXXX`
- New: Your actual Measurement ID (e.g., `G-ABC123XYZ`)

### Step 7: Verify Tracking

1. Save and commit your changes
2. Push to GitHub (CloudFlare Pages will automatically deploy)
3. Wait 2-3 minutes for deployment
4. Go to Google Analytics → Reports → Realtime
5. Visit your website: https://dbwaterheater.com
6. You should see yourself as an active user in the Realtime report

---

## Google Search Console Setup

### Step 1: Add Your Property

1. Go to https://search.google.com/search-console
2. Sign in with the same Google account as Analytics
3. Click "Add property"
4. Choose **URL prefix**
5. Enter: `https://dbwaterheater.com`
6. Click "Continue"

### Step 2: Verify Ownership

**Method 1: HTML tag (Recommended)**

1. Google will show you an HTML meta tag
2. Copy the entire tag (looks like `<meta name="google-site-verification" content="...">`)
3. Add it to the `<head>` section of your `index.html` file (after line 40)
4. Commit and push changes
5. Wait 2-3 minutes for CloudFlare Pages to deploy
6. Click "Verify" in Search Console

**Method 2: Google Analytics**

1. If you've already set up GA4 above, choose "Google Analytics"
2. Select your GA4 property
3. Click "Verify"

### Step 3: Submit Sitemap

1. In Search Console, go to **Sitemaps** (left sidebar)
2. Enter: `sitemap.xml`
3. Click "Submit"
4. Status should change to "Success" within a few hours

---

## Event Tracking (Optional Enhancement)

To track phone calls and SMS clicks, add this code to your `index.html` before the closing `</body>` tag:

```html
<!-- Event Tracking for Phone & SMS -->
<script>
  // Track phone call clicks
  document.querySelectorAll('a[href^="tel:"]').forEach(link => {
    link.addEventListener('click', () => {
      gtag('event', 'phone_call_click', {
        'event_category': 'engagement',
        'event_label': 'Phone: ' + link.textContent.trim()
      });
    });
  });

  // Track SMS clicks
  document.querySelectorAll('a[href^="sms:"]').forEach(link => {
    link.addEventListener('click', () => {
      gtag('event', 'sms_click', {
        'event_category': 'engagement',
        'event_label': 'Text Message'
      });
    });
  });
</script>
```

This will help you track:
- How many people click the phone number
- How many people click the text message button
- Which pages generate the most engagement

---

## Important Notes

### Privacy Compliance

- ✅ Analytics disclosure has been added to your Privacy Policy
- ✅ You're using Google Analytics' default privacy settings (anonymous IP tracking)
- ✅ No cookies banner required for GA4 basic implementation in California

### Data Retention

- Google Analytics 4 default: 2 months of user-level data
- To change: Admin → Data Settings → Data Retention → Select 14 months

### What to Monitor

**Weekly:**
- Realtime users (are people finding your site?)
- Traffic sources (where are visitors coming from?)
- Top pages (which service pages are most popular?)

**Monthly:**
- User trends (is traffic growing?)
- Conversion events (phone/SMS clicks if event tracking is enabled)
- Geographic data (where are your visitors located?)

---

## Troubleshooting

### "No data received" in Google Analytics

1. Check that you replaced `G-XXXXXXXXXX` in all 5 files
2. Verify CloudFlare Pages deployed the latest changes
3. Clear your browser cache and visit the site
4. Check browser console for JavaScript errors (F12 → Console tab)
5. Wait 24-48 hours (sometimes data takes time to appear)

### Sitemap not found in Search Console

1. Verify sitemap exists: https://dbwaterheater.com/sitemap.xml
2. Check that CloudFlare Pages deployed the `sitemap.xml` file
3. Try resubmitting after 24 hours

### Can't verify ownership in Search Console

1. Make sure the HTML tag is in the `<head>` section
2. Verify CloudFlare Pages deployed the changes
3. Try the Google Analytics verification method instead

---

## Next Steps After Setup

1. **Set up Google Business Profile** (critical for local SEO)
   - Go to https://business.google.com
   - Add your business location
   - Verify via postcard

2. **Link Analytics to Ads** (if you plan to run Google Ads)
   - Admin → Property → Google Ads Links

3. **Create custom reports** for leads
   - Focus on phone/SMS click events
   - Track which pages drive the most conversions

---

## Contact Information

**Business:** Doughty Brothers Water Heater
**Phone:** (415) 424-5964
**Email:** dbwaterheater@gmail.com
**License:** 714897
**Website:** https://dbwaterheater.com

---

*Last updated: January 2, 2026*
