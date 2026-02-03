# Stratton Digital Systems Website

Custom-built, performance-first marketing website for Stratton Digital Systems.  
Designed specifically for service-based businesses that rely on calls, contact forms, and local visibility.

This site replaces a previous Squarespace build and is intentionally lightweight, fast, and easy to maintain.

---

## Overview

- **Framework:** Astro (static output)
- **Hosting:** Cloudflare Pages
- **Deployment:** GitHub → Cloudflare Pages (CI/CD)
- **Forms:** Formspree
- **Styling:** Custom CSS (no UI frameworks)
- **JavaScript:** Minimal, only where necessary
- **CMS:** None (static by design)

The site prioritizes:
- Speed and Core Web Vitals
- Mobile-first usability
- Clear calls-to-action
- Long-term maintainability

---

## Project Structure

/
├─ public/
│ ├─ brand/
│ │ └─ sds-logo.webp
│ └─ favicon.png
│
├─ src/
│ ├─ components/
│ │ ├─ Header.astro
│ │ └─ Footer.astro
│ │
│ ├─ layouts/
│ │ └─ BaseLayout.astro
│ │
│ ├─ pages/
│ │ ├─ index.astro
│ │ ├─ services.astro
│ │ ├─ process.astro
│ │ ├─ contact.astro
│ │ └─ thanks.astro
│ │
│ └─ styles/
│ └─ global.css
│
├─ astro.config.mjs
├─ package.json
└─ README.md

---

## Design Philosophy

### Why Astro
- Ships zero JavaScript by default
- Excellent Lighthouse and Core Web Vitals scores
- Simple component model with no runtime overhead
- Ideal for static marketing sites

### Why No CMS
- Content does not change frequently
- Avoids vendor lock-in and admin overhead
- Reduces attack surface
- Faster builds and simpler hosting

A CMS can be added later if requirements change.

---

## Performance Strategy

- Static HTML output
- No JS frameworks
- No client-side routing
- CSS-only animations
- Optimized images (`.webp`)
- CDN-backed delivery via Cloudflare

The site is intentionally built to score high 90s to 100 on Lighthouse mobile.

---

## Mobile Navigation

- **Desktop:** Inline navigation with primary CTA
- **Mobile:** Hamburger menu using native `<details>` / `<summary>`
- No JavaScript required
- No wrapping or duplicated CTAs

This avoids common mobile header issues while remaining accessible and lightweight.

---

## Forms

- Powered by Formspree
- No backend required
- Spam protection enabled
- Minimal JavaScript for form reset on submit
- Default Formspree thank-you page is acceptable by design

### Forms Deployment

- Powered by Formspree
- No backend required
- Spam protection enabled
- Minimal JavaScript for form reset on submit
- Default Formspree thank-you page is acceptable by design

--- 

## Deployment

- Hosted on Cloudflare Pages
- Auto-deploys from the main branch
- Build command: npm run build
- Output directory: dist

### Domain

- DNS managed by Cloudflare
- Apex and www both point to the Pages project
- Squarespace is no longer used for hosting

## SEO

- Clean semantic HTML
- Page-level titles and meta descriptions
- Mobile-first layout
- Fast load times
- Proper heading hierarchy
- Search engine indexing is expected to normalize following DNS cutover.

## Maintenance Notes

- Global styles live in src/styles/global.css
- Header and footer are shared components
- Layout issues should be fixed at the CSS or component level
- Avoid adding libraries unless absolutely necessary

## License

Private project.
All rights reserved © Stratton Digital Systems.