# W_01 — Voici Dashboard (GitHub Pages)

This repo publishes a **code-free dashboard** with [Voici](https://voici.org) to GitHub Pages.

- Notebook: `content/App.ipynb`
- Live page: `/App.html` (built by the workflow)
- Data files: put under `content/data/`:
  - `meta.csv`
  - `tuning_curves.npz`
  - `psth.npz`

If the real data files are missing, the app generates small **demo** data so the page still works.

## Local dev
You generally don't need to run locally; GitHub Actions builds the static site.
