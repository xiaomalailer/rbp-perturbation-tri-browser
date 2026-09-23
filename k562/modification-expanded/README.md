# K562 Modification Seed–Partner Browser

Interactive browser for 65 AD>5 modification-enzyme seeds plus 105 unique AD>5
gene perturbations selected among each seed's top five Pearson partners at
r>=0.3. HDBSCAN uses min_cluster_size=4 and min_samples=3; density-defined
noise is retained as module 0.

Serve this directory over HTTP; for example:

```bash
python3 -m http.server 8000 --directory browser
```

Then open `http://localhost:8000`. The site has no upload feature and does not
publish the source `.h5ad`, GMT, or intermediate analysis files.
