# GRAMA Website

Static multi-page site for [gramagovernance.com](https://gramagovernance.com), served via GitHub Pages (custom domain set in `CNAME`).

## Structure

```
index.html                     Home page (about, JEEViKA partnership, research, team)
other-initiatives.html         "Other Initiatives" — links out to the Cancer Care Initiative (sacci.net)
research-*.html                One page per policy brief, linked from the Research section on index.html
css/research.css               Shared stylesheet for all research-*.html pages
images/
  site/                        Logo, OG preview image, hero photo
  banners/                     Homepage rotating banner strip
  research/                    Research page thumbnails
  team/                        Team headshots
  content/                     In-page story/content photos (JEEViKA meetings, MOU signings)
pdfs/                          Downloadable policy briefs, linked from each research-*.html page
```

The Cancer Care Initiative previously lived here under `cancer-care/`; it now runs as its own site in the separate `sacci-net` GitHub repo, deployed to sacci.net. `other-initiatives.html` links straight out to it.

## Adding a new research page

1. Copy an existing `research-*.html` as a template — it already links to `css/research.css`.
2. Update the `<title>`, meta tags (description, canonical, OG/Twitter — all point to `https://gramagovernance.com/<filename>`), `<h1>`, and summary text.
3. Drop the thumbnail image in `images/research/` and the PDF in `pdfs/`.
4. Add a `.research-card` entry linking to the new page in `index.html`'s Research section.

## Adding images

Team photos: crop to 5:6 ratio (~800×960px, 2x for retina). Research thumbnails: square-ish (~1000px on the long edge). Keep file sizes reasonable — resize before adding rather than uploading originals straight from a camera/phone.

## Deploy

This repo *is* the live site — pushes to `main` deploy automatically via GitHub Pages (Settings → Pages → branch `main`, root). `CNAME` points it at `gramagovernance.com`.

## Contact Form

The Send button on the homepage shows an alert placeholder. To make it work, wire it up to [Formspree](https://formspree.io) (free tier available).
