# POLYBRUTUS 20D — Exact Euclidean 25-point metric and fourteenfold ideal graph mode

**Human research author:** Gabriel St-Pierre, independent researcher.  
**Research status:** reproducible mathematical preprint, not independently peer reviewed by a human.  
**Generative AI disclosure:** OpenAI ChatGPT (Astra) substantially assisted exact mathematics, two separately programmed verification methods, theoretical spectral model, scientific writing and release operations. It is not an author.

## Certified exact results (normalized radius R=1)

- **25 labelled points**, **300 exact pairwise squared distances**, and minimum affine Euclidean embedding dimension **20**.
- All **276** predecessor Polybrutus D19 labelled squared distances are conserved, without moving any earlier point. One new orthogonal unit point adds **24** pair squared distances, each exactly **2**.
- Eight normalized distance classes `k=4d²/R²`: `{4:6,7:2,8:269,9:3,10:10,12:6,13:2,16:2}`.
- Sum of pairwise squared distances exactly `2447R²/4`.
- Exact coordinate-difference rank **20**, centered squared Euclidean distance Gram rank **20**, and positive-semidefinite certificate `B=(HX)(HX)^T`. Coordinates are stored in 21 slots but one original simplex-hyperplane constraint remains.
- **Chosen hypothetical complete weighted graph:** unit scalar masses and all-pairs weights `w_ij=R²/d_ij²`. Its Laplacian has eigenvalue **25/2 with multiplicity 14** and eigenvalue **12 with multiplicity 4**, as exact abstract graph properties, not physical frequencies.
- Two separately implemented exact SymPy/rational programs independently verify **300/300** labelled squared distances, rank and graph multiplicities. The primary program detects **four deliberately invalid configurations**.

## Reproduce

```sh
python -m pip install sympy==1.14.0
python src/verify_d20.py
python tests/independent_d20.py
```

The independent rational metric checker does not import the primary point generator. The `prior/` directory is copied unchanged from frozen `Topbrutus/polybrutus-d19@v0.1.0` (commit `1aa9721edcf6eb374a301863a5c1c4e566e69838`).

The source archive includes `results/certificate_d20.json` (all 300 labelled squared distances), both verifiers, `SPECIFICATION_D20.md`, `PREUVE_D20.md`, `PROVENANCE.md`, research note PDF and Markdown, full predecessor source and certificates, GitHub Actions, and `SHA256SUMS.txt` for frozen Git blobs.

**Parent DOI:** [10.5281/zenodo.24409343](https://doi.org/10.5281/zenodo.24409343).  
**Code license:** MIT. **Scientific manuscript license:** CC BY 4.0.

**Scientific limits:** Orthogonal Euclidean completion and uniform weighted-graph spectral shifts are established mathematical techniques. This is a particular reproducible 20D case study, not a new universal theorem, empirical resonance, or physical extra dimension.
