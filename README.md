# Varun Dusane, portfolio

Static site (no build step). Files: `index.html` (markup), `style.css`, `app.js` (all behaviour and content), `fonts/`, `img/`.
Serve the folder over http (for example `python3 -m http.server`) or deploy it to Vercel.

## Editing content
All site copy lives in the `SITE` object at the top of `app.js`
(hero, proof strip, case study cards, journey, process, toolkit, testimonials).
Any value set to `TODO` (or left empty) is **not shown** on the public page until you fill it in.

## Things you need to fill in
- **Resume PDF**: replace `resume.pdf` in the site root with your real file, then set `SITE.resume.pdfReady` to `true`.
  Until then the "Download resume" buttons use the Google Drive link.
- **Brand identities count** (proof strip): set `SITE.proof` item `brandIdentities` (`n: TODO`) once you have confirmed the number.
- **CloudSecure duration**: set `duration` on the CloudSecure card in `SITE.cases`.
- **Testimonials**: only entries with `name`, `role` and `quote` are shown. Anonymous quotes are never rendered.
  Add the real name and role for each client note to publish it.
- **Domain**: `SITE.siteUrl` and the canonical, `og:*`, `twitter:*` and JSON-LD tags in `<head>` assume
  `https://varundsnportfolio.vercel.app/`. Change them if your live domain is different.

## Sharing image
`img/og.jpg` (1200 x 630) is used for link previews.

## Contact scene
Email, phone and social links are in `SITE.contact` and `SITE.links` at the top of `app.js`. The two brochures on the desk open the catalogue viewer.
