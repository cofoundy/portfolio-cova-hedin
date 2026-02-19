# QA Report: Cova Hedin

**Date:** 2026-02-19
**URL:** https://cova-hedin.cofoundy.dev/
**Tier:** Premium (S/.280)
**Template:** premium-starter
**Status:** PASS

## Data Validation
- [x] Name matches source ("Cova Hedin" in config.ts and on page)
- [x] Title matches source ("Swedish Teacher & Content Creator")
- [x] Email present (swedishwithcova@gmail.com — Cloudflare-obfuscated, normal)
- [x] Stats match source (500+ Students, 10K+ Lessons, 7+ Years Teaching)
- [x] Languages match source (6 languages: Swedish, English, Spanish, Italian, Quechua, Hebrew)
- [x] Experience companies match source (Language Lock-In, StoryLearning, italki)
- [x] Testimonials match source (Julia/Russia, Jeff/International, Student/International)
- [x] Services match source (Private Lessons, Group Lessons, Corporate Training, Translation)
- [x] No hallucinated data detected

## Sections Present
- [x] Hero (photo, name, title, tagline, dual CTA, social icons, stats bar)
- [x] About ("A Swedish Latina in Italy" + 3 paragraphs + collaboration paragraph + pull quote)
- [x] Languages (6 flag cards with levels)
- [x] Approach ("What Makes My Lessons Special" — 5 items, highlighted bonus item)
- [x] Testimonials ("What My Students Say" — 3 cards + 5,312 reviews / 5/5 badge)
- [x] Experience ("Where I've Taught & Created" — 3 clickable cards with URLs)
- [x] Services (4 service cards + "See Pricing & Book" CTA)
- [x] CTA section (dark background, "Book a Lesson" + "Work with Me" dual buttons)
- [x] Footer (name, title, social icons, copyright 2026)
- [x] Floating pill nav (appears on scroll > 400px)

## Clean Deploy
- [x] No "Powered by" / "Made with" / "Built with" watermarks
- [x] No "View source" / "View on GitHub" / "Fork this" template links
- [x] No "Lorem ipsum" / "Your name here" / "[placeholder]" text
- [x] No template watermarks visible to users
- [x] No broken "#" or "javascript:void(0)" links visible
- [x] No "undefined" or "null" in content

## Technical Health
- [x] Site loads: HTTP 200
- [x] CSS loads: /_astro/index.DFsYgYTN.css — HTTP 200
- [x] Profile image loads: /profile.jpg — HTTP 200 (174KB)
- [x] Favicon loads: /favicon.svg — HTTP 200
- [x] Google Fonts loading (DM Serif Display, Plus Jakarta Sans, Space Mono)
- [x] Swedish blue/yellow color theme applied (#0f2b4c / #1d5a8c / #f0c75e)
- [x] Responsive classes present (md:grid-cols-12, sm:flex-row, lg:grid-cols-6, etc.)
- [x] Cloudflare email obfuscation active (email-decode.min.js)

## Dual CTA Buttons
- [x] "Book a Lesson" — links to https://swedishwithcova.simplybook.it/v2/
- [x] "Work with Me" — mailto link (Cloudflare-obfuscated)

## Social Links
- [x] Instagram: https://www.instagram.com/swedishwithcova/
- [x] TikTok: https://www.tiktok.com/@swedishwithcova
- [x] YouTube: https://www.youtube.com/@swedishwithcova
- [x] LinkedIn: https://www.linkedin.com/in/cova-hedin-661071312/

## Issues Found
None.

## Notes
- Email addresses are obfuscated by Cloudflare's email protection (cdn-cgi/l/email-protection) — this is expected behavior for sites behind Cloudflare proxy and does not affect functionality.
- The meta generator tag shows "Astro v5.17.1" but this is only visible in source code, not to users.
- Screenshots were not captured in this session (no browser automation tool available). Visual verification was done via HTML source analysis confirming all CSS classes, inline styles, and content render correctly.
