# Indus Commercial Merchants — Website

Marketing website for **Indus Commercial Merchants** (legal entity: Indus Mercantile (Pvt) Limited), a Pakistan-based commercial import, export and freight-forwarding partner connecting China, Pakistan, the UK, the USA and Europe.

Built as a static, single-page site — no build step, no dependencies.

## Structure

```
.
├── index.html          # all page content/sections
├── assets/
│   ├── style.css        # brand tokens + layout
│   └── hero-trade.jpg   # hero image
└── README.md
```

## Sections

- Hero — headline, CTAs, office locations
- Who We Are — core capabilities, who we serve, core trade lanes
- What Importers Need Solved — the pain points this business addresses
- End-to-End Service Offering — the 6-step process + operational support checklist
- Why Indus Commercial Merchants — differentiators + best-fit customer types
- How We Work With You — 5-step engagement model
- Contact — direct email / phone / WhatsApp links (static, no backend)

## Local preview

```
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. In **Settings → Pages**, set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`.
3. The site will be published at `https://<username>.github.io/<repo>/`.

## Custom domain — indusmercantile.com

This repo includes a `CNAME` file already set to `indusmercantile.com`, which is what tells
GitHub Pages to serve the site on that domain instead of the default `github.io` URL.
Two things still need to happen on the domain side:

1. **At your domain registrar**, add these DNS records for the apex domain (`indusmercantile.com`):

   | Type | Host | Value |
   |------|------|---------------------------|
   | A    | @    | 185.199.108.153 |
   | A    | @    | 185.199.109.153 |
   | A    | @    | 185.199.110.153 |
   | A    | @    | 185.199.111.153 |

   (Optional, for `www.indusmercantile.com` to also work) add:

   | Type  | Host | Value                  |
   |-------|------|------------------------|
   | CNAME | www  | `<username>.github.io` |

2. **In the repo's Settings → Pages**, under "Custom domain" enter `indusmercantile.com` and save
   (GitHub will verify DNS — this can take a few minutes to a few hours to propagate). Once verified,
   tick **Enforce HTTPS**.

DNS changes are made at whichever registrar the domain was purchased through — not from this repo.

## Content source

Copy is taken from the company's own pitch deck and business card (offices, services, process, contact details). Update `index.html` directly to change copy; brand colors and spacing live in `assets/style.css` as CSS custom properties at the top of the file.
