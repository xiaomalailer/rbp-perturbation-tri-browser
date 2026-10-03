# RBP Perturbation Tri-Browser

GitHub Pages site combining condition-specific RBP perturbation similarity browsers for K562, HCT116, and CD4+ T cells.

## Included datasets

- **K562:** 1,376 RBP perturbations; exact 2,319 author-defined HVGs; self-target masking; cosine similarity; Ward hierarchy; Dynamic Tree Cut `deepSplit=2` and `deepSplit=4`; lazy-loaded perturbation volcano plots and GO-BP results.
- **HCT116:** 985 unique RBP perturbations selected with `n_consensus_degs > 5`; 2,000 predefined HVGs; self-target masking; cosine similarity; Ward hierarchy; Dynamic Tree Cut `deepSplit=2`.
- **CD4+ T cells:** three independently analyzed conditions—Rest (772), Stim8hr (846), and Stim48hr (807)—selected with strict `n_downstream > 5`; all 10,282 measured genes; z-score profiles; self-target masking; cosine similarity; Ward hierarchy; Dynamic Tree Cut `deepSplit=2` and `deepSplit=4`; improved volcano plots, direction-specific GO-BP enrichment, and on-target KD efficiency/significance metrics.

Each browser is isolated under `k562/`, `hct116/`, or `cd4/`, so switching the top-level navigation does not mix feature definitions or analysis metadata.

## Local preview

```bash
python3 -m http.server 8766 --directory /home/kaiquan/rbp-perturbation-tri-browser
```

Then open <http://localhost:8766/>.

## GitHub Pages URL

<https://xiaomalailer.github.io/rbp-perturbation-tri-browser/>
