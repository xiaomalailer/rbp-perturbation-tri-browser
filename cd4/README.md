# CD4+ T-cell RBP perturbation browser

Static browser for three independently analyzed conditions: Rest, Stim8hr, and Stim48hr. Each condition retains curated RBP perturbations with strict `n_downstream > 5`, uses all 10,282 measured genes from the h5ad `zscore` layer, masks the matching self-target response, computes cosine similarity, and clusters complete similarity profiles with Ward linkage. Dynamic Tree Cut results are available at `deepSplit=2` and `deepSplit=4` with `minClusterSize=20`.

Per-perturbation volcano data are lazy-loaded. The x-axis is the self-target-masked z-score and the y-axis is the h5ad `adj_p_value` on a reversed log scale. Negative and positive significant response genes use `adj_p_value < 0.1` and the z-score sign.
