# Polybrutus D20 — Exact Gram and spectral verification

## 1. Preserve full labelled predecessor geometry

Starting with 24 exact unit-radius vectors and their 276 labelled squared pair distances from frozen Polybrutus D19, append a zero coordinate to every point and add one new perpendicular unit basis vector. All old distances are identical. Each new squared distance is `||q25-q_i||²=2`, for i=1,...,24. This yields 276+24=**300** labelled pair distances, eight exact normalized families and squared-distance sum `2447R²/4`.

## 2. Minimum Euclidean affine dimension

Let `X` be the 25-by-21 exact coordinate matrix, `D` the 25-by-25 **squared distance** matrix, and `H=I-11ᵀ/25` the centering projection. The primary verifier proves:

```
rank([q2-q1,...,q25-q1])=20
rank(B)=20
B=-(1/2)HDH=(HX)(HX)^T.
```

The final equality certifies positive semidefiniteness. A complete labelled Euclidean squared-distance matrix uniquely fixes its centered Gram, so any Euclidean realization of this exact 300-pair labelled metric has minimal affine dimension **20**. The 21 storage slots include one exact simplex redundancy.

## 3. Selected weighted graph spectrum

Choose a complete positive weighted graph with equal unit scalar masses and weights `w_ij=1/d_ij²` at R=1. The new vertex has 24 edges of weight 1/2. For the predecessor weighted Laplacian `L19`:

```
L20=[ L19+(1/2)I24  -(1/2)1 ]
    [ -(1/2)1ᵀ            12 ].
```

Separating global zero mode, group-differential mode and shifted preceding modes yields:

```
chi25(z)=z(z-25/2)*chi24(z-1/2)/(z-1/2).
```

The frozen D19 spectrum satisfies `chi24(z)=z(z-12)^13(z-23/2)^4*f6(z-17/2)` with `f6(z)=chiP7(z)/z`. Substitution gives:

```
chi25(z)=z(z-25/2)^14(z-12)^4*f6(z-9).
```

The primary program computes the entire 25-by-25 exact characteristic polynomial and verifies the recurrence and closed form. It checks `f6(7/2)!=0` and `f6(3)!=0`, establishing multiplicities **exactly 14** at 25/2 and **exactly 4** at 12. The separate rational metric program independently calculates the graph and certifies the multiplicities using nonzero derivatives of its characteristic polynomial.

## 4. Independent falsification

All 300 labelled pair distances are reconstructed using separate rational structural rules and compared one by one to the JSON certificate, including every predecessor pair. Four negative controls reject altered distances, a duplicate new point that lowers rank, a tilted nonorthogonal point, and point-label permutation that retains the histogram but violates the labelled metric.

**Interpretation:** this is an exact synthetic 20-dimensional affine Euclidean metric and a chosen ideal graph model. It is not a measured physical frequency, a novel universal theorem, or independent human peer review.
