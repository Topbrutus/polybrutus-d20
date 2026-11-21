# Polybrutus 20D: Exact Conservative Euclidean Completion and a Fourteenfold Weighted-Graph Mode

**Research author:** Gabriel St-Pierre  
**Affiliation:** Independent researcher  
**Programme:** Polybrutus-X72  
**Date:** 20 November 2026  
**Version:** 0.1.0  
**Status:** Reproducible mathematical computational preprint, not independently human peer reviewed  
**Parent publication:** Polybrutus 19D, DOI 10.5281/zenodo.24409343  
**Frozen source:** https://github.com/Topbrutus/polybrutus-d20/tree/v0.1.0 (upon release)

## Abstract

We construct an exact **twenty-five-point labelled Euclidean distance configuration** whose minimum affine embedding dimension is **twenty**, conservatively preserving all **276 predecessor labelled pairwise squared distances** of the archived Polybrutus 19D metric. One new unit-radius point perpendicular to the predecessor configuration adds **24 squared distances equal to 2R²**, producing **300 labelled pairs** in eight exact normalized squared-distance families. Exact coordinate-difference rank and centered Euclidean distance Gram rank are both twenty; positive semidefiniteness follows from an explicit algebraic Gram factorization. A separately implemented rational verifier reconstructs all 300 labelled squared distances without importing the geometric point generator.

For a deliberately **chosen theoretical complete weighted-graph scalar-oscillator model**, with unit scalar masses and couplings `w_ij=R²/d_ij²`, the exact 25-by-25 weighted Laplacian has eigenvalue **25/2 of multiplicity fourteen** and eigenvalue **12 of multiplicity four**. The exact root multiplicities and the complete characteristic-polynomial factorization are verified by two differently implemented programs. This is a reproducible case study in established Euclidean and spectral mathematics, **not a discovery of a physical twenty-dimensional universe, measured resonance, particle, or new universal theorem**.

## 1. Research context and immutable predecessor

Polybrutus originates from seven analytically specified radius-R points on a two-sphere embedded in three-dimensional Euclidean space. The first higher-dimensional metric was an exact conservative seven-dimensional configuration: five regular-simplex points in an orthogonal four-dimensional subspace were added without altering the original seven points, yielding twelve vertices and sixty-six labelled pair distances (Polybrutus 7D, DOI 10.5281/zenodo.24407952).

The programme subsequently archived stepwise orthogonal extensions: 8D (13 vertices, 78 pairs, DOI 10.5281/zenodo.24408344), 9D (14, 91, 10.5281/zenodo.24408448), 10D (15, 105, 10.5281/zenodo.24408569), 11D (16, 120, 10.5281/zenodo.24408650), 12D (17, 136, 10.5281/zenodo.24408720), 13D (18, 153, 10.5281/zenodo.24408769), 14D (19, 171, 10.5281/zenodo.24408836), 15D (20, 190, 10.5281/zenodo.24408887), 16D (21, 210, 10.5281/zenodo.24408979), 17D (22, 231, 10.5281/zenodo.24409067), 18D (23, 253, 10.5281/zenodo.24409207), and 19D (24, 276, 10.5281/zenodo.24409343).

The present D20 result starts **exclusively** from `Topbrutus/polybrutus-d19@v0.1.0`, immutable Git source commit `1aa9721edcf6eb374a301863a5c1c4e566e69838`. The earlier frozen program chain and exact labelled-distance certificates are included without alteration under `prior/`. None of the earlier published scientific tags, geometry, Zenodo records or DOIs is modified.

## 2. Exact construction: twenty-five labelled points

At normalized radius `R=1`, take the twenty-four exact frozen D19 unit vectors `p1,...,p24`, represented in twenty coordinate-storage slots. A single exact linear constraint comes from the original five regular-simplex vertices in their centered four-dimensional hyperplane.

Embed every preceding vector into twenty-one storage slots:

```
q_i=(p_i,0),     i=1,...,24.
```

Adjoin the twenty-fifth radius-one point as a new perpendicular basis vector in the twenty-first slot:

```
q25=e21=(0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1).
```

All twenty-five vectors have unit norm; `q25` is orthogonal to every old point. The exact 276 predecessor labelled squared distances remain unchanged. For each preceding `q_i`, the additional squared distance is:

```
||q25-q_i||²=||q25||²+||q_i||²-2<q25,q_i>=2.
```

Scaling every coordinate by a general radius `R>0` changes every squared distance by `R²`. Thus each newly introduced pair squared distance is `2R²`, and the full labelled pair count is:

```
C(25,2)=300=276+24.
```

Define the normalized exact squared-distance class parameter `k=4d²/R²`. Its complete histogram is:

| k | 4 | 7 | 8 | 9 | 10 | 12 | 13 | 16 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Labelled pairs | 6 | 2 | **269** | 3 | 10 | 6 | 2 | 2 |

The eight counts sum to 300; the exact squared pair-distance total is

```
sum_{i<j}d_ij²/R²=2447/4.
```

At radius one the twenty-one-slot centroid is:

```
G=(0,0,1/50,0,0,0,0,0,1/25,1/25,1/25,1/25,1/25,1/25,
   1/25,1/25,1/25,1/25,1/25,1/25,1/25).
```

The **intrinsic affine dimension is twenty**, not twenty-one; the extra coordinate slot is an exact centered-simplex redundancy.

## 3. Exact centered Gram and minimal affine rank

Let `X` be the exact 25-by-21 stored coordinate matrix and `D` the 25-by-25 symmetric matrix of **squared labelled Euclidean distances**. Define the centering projection `H=I-11ᵀ/25` and centered Gram

