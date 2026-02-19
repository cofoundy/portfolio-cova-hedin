# QA Report: Cova Hedin

**Date:** 2026-02-19
**URL:** https://cova-hedin.cofoundy.dev/
**Original URL tested:** https://cova-hedin.cofoundy.dev/portfolio-cova-hedin/ (404)
**Status:** FAIL

## Data Validation
- [x] Name matches source ("Cova Hedin" -- correct, no "Joceline")
- [x] Title matches source ("Swedish Teacher & Content Creator")
- [x] Stats match source (500+ Students, 10K+ Lessons, 7+ Years Teaching)
- [x] Companies match source (Language Lock-In, StoryLearning, italki)
- [x] Testimonials match source (Julia/Russia, Jeff/International, Student/International)
- [x] Booking URL correct (swedishwithcova.simplybook.it/v2/)
- [x] Social links correct (Instagram, TikTok, YouTube, LinkedIn)
- [x] Languages correct (6 languages with flags)
- [x] About section matches source (Gothenburg, Latin American father, Italy)
- [x] Email obfuscated by Cloudflare (expected behavior)
- [x] No hallucinated data detected

## Clean Deploy
- [x] No "Powered by" / "Made with" / "Built with" watermarks
- [x] No placeholder text (Lorem ipsum, "Your name here", etc.)
- [x] No template links (View source, Fork this, etc.)
- [x] No "undefined" or "null" visible in content
- [x] No Astro logo, Vercel badge, or other template branding visible

## Technical
- [!] CSS FAILS to load (HTTP 404) -- CRITICAL
- [!] Profile image FAILS to load (HTTP 404) -- CRITICAL
- [!] Favicon FAILS to load (HTTP 404) -- CRITICAL
- [x] Actual assets exist at root paths (200 OK)
- [x] Google Fonts load correctly
- [x] HTML content renders with correct data

## Issues Found

### CRITICAL: `base` path not removed for custom subdomain

**Root Cause:** `astro.config.mjs` still has `base: "/portfolio-cova-hedin"` but the site is deployed to a custom subdomain (`cova-hedin.cofoundy.dev`). This causes Astro to prefix all asset paths with `/portfolio-cova-hedin`, but since the custom domain serves content at root, all assets 404.

**Broken paths in HTML:**
1. CSS: `href="/portfolio-cova-hedin/_astro/index.jM3tbj04.css"` --> 404
2. Favicon: `href="/portfolio-cova-hedinfavicon.svg"` --> 404 (also missing slash between base and filename)
3. Profile image: `src="/portfolio-cova-hedinprofile.jpg"` --> 404 (also missing slash between base and filename)
4. OG image: `content="/portfolio-cova-hedinprofile.jpg"` --> 404

**Correct paths (all return 200):**
1. CSS: `/_astro/index.jM3tbj04.css`
2. Favicon: `/favicon.svg`
3. Profile image: `/profile.jpg`

**User Impact:** The page loads as unstyled raw HTML with no CSS, no profile photo, and no favicon. The site is essentially broken for end users.

### SECONDARY: Missing slash in base path concatenation

Even if `base` were needed, the favicon and profile image paths show `/portfolio-cova-hedinfavicon.svg` instead of `/portfolio-cova-hedin/favicon.svg` -- indicating a bug in how the template concatenates the base path with static asset filenames.

### FIX REQUIRED:

```javascript
// astro.config.mjs -- CHANGE FROM:
site: "https://cofoundy.github.io",
base: "/portfolio-cova-hedin",

// TO:
site: "https://cova-hedin.cofoundy.dev",
// REMOVE base property entirely
```

Then rebuild and redeploy:
```bash
npm run build
npx gh-pages -d dist --dotfiles --repo "https://github.com/cofoundy/portfolio-cova-hedin.git"
```

## Content Verification Summary

| Item | Source (config.ts) | Page | Match |
|------|-------------------|------|-------|
| Name | Cova Hedin | Cova Hedin | YES |
| Title | Swedish Teacher & Content Creator | Swedish Teacher & Content Creator | YES |
| Stat 1 | 500+ Students | 500+ Students | YES |
| Stat 2 | 10K+ Lessons | 10K+ Lessons | YES |
| Stat 3 | 7+ Years Teaching | 7+ Years Teaching | YES |
| Booking | swedishwithcova.simplybook.it/v2/ | swedishwithcova.simplybook.it/v2/ | YES |
| Instagram | instagram.com/swedishwithcova | Present | YES |
| TikTok | tiktok.com/@swedishwithcova | Present | YES |
| YouTube | youtube.com/@swedishwithcova | Present | YES |
| LinkedIn | linkedin.com/in/cova-hedin-661071312/ | Present | YES |
| Languages | 6 (SE, GB, ES, IT, PE, IL) | 6 flags present | YES |
| Testimonials | Julia, Jeff, Student | All 3 present | YES |
| Experience | Language Lock-In, StoryLearning, italki | All 3 present | YES |

## Sections Present
- [x] Hero (with tagline, dual CTA, social icons, stats bar)
- [x] About (with pull quote)
- [x] Languages (6 flags)
- [x] Approach (5 items, 1 highlighted)
- [x] Testimonials (3 reviews, 5312 count, 5/5 rating)
- [x] Experience (3 roles)
- [x] Services (4 cards)
- [x] CTA section
- [x] Footer
- [x] Floating pill nav

## Evidence
- No screenshots taken (site renders without CSS due to critical asset loading failure)

## Recommendation
FAIL -- Must fix `astro.config.mjs` by removing `base` property and updating `site` to custom domain URL, then rebuild and redeploy before delivery.
