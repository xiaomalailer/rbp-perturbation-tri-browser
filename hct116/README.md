# HCT116 RBP cosine-similarity browser

Static browser for the 985 unique HCT116 RBP perturbations selected by
`n_consensus_degs > 5`. Similarity uses 2,000 predefined HVGs after setting a
perturbation's own target-gene response to zero when the target is an HVG.

The browser includes the cosine-similarity heatmap, the Ward dendrogram,
Dynamic Tree Cut modules (`deepSplit=2`, `minClusterSize=20`), RBP search,
nearest-neighbor ranking, branch/module inspection, block zooming, and CSV
export.

Open `index.html` directly, or serve the directory locally:

```bash
python3 -m http.server 8000 --directory /home/kaiquan/HCT116_perturbseq/browser
```

Then open `http://localhost:8000`.

Rebuild the data payload from the saved analysis outputs with:

```bash
/home/kaiquan/.conda/envs/rbp-vscode/bin/python \
  /home/kaiquan/HCT116_perturbseq/build_similarity_browser.py
```
