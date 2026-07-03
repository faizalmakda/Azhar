# Sterling Consultancy — Website

Marketing website for **Sterling Consultancy** (working name — subject to change once
the domain is confirmed).

> *Operational Leadership for Financial Services — Finance · Strategy · Transformation · AI*

## Status

Multi-page marketing site, built as **dependency-free static HTML/CSS** so it:

- previews instantly (just open `index.html`),
- hosts anywhere for free (GitHub Pages / Netlify / Vercel) — no build step, no domain needed,
- re-brands trivially when the final name is chosen.

## Pages

| File | Page |
|------|------|
| `index.html` | Home — hero, positioning, services overview, approach, global reach, CTA |
| `services.html` | What We Do — the six services in detail |
| `about.html` | About — story, approach, sectors, team (placeholder) |
| `contact.html` | Contact — "Let's discuss your requirements" form |
| `assets/styles.css` | All styling; brand palette defined once at the top (`:root`) |
| `assets/logo-mark.svg` | Placeholder S + skyline mark (logo is "subject to change") |

## Live preview (GitHub Pages)

`.github/workflows/deploy.yml` publishes the site to a free `*.github.io` URL on every push
to the working branch. **One-time setup** (needs a repo admin, ~30 seconds):

1. GitHub → repo **Settings → Pages**
2. Under **Build and deployment → Source**, choose **GitHub Actions**
3. Re-run the "Deploy site to GitHub Pages" workflow (Actions tab) — or just push again

The live URL then appears in the workflow run summary and under Settings → Pages.
*If the run fails with an environment/branch protection error, either allow this branch in
the `github-pages` environment (Settings → Environments) or merge the branch to `main`.*

## Brand palette

| Token | Hex | Use |
|-------|-----|-----|
| Deep Navy | `#0B1D33` | Primary / backgrounds |
| Brushed Gold | `#C79A4A` | Accent / CTAs |
| Platinum | `#D9DADF` | Secondary detail |
| Pure White | `#FFFFFF` | Base |

Fonts: **Cormorant Garamond** (display serif) + **Montserrat** (sans) via Google Fonts,
with system fallbacks.

## Placeholders to confirm

- **Company name** — "Sterling Consultancy" throughout (final name pending domain).
- **Contact email** — `hello@sterlingconsultancy.com` (placeholder).
- **Team** (`about.html`) — names/roles/bios are placeholders, marked *subject to change*.
- **Story** (`about.html`) — draft heritage narrative, marked *subject to change*.
- **Logo** — SVG is a placeholder approximation of the brand mark.
- **Contact form** — needs an endpoint to actually send (see below). Falls back to `mailto:` for now.

### Wiring the contact form (once hosting is chosen)

- **Netlify:** add `netlify` attribute to the `<form>` tag — forms work automatically.
- **Formspree:** set `action="https://formspree.io/f/XXXX"` and `method="POST"`.

## Renaming later (when the domain lands)

Find-and-replace "Sterling Consultancy" + the email/domain across the `.html` files. Colours
live only in `assets/styles.css` (`:root`); the name never appears there.

## Roadmap (post-domain)

- [ ] Confirm final name + register domain
- [ ] Swap in real logo files
- [ ] Add real team names/bios and finalise the story
- [ ] Wire up the contact form + branded email
- [ ] Point a custom domain at the deployment (add `CNAME`)
- [ ] SEO metadata, OG image, analytics, cookie/privacy pages
