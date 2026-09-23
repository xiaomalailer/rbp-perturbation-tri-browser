# K562 Modification-Enzyme Perturbation Browser (Li Lab)

Static public browser for 65 K562 RNA-modification-enzyme perturbations retained
by maximum-AD guide deduplication and the strict AD>5 filter. It includes
HDBSCAN similarity maps, functional annotations, and lazy-loaded volcano and
GO Biological Process results for every perturbation. HDBSCAN uses Euclidean
distance on complete Pearson-similarity profiles with min_cluster_size=4 and
min_samples=3; density-defined noise is retained as module 0.

Serve this directory over HTTP; for example:

```bash
python3 -m http.server 8000 --directory browser
```

Then open `http://localhost:8000`. The site has no upload feature and does not
publish the source `.h5ad`, GMT, or intermediate analysis files.
