# CD4+ T-cell RBP perturbation browser

Static browser for three independently analyzed conditions: Rest, Stim8hr, and Stim48hr. Each condition retains curated RBP perturbations with strict `n_downstream > 5`, uses all 10,282 measured genes from the h5ad `zscore` layer, masks the matching self-target response, computes cosine similarity, and clusters complete similarity profiles with Ward linkage. Dynamic Tree Cut results are available at `deepSplit=2` and `deepSplit=4` with `minClusterSize=20`.

Per-perturbation response data are lazy-loaded. Volcano plots use the self-target-masked z-score on the x-axis and `-log10(adj_p_value)` on the y-axis. Negative and positive response genes are defined by `adj_p_value < 0.1` and the z-score sign. Only five prioritized labels per direction are placed in collision-separated side lanes.

GO Biological Process enrichment is calculated separately for negative and positive significant response genes, following the K562 browser implementation: one-sided hypergeometric tests against the 10,282 measured-gene background, MSigDB `c5.go.bp.v2026.1.Hs.symbols.gmt`, term sizes 5–500, at least two overlapping genes, and BH FDR < 0.05. Up to 25 terms per direction are displayed.

The detail panel also reports the unmasked target-gene log2 fold change, z-score, adjusted p-value, the author-provided `obs.ontarget_significant` call, and estimated knockdown efficiency calculated as `100 * (1 - 2^log2FC)`.
