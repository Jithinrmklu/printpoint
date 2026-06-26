# Print Point — Project Continuation File

## Current Status

**Phase:** Not started — `index.html` has NOT been generated yet.

The original prompt was received and acknowledged. The working directory
(`/Users/jithinramapurath/code/printpoint/`) was confirmed empty. The
assistant began writing a response but was interrupted before any file was
written. **No code exists yet.**

---

## Files Generated

| File | Status |
|------|--------|
| `index.html` | ❌ Not created |
| `CONTINUATION.md` | ✅ This file |

---

## Design Decisions (Pre-planned)

### Stack
- Pure HTML5 — single `index.html`, zero build tools
- Tailwind CSS via CDN (`https://cdn.tailwindcss.com`)
- Google Fonts: Poppins (headings) + Inter (body) via `<link>` tag
- Lucide Icons via CDN (`https://unpkg.com/lucide@latest`)
- Vanilla JavaScript only — for scroll animations, counter, mobile menu

### Color Palette
```
Primary:    #DC2626  (red)
Secondary:  #2563EB  (blue)
Accent:     #F59E0B  (amber)
Background: #FFFFFF
Text:       #0F172A
Light BG:   #F8FAFC
```

### Typography Scale
- Display/Hero: Poppins 700, 5xl–7xl
- Section titles: Poppins 700, 3xl–4xl
- Subheadings: Poppins 600, xl–2xl
- Body: Inter 400/500, base–lg

### Design Aesthetic
- Inspired by: Apple, Stripe, Canva, VistaPrint, Linear
- Glassmorphism cards (backdrop-blur, semi-transparent bg)
- Gradient mesh backgrounds in hero and stats sections
- Subtle geometric SVG decorations (circles, grids, blobs)
- Scroll-reveal animations via IntersectionObserver (no library)
- Counter animation triggered when stats section enters viewport
- Sticky nav with blur-on-scroll effect

### No-SVG-image approach
Because this is a static single file with no network assets, decorative
"illustrations" are built from pure CSS shapes and Tailwind utilities
(gradient blobs, geometric grids, icon clusters) — no `<img>` tags that
would 404. Portfolio gallery uses color-gradient placeholder tiles with
Lucide icons and descriptive labels.

---

## Planned Sections (in order)

1. **`<head>`** — SEO meta, OG tags, Twitter card, JSON-LD LocalBusiness schema,
   Google Fonts, Tailwind CDN, Lucide CDN, inline Tailwind config for custom
   colors, custom CSS for animations

2. **Navigation** — sticky, blur-on-scroll, hamburger menu for mobile,
   smooth-scroll links

3. **Hero** — full-height, gradient mesh bg, large headline, subheadline,
   three CTA buttons (Call / WhatsApp / Explore Services), four stat pills,
   decorative CSS illustration cluster

4. **About** — two-column layout, paragraph copy, six icon-feature cards
   (Creative Designs, Premium Quality, Affordable Pricing, Fast Delivery,
   Personalised Service, Customer Satisfaction)

5. **Services** — six service category cards in a responsive grid
   (Graphic Design, Printing Services, Photo & Gift, Business Branding,
   Festival & Event, Custom Printing), each card expands a bullet list

6. **Portfolio** — masonry/CSS-grid gallery, 12 tiles with gradient
   backgrounds, Lucide icons, hover-scale + overlay reveal effect

7. **Why Choose Us** — eight feature cards in a 4×2 grid

8. **Impact / Stats** — dark gradient section, four animated counters
   (1000+ / 5000+ / 10+ / 100+)

9. **How We Work** — alternating-side timeline, six steps

10. **Testimonials** — three testimonial cards with star ratings and
    avatar initials

11. **Contact & Location** — two-column: info block (address, phone,
    WhatsApp CTA, business hours) + Google Maps `<iframe>`

12. **Footer** — four-column layout (brand, quick links, services, contact),
    copyright bar

---

## Remaining Tasks

- [ ] Write the complete `index.html` (~1 200–1 800 lines)
- [ ] Verify all Tailwind utility classes render correctly (CDN play mode)
- [ ] Confirm Lucide icon names are valid against the v0.x API
- [ ] Test responsive breakpoints (sm / md / lg / xl) mentally
- [ ] Check all `href="tel:+919745397910"` and `href="https://wa.me/919745397910"` links
- [ ] Validate JSON-LD schema syntax
- [ ] Confirm Google Maps embed URL is generic/works without API key
  (standard `maps.google.com/maps?q=...&output=embed` URL)

---

## Technology Constraints (Hard Rules)

- **Single file only** — everything inline in `index.html`
- **No npm / Node / build step** — open file directly in browser
- **No React / Vue / Angular / TypeScript**
- **No backend, forms, login, payment, chat widgets**
- **No external image URLs** — all visuals are CSS / SVG / icon-based
- **No jQuery** — vanilla JS only
- **Buttons may only**: call the business, open WhatsApp, or scroll to a section
- Tailwind config must be done via `tailwind.config` in the CDN script tag
  (not a separate config file) to keep the single-file constraint

---

## Exact Prompt to Continue

Paste the following message verbatim into a new Claude Code session (in the
same working directory `/Users/jithinramapurath/code/printpoint/`):

---

```
Continue building the Print Point website.

Status: `index.html` has NOT been created yet. The directory is empty except
for CONTINUATION.md.

Read CONTINUATION.md for the full design spec. Then create the complete
`index.html` now — all sections, all content, no placeholders.

Key reminders from the spec:
- Single HTML file, Tailwind CDN, Google Fonts (Poppins + Inter), Lucide CDN
- Colors: Primary #DC2626 | Secondary #2563EB | Accent #F59E0B | BG #FFFFFF | Text #0F172A
- No backend, no forms, no login. Buttons only call/WhatsApp/scroll.
- No external image URLs — use CSS gradients + Lucide icons for all visuals.
- All 12 sections from CONTINUATION.md must be present and complete.
- Include JSON-LD LocalBusiness schema, OG tags, Twitter card meta.
- Phone: +91 97453 97910 | WhatsApp: same number | Address: Bus Stand, Near Cherupuzha, Kerala 670511
- Scroll-reveal via IntersectionObserver, counter animation on stats section.
- Design feel: Apple + Stripe + Canva. Premium, clean, modern, colorful.

Write the file. Do not stop partway through.
```

---

## Notes

- The Google Maps embed should use the address "Bus Stand, Cherupuzha,
  Kerala 670511" in a standard embed URL (no API key required for basic
  embed iframes).
- Business hours are not specified in the brief; use reasonable defaults
  for a Kerala print shop: Mon–Sat 9 AM – 8 PM, Sun 10 AM – 6 PM.
- Testimonials are illustrative (no real customer names given); use
  initials-based avatars (e.g., "R.K.", "A.M.", "S.P.") and keep them
  general/positive per the brief examples.
- The portfolio section intentionally uses styled placeholder tiles because
  real print files are not available — this is documented in the design
  decisions above so a future maintainer understands the intent.
