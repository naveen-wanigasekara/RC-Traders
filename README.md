# RC Traders (Pvt) Ltd — Landing Page

Company landing page for RC Traders (Pvt) Ltd, a Sri Lankan importer and supplier of genuine
vehicle spare parts sourced directly from Japan and Australia. Body parts, lighting components,
accessories, and a custom import/sourcing service.

**Live site:** https://rctraders.netlify.app/

## Tech stack

Single-file static site — one `index.html` with inline CSS and vanilla JS. No build step, no
framework, no dependencies. Deployed as-is to Netlify.

## Project structure

```
index.html          the entire site (markup, styles, scripts)
images/
  hero.jpg           hero banner photo
  about.jpg          warehouse/storefront photo
  gallery-1.jpg       gallery: storefront
  gallery-2.jpg       gallery: parts shelf
  gallery-3.jpg       gallery: headlight close-up
  gallery-4.jpg       gallery: delivery/fitting
  *.svg               brand-styled illustrated fallback for each photo above
```

### Image fallback behavior

Each image slot tries its real photo first (e.g. `images/hero.jpg`). If that file is missing or
fails to load, it automatically falls back to a hand-built gold/black SVG illustration of the same
name (`images/hero.svg`), so the site never shows a broken image. To update a photo, just replace
the `.jpg` file with the same name — no HTML changes needed.

## Local development

No build step required. Either:

```bash
open index.html
```

or serve it locally:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

The site is deployed on Netlify and linked to this GitHub repository for continuous deployment —
every push to `main` triggers an automatic rebuild and deploy. No manual re-upload needed.

## Editing content

All copy, contact details, and section content live directly in `index.html` — there's no CMS or
data file. Key things to know:

- **Contact info**: phone/WhatsApp number, address, and hours are in the header, hero, and contact
  section. The WhatsApp number is in international format (`94718876210`) wherever it's used as a
  link.
- **Enquiry form**: has no backend — on submit, it builds a `wa.me` deep link from the form fields
  and opens WhatsApp directly.
- **Testimonials**: currently placeholder sample reviews. Replace with real customer quotes
  (Google/Facebook reviews) when available.
- **Map**: the contact section embeds Google Maps using exact coordinates (not an address text
  query, which can geocode incorrectly) — see the `iframe src` in the Contact section.

## Company details

- **Company:** RC Traders (Pvt) Ltd
- **Reg. No.:** PV 00302151
- **Address:** No. 74/1, Weliamuna Road, Hendala, Wattala 11300, Sri Lanka
- **Tel/WhatsApp:** 071 8876 210
- **Director:** Roshen Chathuranga
