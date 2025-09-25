
# Neuro Lite Starter (JupyterLite)

A zero-server, browser-only dashboard for neuroscience data using **JupyterLite** (Python in the browser).

## Quick start

1. **Create a new GitHub repo** and upload this project.
2. In the repo **Settings → Pages**, set: Source = "GitHub Actions".
3. Push to `main`. The included workflow builds the site and publishes to GitHub Pages.
4. Open your site at: `https://<youruser>.github.io/<yourrepo>/`.
5. Click **Start.ipynb** → choose the **built-in sample** → open **Dashboard.ipynb**.

## Add your real data packages

- Convert your data to **CSV** (tables) and **NPZ** (NumPy arrays).
- Zip each package so users download once. Inside the zip, place files with the same names used in the sample (`meta.csv`, `tuning_curves.npz`, `psth.npz`). You can add more.
- Host the zips on object storage or any static host with **CORS** enabled.
- Edit `content/Start.ipynb`: add entries to the `packages` list:
  ```python
  packages = [
      {"name":"Set A (200 MB)","id":"setA","zip_url":"https://.../setA.zip","size_mb":200},
      {"name":"Set B (350 MB)","id":"setB","zip_url":"https://.../setB.zip","size_mb":350},
  ]
  ```
- Users pick a set, click **Download**, and JupyterLite stores it locally in the browser (IndexedDB). The dashboard then runs on the local files (fast).

## Customize the dashboard

- Edit `content/Dashboard.ipynb` to add filters (ipywidgets) and plots (matplotlib).
- Add more notebooks (e.g., `Rasters.ipynb`) and read from the **current package** using the helper in the dashboard.

## Notes

- JupyterLite runs Python via Pyodide; only **pure-Python** packages are supported.
- For large data, split into **200–300 MB** packages; users can switch packages from **Start.ipynb**.
- Everything runs client-side; no user needs Python or MATLAB installed.
