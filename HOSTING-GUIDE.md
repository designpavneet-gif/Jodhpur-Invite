# Wedding & House Warming Dinner — hosting guide

Invitation to the **Wedding & House Warming Dinner** of Manmeet Singh and Simranjeet Kaur —
Sunday, 13 December 2026 · 7:30 PM · Adarsh Vatika, Jodhpur (the date and time are highlighted
on the parchment scroll).

```
website/                      ← the complete website (recommended)
invitation-single-file.html   ← the whole site in ONE file (alternative)
HOSTING-GUIDE.md              ← this file
```

This edition has the RSVP section (family welcome and Ira's note) **without the form** —
nothing to connect, no Google Sheet involved.

## Option A — upload the `website` folder (recommended)

Upload the **contents** of `website/` to any static host. It works at a domain root or in a sub-folder,
so it can live next to the main invitation (e.g. `yoursite.com/dinner/`).

- **Netlify** — drag the `website` folder onto <https://app.netlify.com/drop>.
- **Vercel / Cloudflare Pages** — new project, upload the `website` folder (already built).
- **GitHub Pages** — put the contents of `website/` in a repository and enable Pages.
- **Hostinger / GoDaddy / cPanel** — File Manager → `public_html` (or a sub-folder) → upload everything
  inside `website/`.

> Test on a host (or with `npx serve website`), not by double-clicking `index.html`.

## Option B — the single file

`invitation-single-file.html` contains every image, the song and all code. Rename it to `index.html`
and upload it anywhere (it also opens by double-clicking). Needs internet for its fonts and code library.

## After it is online

1. **WhatsApp link preview** — in `index.html` (or the single file) replace `YOUR-SITE-ADDRESS` in
   `https://YOUR-SITE-ADDRESS/og-image-dinner.jpg` with your real address. Shared links then show the
   Ik Onkar, monogram, names, "Wedding & House Warming Dinner", the date, time and venue.
   (For the single file, upload `og-image-dinner.jpg` from the `website` folder next to it.)
2. **Open it on a phone**, tap once (music starts on the first tap), and scroll through.

## Optional: Call / WhatsApp buttons in the RSVP section

To let guests reply to a family member directly, add contacts in the source code (`src/content.js` →
`rsvp.contacts`, e.g. `{ name: 'Sukhvinder Singh Saluja', phone: '+919876543210' }`) and rebuild with
`npm run build:dinner` — each contact appears with **Call** and **WhatsApp** buttons.
