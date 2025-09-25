# W_01 — JupyterLite + Voici (Dashboard-Only)

Open your dashboard after deployment at:
```
https://<your-username>.github.io/<your-repo>/voici/render/App.ipynb
```
For this repo it should be:
```
https://aminvafag.github.io/W_01/voici/render/App.ipynb
```

## How to use
- Your app notebook lives at `content/App.ipynb`. Replace it with your own if needed (keep the name).
- Data files for in-browser access go under `files/` (e.g., `files/data/data.csv`).
  - Read in Python with paths like: `/files/data/data.csv`.
- GitHub Action in `.github/workflows/voici.yml` builds and deploys to GitHub Pages.

## Deploy
1. Commit & push all files to the `main` branch.
2. In GitHub → **Settings** → **Pages** → set **Source** to **GitHub Actions**.
3. After the workflow completes, visit the URLs above.
