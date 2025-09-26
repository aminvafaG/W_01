# JupyterLite + Voici (single GitHub Pages site)

This repo builds a **single static site** that contains both:
- **JupyterLite Lab** (full JupyterLab UI), and
- **Voici** (static dashboard rendering of your notebooks).

## How to use

1. Push this repo to GitHub (or create one from it).
2. In GitHub → *Settings* → *Pages*, set **Source** to *GitHub Actions*.
3. Push to `main`. The included workflow will build and deploy to Pages.

When deployed under `https://<USER>.github.io/<REPO>/`, your main links are:

- JupyterLab (opens the notebook):  
  `https://<USER>.github.io/<REPO>/lab/index.html?path=App.ipynb`

- Voici (renders the notebook as an app):  
  `https://<USER>.github.io/<REPO>/voici/render/App.html`

> Tip: Replace `App.ipynb` with your own notebooks (add them to the `content/` folder).

## Add packages
Packages are pre-installed at build-time using `environment.yml` (via `emscripten-forge` and `conda-forge`).  
Add packages there (only `noarch` or `emscripten-forge` packages are supported in the browser).

## Local build (optional)
```bash
python -m pip install -r requirements-build.txt
jupyter lite build --contents content --output-dir _site --apps lab --apps voici
python -m http.server 8000 --directory _site
# then open http://localhost:8000
```
