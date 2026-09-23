# RBP Perturbation Tri-Browser

This is a new, independent GitHub Pages site that combines the latest
high-variable-gene RBP perturbation browsers for two cell lines and reserves a
third navigation slot for CD4+ T cells.

## Included datasets

- **K562:** 1,376 RBP perturbations; exact 2,319 author-defined HVGs;
  self-target masking; cosine similarity; Ward hierarchy; Dynamic Tree Cut
  `deepSplit=2` and `deepSplit=4`.
- **HCT116:** 985 unique RBP perturbations selected with
  `n_consensus_degs > 5`; 2,000 predefined HVGs; self-target masking; cosine
  similarity; Ward hierarchy; Dynamic Tree Cut `deepSplit=2`.
- **CD4+ T cells:** navigation placeholder for a future dataset.

The two browsers remain isolated under `k562/` and `hct116/`, so switching the
top-level navigation does not mix their feature definitions or analysis
metadata.

## Local preview

```bash
python3 -m http.server 8766 --directory /home/kaiquan/rbp-perturbation-tri-browser
```

Then open <http://localhost:8766/>.

## Intended GitHub Pages URL

<https://xiaomalailer.github.io/rbp-perturbation-tri-browser/>

This repository is separate from `rbp-perturbation-browser`; publishing it does
not modify the existing site.
