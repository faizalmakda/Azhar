# Sterling Consultancy — Website

Marketing website for **Sterling Consultancy** (working name — subject to change once
the domain is confirmed).

> *Operational Leadership for Financial Services — Finance · Strategy · Transformation · AI*

## Status

First-pass, single-page marketing site. Built as **dependency-free static HTML/CSS** so it:

- previews instantly (just open `index.html`),
- hosts anywhere for free (GitHub Pages / Netlify / Vercel) — no build step, no domain needed,
- re-brands trivially when the final name is chosen.

## Structure

```
index.html          # the whole site (one-page scroll)
assets/
  styles.css        # all styling; brand palette defined once at the top (:root)
  logo-mark.svg     # placeholder S + skyline mark (logo is "subject to change")
```

## Brand palette

| Token | Hex | Use |
|-------|-----|-----|
| Deep Navy | `#0B1D33` | Primary / backgrounds |
| Brushed Gold | `#C79A4A` | Accent / CTAs |
| Platinum | `#D9DADF` | Secondary detail |
| Pure White | `#FFFFFF` | Base |

Fonts: **Cormorant Garamond** (display serif) + **Montserrat** (sans) via Google Fonts,
with system fallbacks.

## Renaming later (when the domain lands)

The name appears in a small, known set of places:
- `index.html` — `<title>`, brand blocks, footer, contact email
- `assets/styles.css` — the `:root` palette (colours only; no name)
- `README.md`

A find-and-replace of "Sterling Consultancy" plus the email/domain is all that's needed.

## Placeholders to confirm

- **Contact email** (`index.html` → `#contact`) — currently `hello@sterlingconsultancy.com`.
- **Real content** — services copy is written to be credible for a FS consultancy but should
  be reconciled against the old site (`realassetsolutions.co.uk`) and the client's own wording.
- **Logo** — SVG is a placeholder approximation of the brand mark.

## Roadmap (post-domain)

- [ ] Confirm final name + register domain
- [ ] Swap in real logo files
- [ ] Fold in real content from the previous site / client
- [ ] Add About / Team and per-sector or per-service detail pages
- [ ] Wire up a real contact form (or `mailto:`) + branded email
- [ ] Deploy to a live host and point DNS
- [ ] SEO metadata, OG image, analytics, cookie/privacy pages
