# DES INV 15 Project Site: SpinShelf

Static single-page site for a UC Berkeley **DES INV 15** (Fall 2026) design methodology course project.

## Files

- `index.html`: page content and section structure
- `styles.css`: layout, palette (CSS variables), and responsive styles
- `images/`: team photos (`minseo.jpg`, `leo.jpg`, `aadi.jpg`), creative matrix (`creative-matrix.png`), and source PDFs (`margaret-persona.pdf`, `abstract-ladder.pdf`)

Problem illustrations and charts are inline SVGs in `index.html`. Persona, abstract laddering, and creative matrix sections live after How Might We.

## Team photos

Team names and photos are already set in `index.html`. To replace a photo, overwrite the matching file in `images/` (keep the same filename and extension), or update the `src` on that person’s card. Circular crop is handled in CSS (`.media-placeholder--round`).

If an image fails to load, the grey labeled circle fallback still appears (`data-label` + `onerror`).

To replace an illustration SVG with a photo later, swap the `.illustration` block for a figure with an `<img>` and caption.

## Add a new section later

Copy an existing `<section id="..." class="section">` block, give it a new `id`, add a matching link in the sticky nav, and keep the same `.container` / `.section-header` pattern. Optional alternate background: add `section--alt`.

## Preview locally

Open `index.html` in a browser, or from this folder:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## Deploy free

### GitHub Pages

1. Create a GitHub repo and push this `project-site` folder (or put these files at the repo root).
2. In the repo: **Settings → Pages → Build and deployment**.
3. Set source to **Deploy from a branch**, branch `main` (or `master`), folder `/` (or `/docs` if you keep the site under `docs/`).
4. Save; the site URL appears on the Pages settings screen after a short publish delay.

### Vercel

1. Push the folder to GitHub (or import the directory in the Vercel dashboard).
2. In [Vercel](https://vercel.com): **Add New Project** → import the repo.
3. Set the **Root Directory** to this site folder if it is not the repo root.
4. Leave framework preset as **Other**; deploy. Vercel will host the static HTML/CSS.
