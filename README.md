# NutriSmart — Website

Static marketing/landing site for **NutriSmart**, the smart-nutrition platform that
adapts meal recommendations to your location, weather, and health profile so you can
lose weight or gain muscle on your own terms.

Built with plain **HTML, CSS, and vanilla JavaScript** — no framework, no build step.

## Pages

| Page            | File             | Content                                              |
|-----------------|------------------|------------------------------------------------------|
| Home / Landing  | `index.html`     | Hero carousel, value proposition, feature highlights |
| Features        | `features.html`  | Smart Scan, global/contextual recommendations, etc.  |
| About Us        | `about-us.html`  | Product story and team                               |
| Contact         | `contact.html`   | Contact form                                         |
| Terms           | `terms.html`     | Terms and conditions                                 |

## Features

- **Bilingual (i18n):** English (`en_US`, default) and Latin-American Spanish (`es_419`).
  Handled by `js/i18n.js`; the choice is persisted in `localStorage` and applied to any
  element carrying `data-i18n`, `data-i18n-placeholder`, or `data-i18n-aria`.
- **Responsive navigation** with hamburger drawer and overlay backdrop.
- **Hero carousel**, **FAQ accordion**, and **contact form** — all initialized in
  `js/main.js` on `DOMContentLoaded`.
- **Optimized assets:** all images served as `.webp`, plus an Open Graph image
  (`assets/images/og-image.webp`) for social sharing.

## Project structure

```
nutrismart-website/
├── index.html            # Home
├── features.html
├── about-us.html
├── contact.html
├── terms.html
├── css/
│   └── styles.css        # All site styles
├── js/
│   ├── i18n.js           # Translation engine + en/es strings
│   └── main.js           # Nav, carousel, FAQ, contact form
└── assets/
    └── images/           # .webp images (hero, features, logos, OG)
```

## Running locally

No build or dependencies. Serve the folder with any static server, e.g.:

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

Then open <http://localhost:8000>. Opening `index.html` directly via `file://` also
works, though a local server is recommended so relative paths and `localStorage`
behave consistently.

## Deployment

Being fully static, the site can be hosted on any static host (GitHub Pages, Netlify,
Vercel, S3/CloudFront, Nginx) by publishing the repository contents as-is.

## Related repositories

- `nutrismart-platform` — backend (Spring Boot / DDD).
- `nutrismart-webapp` — web application (Angular).
