# W_01 — Voici (JupyterLite) Dashboard

This repo skeleton lets you publish a **code-free dashboard** from a Jupyter notebook using **Voici** (static Voilà on top of JupyterLite).

## How to use
1. Replace `content/App.ipynb` with **your actual notebook** (keep the filename `App.ipynb`).
2. Put any data files under `content/data/` (or adjust your notebook paths).
3. Commit to your repo (`main` branch).  
4. Ensure GitHub Pages is set to **Source: GitHub Actions**.
5. After the workflow finishes, open:

```
https://<your-username>.github.io/<your-repo>/voici/render/index.html?path=App.ipynb
```

## Files
- `build-environment.yml` — tools for the GitHub Action to build the static site.
- `environment.yml` — **browser runtime** packages (xeus-python + libs) that run in WebAssembly.
- `.github/workflows/voici.yml` — build & deploy to Pages.
- `content/` — notebooks and assets published to the site.
  - `index.html` — auto-redirects to the dashboard.
  - `App.ipynb` — **placeholder**; replace with your notebook.
  - `data/` — put your CSV/parquet/etc. here (empty).
