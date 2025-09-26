# W_01 — Dashboard (Voici + JupyterLite)

- Voici (code‑free): `/W_01/voici/render/App.html`
- JupyterLite Lab:   `/W_01/lab/index.html?path=App.ipynb`

Build locally (optional):
```
pip install voici "jupyterlite[lab]" jupyterlite-pyodide-kernel libarchive-c
voici build --contents content --output-dir _output --base-url /W_01/ --overwrite
jupyter lite build --contents content --output-dir _output_lite --base-url /W_01/lab/
mkdir -p _output/lab && cp -r _output_lite/* _output/lab/
```
