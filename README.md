# Triya Eventz — triyaeventz.com

Static one-page site. No build step, no dependencies.

## Deploy to Vercel

1. Push this folder to a GitHub repo (contents at the repo root).
2. In Vercel, import the repo.
   - Framework Preset: **Other**
   - Build Command: leave empty
   - Output Directory: leave empty (or `.`)
3. Add `triyaeventz.com` under Settings → Domains.

If you keep this folder nested inside a larger repo, set Vercel's **Root Directory** to `site`.

## Files

```
index.html          the whole page
robots.txt          allows all crawlers, points at the sitemap
sitemap.xml         single URL
assets/
  triya-logo.png    favicon, apple-touch-icon, closing mark
  kids-safari.jpg   spread 03 — real Triya work, from the safari reel
  og-image.jpg      1200x630 link preview card
```

## Before it goes live

**Three images are hotlinked from another company's Wix CDN** (the hero and spreads 01 and 02).
They load, but they are placeholders on someone else's server and can disappear without warning.
Replace them with Triya's own photography. Search `static.wixstatic.com` in `index.html` — three hits.

Recommended sizes: hero 1920×1080 landscape, spreads 1400×1050 (4:3).

## Not yet included

- **No contact route except Instagram.** Every CTA opens a DM. Add a WhatsApp click-to-chat link
  (`https://wa.me/91XXXXXXXXXX?text=...`) and a `tel:` link once there's a business number.
- **No Google Business Profile.** This is the main driver of local search in Hyderabad.
  Create one, then add `telephone`, `openingHours` and the full `address` to the JSON-LD
  block in `index.html`.
- **No analytics.** Vercel Analytics is one toggle in the dashboard if you want traffic numbers.

## Editing copy

All text is plain HTML in `index.html` — no templating. The three portfolio spreads are
`<article class="spread">` blocks; the occasions list is `<div class="occasion">` blocks.
