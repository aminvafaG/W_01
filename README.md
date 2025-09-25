# JupyterLite + Voici (Dashboard‑Only) Starter

This repo is set up to publish a **dashboard‑only** page at:

```
https://<your-username>.github.io/<your-repo>/voici/render/App.ipynb
```

## How it works

- Put your notebook(s) in `content/`. The main one should be named **`App.ipynb`**.
- Put your data files under `files/` (for example, `files/data/data.csv`).
  - Read them at runtime from Python via paths like `/files/data/data.csv`.
- The GitHub Action in `.github/workflows/voici.yml` builds the static site with **Voici** and deploys it to GitHub Pages.
- **Only the output UI** is shown (code is hidden), like Voilà.

## Quick start

1. Replace `content/App.ipynb` with your real dashboard notebook (keep the same name).
2. Add your dataset (e.g., `data.csv`) to `files/data/`.
3. Commit to `main` and push.
4. In your repo settings, enable **Pages** → **Source: GitHub Actions**.
5. After the action runs, open:

```
https://<your-username>.github.io/<your-repo>/voici/render/App.ipynb
```

## Notes

- If your notebook needs Python packages not bundled with Pyodide, use `piplite`/`micropip` inside the notebook to install web‑friendly wheels at runtime.
- Large files: keep data compact or consider pre‑aggregating.
- If you want a landing page redirecting to the app, keep `index.html` at the repo root.