```
B=-(1/2)HDH.
```

The primary symbolic program establishes without floating-point approximation:

```
rank([q2-q1,...,q25-q1])=20;
rank(B)=20;
B=(HX)(HX)^T.
```

The final identity gives an exact **positive-semidefinite factorization** and certifies Euclidean realizability. Since a complete labelled Euclidean squared-distance matrix uniquely determines its centered Gram, any Euclidean point configuration with exactly these 300 labelled pair distances must have minimum affine dimension **twenty**. The result does not imply a physical spacetime of twenty dimensions.

The second independently implemented verifier reconstructs all 300 squared distances using only rational structural distance rules: the original seven-point coordinate differences are encoded by a rational quadratic form, five regular-simplex vertices have internal squared distances `5/2`, and each appended unit point is orthogonal to all preceding subspaces. The checker does **not** import the main or parent coordinate generators. It verifies **300/300 labelled distances**, all **276** frozen predecessor pairs, and centered Gram rank **20**.

## 4. Fourteenfold eigenvalue in a selected ideal oscillator graph

For illustration only, choose a complete weighted graph on the twenty-five points, with equal unit scalar oscillator masses and pair couplings `w_ij=R²/d_ij²`. This is a **modelling definition**; it is not derived from any instrument or experiment.

The new twenty-fifth vertex lies at squared distance 2 from all twenty-four old points (for R=1), so each of its new graph edges has weight `1/2`. Let `L19` denote the predecessor 24-by-24 graph Laplacian and `L20` the new 25-by-25 graph Laplacian. Exactly:

```
L20=[ L19+(1/2)I24       -(1/2)1 ]
    [ -(1/2)1ᵀ                  12 ].
```

The resulting decomposition into the global uniform zero mode, the new intergroup differential mode, and the shifted preceding nonuniform modes gives an exact characteristic-polynomial recurrence:

```
chi25(z)=z(z-25/2)chi24(z-1/2)/(z-1/2).
```

The frozen D19 case established the exact polynomial

```
chi24(z)=z(z-12)^13(z-23/2)^4*f6(z-17/2),
f6(z)=chiP7(z)/z,
```

where `chiP7` is the weighted characteristic polynomial of the original seven-point graph and `f6` comprises its six nonzero modes. Substitution yields:

```
chi25(z)=z(z-25/2)^14(z-12)^4*f6(z-9).
```

The primary exact verifier explicitly computes the **complete 25-by-25 characteristic polynomial** and proves equality to both the recurrence and this factored form. It checks `f6(7/2)!=0` and `f6(3)!=0`, excluding coincident additional eigenvalues at the named roots. Therefore **25/2 has multiplicity exactly fourteen** and **12 has multiplicity exactly four**.

The independent rational-metric program reconstructs the complete graph separately and checks both multiplicities by vanishing and nonvanishing derivatives of its own full characteristic polynomial. These eigenvalues are dimensionless **abstract model properties**, not measured oscillations in hertz or evidence of a new physical particle.

## 5. Reproduction, negative controls and archival integrity

The source repository contains `src/verify_d20.py` (primary exact coordinates, labelled metric, Gram, graph spectrum), `tests/independent_d20.py` (independent rational distance and graph certificate), `results/certificate_d20.json` (all 300 exact labelled squared distances), original predecessor source and certificates in `prior/`, mathematical proof, specification, GitHub Actions workflow and SHA-256 index.

Reproduce the tests:

```sh
python -m pip install sympy==1.14.0
python src/verify_d20.py
python tests/independent_d20.py
```

Both programs must report PASS and the same SHA-256 for the regenerated JSON certificate. Four deliberately false cases are detected: one modified labelled squared distance; a duplicate new point reducing rank; a tilted point violating perpendicularity; and a label swap which preserves the unlabelled histogram but changes the labelled metric.

The Zenodo scientific record will contain exactly three archived artifacts: source ZIP generated directly from the immutable successful `v0.1.0` Git tag, this PDF preprint and the complete exact 300-pair JSON certificate. Source SHA-256 and archived file checksums support byte-level validation.

## 6. Scientific precedence and interpretative boundaries

Orthogonal Euclidean completion, centered Euclidean distance Gram reconstruction and uniform weighted-graph Laplacian joins are established mathematical methods. This is a reproducible **specific Polybrutus 20D case study**: it does not invent a new universal theorem or establish any extra physical spacetime dimension, experimentally measured resonance, elementary particle interaction or novel physical law. Independent human mathematical peer review has not occurred.

**Human author and scientifically responsible investigator:** Gabriel St-Pierre, independent researcher, who originated the Polybrutus programme and directs its staged dimensional research.

**Generative AI disclosure:** OpenAI ChatGPT (Astra) substantially assisted exact symbolic mathematical verification, the primary and separately implemented rational verifier programs, theoretical graph spectral derivation, source ancestry checks, preprint drafting, documentation and GitHub/Zenodo archival operations. The AI tool is **not a research author**.

**Rights:** manuscript and narrative prose CC BY 4.0; scientific source programs MIT.

**Sources:** initial Polybrutus specification https://github.com/Topbrutus/polybrutus/blob/main/SPECIFICATION.md ; predecessor 19D source https://github.com/Topbrutus/polybrutus-d19/tree/v0.1.0 ; predecessor DOI https://doi.org/10.5281/zenodo.24409343 ; full earlier published DOIs recorded in the repository's `PROVENANCE.md`.
